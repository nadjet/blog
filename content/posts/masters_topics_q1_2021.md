---
title: "Data Science Projects (Q1-2021)"
date: 2020-10-10T12:11:38+01:00
draft: false
tags: ["master","Q/A","Knowledge graphs","DBPedia","NLG","Bert"]
---

This first quarter of the 2020-2021 academic year, I supervise 6 final year projects in the [Data Science Master](https://estudios.uoc.edu/es/masters-universitarios/data-science/presentacion) of the UOC University, ranging from the development of a COVID-19 FAQ-based Q-A system to building knowledge graphs and performing end-to-end Natural Language Generation. Below is a list of resources and references I offer to get the students started.

<!--more--> 


# Introduction to Natural Language Processing

- [A code-first introduction to Natural Language Processing](https://www.fast.ai/2019/07/08/fastai-nlp/), Fastai Course given by Rachel Thomas. Highly recommended.
- Real world Natural Language Processing. Manning edition. [First chapter of the book](https://livebook.manning.com/book/real-world-natural-language-processing/chapter-1/v-3/61).
- Natural Language Processing in Action: Understanding, analyzing, and generating text with Python. Manning edition. [First chapter of the book](https://manning-content.s3.amazonaws.com/download/a/c9fc557-b088-4f1f-87a8-7ea2e488d262/Lane_NLPiA_MEAP_V10_ch1.pdf)

# Wikipedia and DBPedia

- [Wikipedia mining: Wikipedia as a corpus for knowledge extraction](https://pdfs.semanticscholar.org/074a/960ad3b842061a2aeddb4a157f2a4d48931c.pdf?_ga=2.168954662.622148293.1582216407-1040985544.1579873591). K. Nakayama, M. Pei, M. Erdmann, M. Ito, M. Shirakawa, T. Hara, and S. Nishio. In Annual Wikipedia Conference (Wikimania), 2008.
- To download a small set of Wikipedia articles in xml format, paste the URIs (e.g., "Rafael_Nadal") in 
"Add pages manually" in [that page](https://en.wikipedia.org/wiki/Special:Export). To get the URIs given the names, you can query a [SPARQL endpoint](https://dbpedia.org/sparql).
- [DBpedia – A Large-scale, Multilingual Knowledge Base Extracted from Wikipedia](https://www.semanticscholar.org/paper/DBpedia-A-large-scale%2C-multilingual-knowledge-base-Lehmann-Isele/d2946a868682e4141beabc288d79253ae254c6e1), Jens Lehmann et al., Semantic Web Journal 2012
- [Wikipedia Data Science: Working with the World’s Largest Encyclopedia](https://towardsdatascience.com/wikipedia-data-science-working-with-the-worlds-largest-encyclopedia-c08efbac5f5c). How to programmatically download and parse Wikipedia. 
- [How to setup DBPedia and Geonames on OpenLink Virtuoso](https://medium.com/@nadjetba/how-to-setup-dbpedia-and-geonames-on-openlink-virtuoso-f203321fd0fe). 
- SPARQL and DBPedia: [article 1](https://medium.com/@humam.fauzi/sparql-and-dbpedia-cb68a005c5c5) and [article 2](https://medium.com/virtuoso-blog/dbpedia-basic-queries-bc1ac172cc09). 
 
# Building Knowledge Graphs from Texts

- [Mining Knowledge Graphs from texts](https://kgtutorial.github.io/), 2018 Tutorial 
-  [Knowledge Graph — A Powerful Data Science Technique to Mine Information from Text](https://medium.com/analytics-vidhya/knowledge-graph-a-powerful-data-science-technique-to-mine-information-from-text-with-python-f8bfd217accc)
- [Building a Large-scale, Accurate and Fresh Knowledge Graph](https://kdd2018tutorialt39.azurewebsites.net/KDD%20Tutorial%20T39.pdf), 2018 Tutorial: you will find definitions of what is a knowledge graph with references, techniques, etc.
- [Bring Order to Chaos: A Graph-Based Journey from Textual Data to Wisdom](https://graphaware.com/nlp/2018/09/26/bring-order-to-chaos.html), Blog Entry, 2018.
- [Concept Wikification for COVID-19](https://openreview.net/pdf?id=ylgU9BB1vEd). Automatically recognizes mentions of concepts related to COVID-19 in text and resolve them into Wikipedia titles.
- [Building a KG from a new dataset](https://adimen.si.ehu.eus/~rigau/publications/jws2016.pdf).
 
## Information Extraction and Text Mining tasks

- [Entity linking, a primary NLP task for Information Extraction](https://medium.com/analytics-vidhya/entity-linking-a-primary-nlp-task-for-information-extraction-22f9d4b90aa8).
- [Exploiting semantic similarity for named entity disambiguation in knowledge graphs](https://www.sciencedirect.com/science/article/pii/S0957417418300897). G. Zhu, and C. Iglesias. Expert Syst. Appl. (2018)
- [Anaphora and coreference resolution: A review](https://www.sciencedirect.com/science/article/pii/S1566253519303677). Sukthanker, Rhea, et al.  Information Fusion 59 (2020): 139-162
- [Relation Extraction](https://arxiv.org/abs/1712.05191): A Survey, CoRR 2017. Sachin Pawar, Girish K. Palshikar and Pushpak Bhatacharyya.
- [How to train your dragon...I mean your entity linker, with Spacy](https://github.com/explosion/projects/tree/master/nel-wikipedia).
- [A survey on Open Information Extraction](https://www.aclweb.org/anthology/C18-1326.pdf), 2018.
 
# Language Models and Bert

- Sentence similarity (including question similarity) with [Bert as a service](https://github.com/hanxiao/bert-as-service)
- [SBert](https://github.com/UKPLab/sentence-transformers), aka Sentence embeddings.
- [Sentence similarity using SBert vs Bert](https://nadjet.github.io/blog/posts/sentence_similarity/).
- Jay Alammar’s Blog, [A visual guide to using Bert for the first time](http://jalammar.github.io/a-visual-guide-to-using-bert-for-the-first-time/). Check out his other visual blog posts: word embeddings, seq2seq, etc.
- [BERT Word Embeddings Tutorial](https://mccormickml.com/2019/05/14/BERT-word-embeddings-tutorial/), Chris McCormick, 2019.
- [BERT fine-tuning tutorial with Pytorch](https://mccormickml.com/2019/07/22/BERT-fine-tuning/), Chris McCormick, 2020.
 
 
# Catalan Language Processing

- [StanfordNLP - Catalan (Ancora)](https://stanfordnlp.github.io/stanfordnlp/models.html).
- [Stanza](https://stanfordnlp.github.io/stanza/): a wrapper that allows to use StanfordNLP models with Spacy.
- [FreeLing](http://nlp.lsi.upc.edu/freeling/node/1).
- [caWaC - Catalan Web Corpus](http://nlp.ffzg.hr/resources/corpora/cawac/).
- [Catalan model for Spacy](https://github.com/ccoreilly/spacy-catala).
- [CalBert](https://github.com/codegram/calbert): Catalan Albert.
 
# Question Answering (Q/A) systems in general

- [Automatic Question Answering: Problem Solved?](http://iberspeech2018.talp.cat/download/IberS18_KN3_Marquez.pdf), by Lluis Màrquez, 2018 talk. Good intro to general problem, with retrospective, achievements and challenges.
- [Question Answering](https://web.stanford.edu/~jurafsky/slp3/25.pdf), Chapter 25 of Jurafsky  and Martin’s book, “Speech and Language Processing”, 2019 edition.
- [Tutorial about Open Domain Q/A](https://github.com/danqi/acl2020-openqa-tutorial), 2020
- [Reading Wikipedia to Answer Open-Domain Questions](https://arxiv.org/pdf/1704.00051.pdf), 2017, and implementation in PyTorch, [DrQA](https://github.com/facebookresearch/DrQA)
- [List of Q/A Datasets](https://github.com/ad-freiburg/large-qa-datasets)
 
# Q/A From Knowledge Graphs

- [Q/A from knowledge base](https://www.aclweb.org/anthology/N18-2047.pdf), 2018
- [Introduction to Question Answering over Knowledge Graphs](https://yashuseth.blog/2019/10/08/introduction-question-answering-knowledge-graphs-kgqa/), Blog Post, 2019
- [Core techniques of question answering systems over knowledge bases: a survey](http://wdaqua.eu/assets/publications/2017_KAIS.pdf), 2017
- [QALD: Question Answering over Linked Data
Hybrid Question Answering System based on Natural Language Processing and SPARQL Query](http://qald.aksw.org/index.php?x=task1&q=3)
- [Improving Multi-hop Question Answering over Knowledge Graphs using Knowledge Base Embeddings](https://www.aclweb.org/anthology/2020.acl-main.412/), 2020.
 
# Q/A about COVID-19
 
- [EMNLP'2020 workshop on NLP and COVID](https://openreview.net/group?id=EMNLP/2020/Workshop/NLP-COVID). 
- [ACL'2020 workshop on NLP and COVID](https://yashuseth.blog/2019/10/08/introduction-question-answering-knowledge-graphs-kgqa/). 
- [COVID-Q/A Dataset](https://github.com/deepset-ai/COVID-QA)
- [How we created an open source covid 19 chatbot](https://towardsdatascience.com/how-we-created-an-open-source-covid-19-chatbot-c5c900b382df), Medium Article
- [Testing Bert-based question answering on Coronavirus articles](https://towardsdatascience.com/how-we-created-an-open-source-covid-19-chatbot-c5c900b382df), Medium Article
- [What are people asking about COVID 19: a new Question Classification dataset](https://towardsdatascience.com/what-are-people-asking-about-covid-19-a-new-question-classification-dataset-adcaeaddcce4)
- [COVID-Q Dataset](https://github.com/JerryWei03/COVID-Q)
- [Implement Question Answering System on Corona : Approach](https://medium.com/@aakashgoel12/question-answering-system-on-corona-approach-01-6ef9799695cb)
- [Real time disaster and monitoring tool using Wikipedia](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/44015.pdf). Thomas Steiner & Ruben Verborgh. 2015 AAAI Spring Symposium Series.   
 
# Open Q/A with SQuAD
- [SQuAD: The Stanford Question Answering Dataset](https://rajpurkar.github.io/SQuAD-explorer/explore/v2.0/dev/Southern_California.html).
- [Question Answering with SQuAD Kaggle starter pack](https://www.kaggle.com/jonathanbesomi/question-answering-starter-pack)
- [Question Answering on SQuAD](https://web.stanford.edu/class/cs224n/project/default-final-project-handout.pdf), university project assignment handout
- [Kaggle Tensorflow open Q/A Competition](https://www.kaggle.com/c/tensorflow2-question-answering)
- [Applying Bert to Question Answering with SQuAD](https://www.youtube.com/watch?v=l8ZYCvgGu0o)

# Natural Language Generation from Wikipedia Triples and texts

## General

- NLP with Deep Learning | Winter 2019 | Lecture 15 – Natural Language Generation: [video](https://www.youtube.com/watch?v=4uG1NMKNWCU) and [slides](http://web.stanford.edu/class/cs224n/slides/cs224n-2019-lecture15-nlg.pdf).
- ACL Conference 2019 [Tutorial on Storytelling from structured data and knowledge graphs](https://drive.google.com/file/d/1HaGCNc6n_sjyGLdaGzAVPvAeT0ZhhL3Q/view) (especially the introduction).
- [Seq2seq NLG: The Good, the Bad and the Boring](https://medium.com/analytics-vidhya/seq2seq-nlg-the-good-the-bad-and-the-ugly-8de0a05d9da1).
- [Survey of the State of the Art in Natural Language Generation: Core tasks, applications and evaluation](https://arxiv.org/abs/1703.09902), by Gatt & Krahmer, 2017.

## End-to-end Neural NLG
- Neural Wikipedian: Generating Textual Summaries from Knowledge Base Triples, 2018. [Code](https://github.com/pvougiou/Neural-Wikipedian) and [Article](https://www.sciencedirect.com/science/article/pii/S1570826818300313).
- Neural Text Generation from Structured Data with Application to the Biography Domain, 2016. [Dataset](https://github.com/DavidGrangier/wikipedia-biography-dataset) and [Article](https://arxiv.org/abs/1603.07771).
- Automatic Generation of Company Descriptions, 2018. [Dataset](https://gricad-gitlab.univ-grenoble-alpes.fr/getalp/wikipediacompanycorpus) and [Article](https://www.aclweb.org/anthology/W18-6532/).

## Datasets
- [T-Rex : A Large Scale Alignment of Natural Language with Knowledge Base Triples](https://github.com/hadyelsahar/RE-NLG-Dataset), 2018
- [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page): Automatic Alignment of Wikipedia articles with triples.
- WebNLG: a dataset of triples and Wikipedia texts. [Dataset](https://github.com/ThiagoCF05/webnlg) and [Article](https://www.aclweb.org/anthology/W18-6521.pdf).

## Evaluation
- [Best practices for the human evaluation of automatically generated text](https://www.inlg2019.com/assets/papers/98_Paper.pdf), INLG Conference 2019.
- [Evaluating the State-of-the-Art of End-to-End Natural Language Generation: The E2E NLG Challenge](https://www.sciencedirect.com/science/article/pii/S0885230819300919), 2020. In this paper, there are a lot of references of e2e systems that used the dataset of the challenge.
