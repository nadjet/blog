---

title: "My cherry-picked highlights from the EMNLP'21 Conference"
date: 2021-11-20T20:17:02+01:00
draft: false
tags: ["NLP", "conference"]


---

A couple of weeks ago I attended virtually the EMNLP'2021 Conference. This is the first time I attend a conference virtually. I must admit  <!--more--> this is not without its advantages: cheaper registration fees, no Jet-Lag, the ability to get your brain blasted in the comfort of your own home, the ability to switch between sessions much more quickly than if it was in a physical setting, as well as in my experience, a more "intimate" one-to-one interaction during the poster sessions. 

On the negative side, technical network problems meant the presentations were often recorded with no time for questions, and the likeliness that you will bump into someone you know is less likely, although I enjoyed "stalking" presenters to their poster rooms in "Gather Town", the virtual conference venue :-)... 


Below are some interesting talks I "attended" at the conference, organized by topic:

- [Bias and Ethics](#bias)
- [Language Models as Knowledge Bases](#lms_kbs)
- [Pattern Exploiting Training (PET)](#pet)
- [Datasets](#datasets)
- [Question Answering](#q_a)
- [Text mining](#text_mining)


# <a name="bias"></a>Bias and Ethics 

## Bertology

Several papers examined the biases of Pretrained Language Models (PLMs) from different angles, using principally the so-called Cloze Prompt Test (CPT). I sometimes think though that examining those Language Models using the Cloze Prompt Test is akin to a close-lookup through a keyhole at something big and complex... For example, [this paper](https://aclanthology.org/2021.emnlp-main.375/) examined PLMs bias towards specific demographic groups, [that paper](https://aclanthology.org/2021.emnlp-main.111/) what stereotypes PLMs learn about specific social groups, and [that other paper](https://aclanthology.org/2021.emnlp-main.150/) how Bert and other language models treat gender as binary as opposed to something more gender-fluid and perpetuate this bias in downstream tasks.

[This paper](https://aclanthology.org/2021.emnlp-main.42/) examines ethnic bias on Monolingual Language Models (MLMs) such as Korean, English and German MLMs, and proposes a metric to quantify this bias and two approaches for mitigating this bias, one of which is the use of Multilingual Language Models. One telling example about this ethnic bias is cited by the authors regarding Toxic Classification task on the Jigsaw Toxic Comment Classification training set: 2% of the sentences containing the word "Italy" are toxic and 6.5% of the sentences containing the word "Afghanistan" are toxic. Yet this translates into 1.3% False Positives for sentences with "Italy" in them vs a whooping 12% FPs for sentences with "Afghanistan"! 

## The Ethics of mining implicit information

Not wanting to pick on a single work but I listened with great interest to [PRIDE: Predicting Relationships in Conversations](https://aclanthology.org/2021.emnlp-main.380/). The author implements a classifier to detect relationships in conversations using film dialogues. The relations are crowdsourced and classification takes into account a number of features including relationship dimensions (equal/hierarchical, intense/superficial, temporary/long term, etc). I couldn't help thinking this is extracting information that is implicit in the dialogue which the user might not necessarily be willing to give. In the same way that we anonymize Personal Identifier Information, revealing a person's relation with another one might also be sensitive.


## LT and Critically Endangered Languages

Steven Bird in his keynote on "LT4All? Rethinking the agenda", questions, as the title says, whether we must provide Language Technology for all languages, including Critically Endangered Languages (CELs). He seemed to say that this is advocated as a means to preserve those CELs. Instead, he points that LT should expand onto trade languages and regional varieties which could act as pivots to those CELs (after all, most CELs speakers speak a pivot language). He also points out that speakers of CELs are not particularly interested in traditional LT applications such as Speech-to-Text (Transcription) or MT but instead want, for instance, Language Learning tools, so-called ComputEL, i.e., Technology for Endangered Languages. In other words LT must be made with its final specific users and user groups in mind.

I really liked that he reminded us of the role of Language and therefore LT as Communication as opposed to a dry Language Encoding-Decoding endeavor, and also that each group, community and individual convey messages according to their own culture, beliefs and organization: there is no one size fits all model.


# <a name="lms_kbs"></a>Language Models as Knowledge Bases

Whilst some researchers work on uncovering Contextual Language Models' various biases (see above), others have wondered about CLMs ability to learn knowledge. For evaluating CLMs capabilities as KBs, Facebook's [LAMA](https://github.com/facebookresearch/LAMA) probe is a commonly used resource: it allows to evaluate CLMs on Cloze Tests with masked entities aka knowledge. In [this paper](https://aclanthology.org/2021.emnlp-main.388/), the authors present BioLAMA, which is a benchmark of 49K biomedical factual knowledge triples for probing biomedical LMs such as BioBert.

In [this paper](https://aclanthology.org/2021.emnlp-main.81/), the authors present an exhaustive review of the use of Contextual Language Models (CLMs) as Knowledge Bases (KBs).  Approaches to CLMs as KBs can be implicit through word associations, that is the CLM has learnt some knowledge through its indirect exposure to it on large amounts of textual training data. 

Other approaches can be explicit, using entity-level supervision or relation-level supervision. In Entity Level Supervision Approaches, the goal may be to output entity mentions, for example by masking mentions in the texts and training the CLM to predict them. Other Entity Level Supervision Approaches not only model entities but also link those entities to a specific reference in a KB, hence performing entity linking. This modelling can be done in the latter layer of the CLM architecture by outputting entity reference tokens as in [this](https://aclanthology.org/K19-1063.pdf). Or it can be done in middle layers or early layers of the CLM architecture: for example entity reference tokens can be modelled in the embedding layer of the CLM, hence performing entity linking by early fusion with the CLM. Finally, the authors present approaches that incorporate KB relations in the CLM.


# <a name="pet"></a>Pattern Exploiting Training


I hadn't heard about Pattern Exploiting Training (PET) before this conference. In PET for classification, multiple models are trained on a Clozed Prompt Test word prediction task, one per instruction, with only a two or three examples per instruction. Then a set of unlabelled examples are processed with each model, and the output distributions for each example are averaged to get soft labels. This softly labelled dataset is then used to train a classifier.

 This technique is adapted in [Few-Shot Text Generation with Natural Language Instructions](https://aclanthology.org/2021.emnlp-main.32/) to few-shot summarization generation, where pattern input and instruction to summarize is given to an encoder or pattern input is given to encoder and instruction to summarize to decoder. Final summary with highest probability is selected.
 
 It is also applied in [this work](https://aclanthology.org/2021.emnlp-main.845/) that develops a semi-supervised approach for few-shot exaggeration detection. They implement 2 different tasks for PET, namely exaggeration detection and claim strength prediction and train several models for different templates based on a small seed annotated dataset. 
 
# <a name="datasets"></a>Datasets

There was quite a few papers focusing on datasets and benchmarks, most notably [Huggingface's community library of datasets](https://arxiv.org/abs/2109.02846), which encourages better documentation and seamless use of datasets within their library, and [Hugginface's C4](https://aclanthology.org/2021.emnlp-main.98/) aka "Colossal Clean Crawled Corpus", which argues that when scraping datasets from the web, one should know the provenance of the data, what it includes and what it does not, and be aware of overlap between different datasets. A [UI](https://c4-search.apps.allenai.org/) is made available where one can check the content of the C4 corpus.

I also found it interesting to hear about datasets that focus on implicit or "hard" examples:

- In [this paper](https://aclanthology.org/2021.emnlp-main.29/), the authors propose a taxonomy of implicit hate speech and develop a dataset of tweets with implicit hate speech mined from different "hate groups", crowdsourced for target and category. They showcase this dataset by implementing a binary and multi-class classifier and training a generative model which, given a sentence, produces the implicit statement. 

- In [that paper](https://aclanthology.org/2021.emnlp-main.568/), the  authors develop a multilingual dataset of product reviews for CounterFactual Detection (CFD). An example of counterfactual proposition in a review is ""It would be better if it had come with a leg rest", where obviously the product has no leg rest. Detection of these CFDs can be beneficial for many NLP applications such as sentiment analysis or question answering.


I also liked approaches that iteratively and semi-automatically build so-called datasets with "silver annotations" (as opposed to gold ones). In [A Large-Scale Dataset for Empathetic Response Generation](https://aclanthology.org/2021.emnlp-main.96/), the authors produce EDOS (Emotional Dialogue OpenSubtitle), a large dataset of empathetic dialogue turns annotated with fine-grained emotions and empathetic response intents. Having such a dataset is useful to improve empathetic responses of open conversational agents. The authors obtain an initial dataset by training an empathetic classifier on a small ground truth and applying this "weak classifier" on the subtitle dataset to gather the dialogues that convey the strongest emotions. A data augmention technique is then applied by manually annotating a small set of those emotional dialogues with Amazon Mechanical Turk using the weak labeller's top 3 predictions. The seed and augmented sets are used to train an initial emotion classifier which is used to label the data. The data with the strongest predictions are fed again back to the classifier as training data together with a smaller set of other strongly similar data. 


# <a name="q_a"></a>Question Answering


- In [this paper](https://aclanthology.org/2021.emnlp-main.708/), the authors use [Question Decomposition Meaning Representation](https://arxiv.org/pdf/2001.11770.pdf) as a "pivot language" to map a query in natural language to a SPARQL query. 

- The authors of [that paper](https://aclanthology.org/2021.emnlp-main.346.pdf) perform complex question answering over a knowledge base guided by a Relation Graph (RG) instead of a Knowledge Graph, where two entities are connected if they share entities as arguments. The reason for focusing on an RG instead of a KG is that it is much smaller: the number of relations is much smaller than the number ot entities. Their approach achieves SOTA performance on the [ComplexWebQuestion](https://www.tau-nlp.org/compwebq) (CWQ) dataset.

- In [Case-based Reasoning for Natural Language Queries over Knowledge Bases](https://aclanthology.org/2021.emnlp-main.755/), first similar questions to the input question are retrieved together with their logical form. Next the  input question's logical form is generated by reusing various components of the logical forms of the retrieved cases. The authors argue that this approach is scalable (you can add new unseen cases without necessity of retraining), explainable (you can understand where each part of the logical borrows from). Like above, this approach 
 achieves SOTA performance on the CWQ dataset.
 
- In [Open-Domain Q/A for COVID-19...](https://arxiv.org/abs/2110.06962), the authors perform retrieval and snippet extract from biomedical articles given a user question about covid. Each of these 2 steps is performed by training a classifier using a pretrained model. Also, [this paper](https://aclanthology.org/2021.emnlp-main.305/), a benchmark dataset for COVID-19 FAQ retrieval.


# <a name="text_mining"></a>Text Mining

- The [IBM's Project Debater API](https://arxiv.org/abs/2110.01029) demo provides a suite of functionalities for Argument Mining such as key point extraction (though it seems only available for English + you can't train your own models in the non-commercial free version).

- An approach for [Evaluating Scholarly Impact: Towards Content-Aware Bibliometrics](https://aclanthology.org/2021.emnlp-main.488/) is proposed, where the impact of a paper is measured by the overlap of concepts, modelled using Scispacy embeddings, between abstract of cited paper and citing paper as opposed to number of citations. One of the motivations for this work is that some online editing platforms request that authors cite papers of the same journal/platform, thus artificially increasing weight. 

- A pipeline for the [Named Entity Recognition of Chemical Compounds](https://aclanthology.org/2021.emnlp-main.424/) was presented that performs an iterative distant label supervision to annotate chemical elements in text using information from KBs, both for label matching and for disambiguation using the context of nearby entities/types in the ontology.

- In [Classifying Dyads for Militarized Conflict Analysis](https://aclanthology.org/2021.emnlp-main.613/), the authors extract a large knowledge graph about military conflicts from Wikipedia and represent entities in ally or enemy relationships. I thought this approach was a bit simplistic in its representations of those concepts, in that ally/enemy relationships are not fixed and may evolve over time and this is not reflected in the KG.

