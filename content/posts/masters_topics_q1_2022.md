---
title: "Data Science Projects (Q1-2022)"
date: 2021-07-29T14:18:55+01:00
draft: false
tags: ["master","argument mining","text mining", "wikipedia", "anonymization", "aircraft maintenance","telemedecine"]
---

This first quarter of the 2021-2022 academic year, I supervise 5 final year projects in the [Data Science Master](https://estudios.uoc.edu/es/masters-universitarios/data-science/presentacion) of the UOC University, three of which in "general" domains which are 1) [argument mining](#1-argument-mining), 2) [mining of encyclopedic knowledge from wikipedia](#2-wikipedia), 3) [text anonymization](#3-anonym), and two of which in applied domains that are 4) use of [NLP in an online medical consultation application](#4-medical), and 5) [detection of recurrent defects in aircraft safety reports](#5-defects). Below is a selection of the resources and references I give to the students ti get them started (sorry, the bibliographical citations are a bit sloppy).

<!--more--> 


# 1. <a name="1-argument-mining"></a>Argument Mining

[Argument mining resources page](https://github.com/raul23/argumentation-mining)

## 1.1. Tutorials and surveys

- [Argument Mining, A Survey](https://www.researchgate.net/publication/336351909_Argument_Mining_A_Survey), Lawrence and Reed, 2019. Computational Linguistics.
- [An insider’s guide to AI: Argument Mininghttps://www.contactengine.com/insights/an-insiders-guide-to-ai-argument-mining/), interview with Chris Reed (video)
- [Advances in Debating Technologies: Building AI That Can Debate Humans](https://www.youtube.com/watch?v=XZxJalCD-fI) (video based on IBM Debater Project, tutorial). ACL 2020
- [Five Years of Argument Mining: a Data-driven Analysis](https://www.ijcai.org/Proceedings/2018/0766.pdf), Cabrio and Villata, IJCAI 2018.
- Tutorial on [Advances in Argument Mining](https://aclanthology.org/P19-4008.pdf), ACL 2019. 

## 1.2. Papers

- Stance Classification of Context-Dependent Claims, Bar-Haim et al, 2017.
- Towards an Argument Mining Pipeline Transforming Texts to Argument Graphs, Lenz et al, 2020.

## 1.3. Datasets + tools/APIs

- [IBM Debater Datasets](https://www.research.ibm.com/haifa/dept/vst/debating_data.shtml)
- BBC Moral Maze: [here](https://www.bbc.co.uk/programmes/b006qk11/episodes/player) is the program's page and [here](https://figshare.com/articles/dataset/Moral_Maze_Transcripts/741242) are the program's transcripts. This is an interesting dataset, although to the best of my knowledge it has not been annotated.
- TARGER: open source argument miner, the [tool's page](http://ltdemos.informatik.uni-hamburg.de/targer/), the [github page](https://github.com/achernodub/targer) and :the paper: [TARGET: Neural Argument Mining at Your Fingertips, 2019](https://aclanthology.org/P19-3031v2.pdf).
- ArguminSci: [A Tool for Analyzing Argumentation and Rhetorical Aspects in Scientific Writing. Lauscher et al](https://d-nb.info/1193929318/34), and the [github page](https://github.com/anlausch/ArguminSci). 


# 2.  <a name="2-wikipedia"></a>Mining of Encyclopedic Knowledge from Wikipedia

The idea of this project is to perform extraction of encyclopedic knowledge from Wikipedia, in order to expand Wikipedia-based knowledge graph. Example encyclopedic knowledge include categorical information (e.g., "crew neckline" is a type of [neckline](https://en.wikipedia.org/wiki/Neckline) and is without specific article).



* [An open-source toolkit for mining Wikipedia](https://pdf.sciencedirectassets.com/271585/1-s2.0-S0004370212X00110/1-s2.0-S000437021200077X/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEEAaCXVzLWVhc3QtMSJGMEQCICO9XA0DA%2BHguNSQLl927NeNfjqTAhpAMZ8csr7hWjbhAiAVZq%2BjqiDkeJ4rcaMPoqB%2F0Zuj4oh4k1h7aJnnBiGgmir6AwgoEAQaDDA1OTAwMzU0Njg2NSIM7Dnowr336LNfUh1RKtcDkf7ZaqMkejfwgzcCS0OFoDlh3magHZjTBa7WqMPbCWGUuBOvEc67GRDXAu0dk8B6KSCrtn75wTh%2BZoEYlZaBp3XzR1T63PxW7nhrxK7Y4aqkqdftWzoIkA3neBDirBUG4KIsEXevbOkk%2FtFge2J6Gnl95GAo4oApMpNFdLJEUyKiHI0GDDWCqTJr78q0s%2F5gib7P3bJ98%2F40MqjVfMGtm7G2Xe%2BTQdrJ%2BAqrPbxLJp7ItI1ghVlVXjNFm4FFD8GMX%2BY1P670STDWv8mn73qVaTlKDoT5kwi3B4D%2F0r1W4j0xWIFFN6AazeB5s9BT4zAtRkUSzqS5hj2UxwO9I6ytlRnhFkVDvPqTrA6JWUlzvCdHYoSO85DaQ9hpo5Ji5j%2B90uF3Zg3lt5gFtCzKfglnGdPH42GT5f9S%2FDDuVeacbajzdETdC4Cw7Wk4100W4VtBaaSrvVvEjNuwzILWzcCjh60od7ctxjRVWNBrmiFLe4Wg39lFRUVxwyMkZYUCFa7DI9X3LFZy%2FBqPLrxDBu0nANcMuWnhnax%2Fj6O3xapVhfONJGRzmTn0%2BgnDF7BP1Kn8qFNyQz%2FW37srfJITcttHS3wyu5hUc26jEIILIz8L4VzUDoXV5SuMMIbjiocGOqYBMuYdxC%2B4xDFwyLqYGOItnMumLJhkCHUUrmNHzAxBBmLCJpQQtKKz8CNDHhPRKgAVbOUEcQmfYWT4ACSW1%2FLe7J2JWRwuT8PEdy9PDSKQuWmtGv%2BaCaVcadHQxCP4KBDBFHmz2ZKtJJUeFQJkhbRMrHG6bkaaDPzfwzIH%2BXNewkUJZmeW3UMzrWpG0XsXHq5C9twgm%2BTI3KTUcsLUryukV4KTsOnH0Q%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20210705T082221Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYR4UM7F5B%2F20210705%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=c113968fbe79c6f8b2044042497dfeef6b03e52ddf1bcd5641d8130414658d27&hash=cfe566ea28e0713caba0fbee0e490971ad73825734600169bb1abc1844591d31&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S000437021200077X&tid=spdf-d34d1a2e-f7fd-4802-897a-9fc561af5795&sid=4b4cf5f734da634b6f68ce577d049546f86egxrqb&type=client).  David Milne, Ian H. Witten, 2013.
* [Extracting RDF Relations from Wikipedia’s Tables](http://emunoz.org/wikitables/).Emir Muñoz. 2014.
* [Wikipedia Mining: Wikipedia as a Corpus for Knowledge Extraction](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.178.3046&rep=rep1&type=pdf). Kotaro Nakayama et al, 2008
* Language Models are Open Knowledge Graphs. 2020, [Medium article](https://towardsdatascience.com/language-models-are-open-knowledge-graphs-but-are-hard-to-mine-13e128f3d64d). 
* [T-REx: A Large Scale Alignment of Natural Language with Knowledge Base Triples](https://aclanthology.org/L18-1544.pdf).
* [Extracting RDF Relations from Wikipedia’s Tables](http://emunoz.org/wikitables/). Elsahar et al, 2018. In this work, the authors produce a large dataset of wikipedia abstracts aligned with triples. The goal to do so is to produce an align dataset for doing Natural Language Generation. The dataset is available [here](https://hadyelsahar.github.io/t-rex/).
* [Extracting Named Entities and Synonyms from Wikipedia for use in News Search. ](https://core.ac.uk/download/pdf/52104388.pdf)Christian Bøhn. Master project. 2010. A bit old but very relevant.
* [Entity Extraction from Wikipedia List Pages](https://link.springer.com/chapter/10.1007/978-3-030-49461-2_19).Nicolas Heist and Heiko Paulheim. ESWC 2020.
* [Building up Ontologies with Property Axioms from Wikipedia](http://ceur-ws.org/Vol-2293/paos2018-passcr2018_paper1.pdf), Kawakami et al. 2018
* [Expanding basic ontology from Wikipedia](https://decsai.ugr.es/pi/lidvis/IPMU2018SS/CastroEtAl.pdf), Castro et al.
* [Mining Domain-Specific Thesauri from Wikipedia: A Case Study.](https://ieeexplore.ieee.org/document/4061409) Milne et al. 2006 (rather old, but seems very relevant)
* [Automatic Creation of a Domain Specific Thesaurus Using Siamese Networks](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9364403), Dhaliwal et al. 2021. Related to Milne and Witten's article above, but more recent.
* [Entity Extraction from Wikipedia List Pages](https://link.springer.com/chapter/10.1007/978-3-030-49461-2_19), Heist and Paulheim. 2020
* [Machine Knowledge: Creation and Curation of Comprehensive Knowledge Bases](https://arxiv.org/pdf/2009.11564.pdf), Weikum et al. 2021. (book)
* This project also belongs to the field of “[Ontology Learning](https://en.wikipedia.org/wiki/Ontology_learning)” y also “[Automatic Taxonomy Construction](https://en.wikipedia.org/wiki/Automatic_taxonomy_construction)”: see for example “Codifying Collaborative Knowledge: Using Wikipedia as a Basis for Automated Ontology Learning”, Guo et al. (2009) 
* [Keyword Extraction](https://textminingonline.com/getting-started-with-keyword-extraction) (RAKE and KEA).  


# 3. <a name="3-anonym"></a>Text Anonymization



* [Anonymisation Models for Text Data: State of the art, Challenges and Future Directions](https://aclanthology.org/2021.acl-long.323.pdf),  Lison et al. ACL 2021.
* Microsoft's Presidio:
	* [https://towardsdatascience.com/nlp-approaches-to-data-anonymization-1fb5bde6b929](https://towardsdatascience.com/nlp-approaches-to-data-anonymization-1fb5bde6b929)
	* [https://presidio-demo.azurewebsites.net/](https://presidio-demo.azurewebsites.net/)
	* [https://github.com/microsoft/presidio](https://github.com/microsoft/presidio)
	* [https://github.com/microsoft/presidio-research](https://github.com/microsoft/presidio-research)

* [John Snow Labs approach](https://www.johnsnowlabs.com/simpler-more-accurate-deidentification-in-spark-nlp-for-healthcare/) to deidenficiation for healthcare using Spark NLP.
* [How to Build and Deploy a Document Anonymizer with Streamlit and SpaCy](https://www.youtube.com/watch?v=lCbG05lyDNk), 2021.
* A Python library to de-identify medical records with state-of-the-art NLP methods, called deidentify: [github page](https://github.com/nedap/deidentify) and [blog post](https://medium.com/nedap/de-identification-of-ehr-using-nlp-a270d40fc442).
* Blog post on data (not text) anonymization: [part 1]((https://medium.com/daimler-tss-tech/data-privacy-anonymization-and-pseudonymization-part-1-6b145459a3bf)) and [part 2](https://medium.com/daimler-tss-tech/data-privacy-anonymization-and-pseudonymization-part-2-2ee795a7cbda).
* Datasets: [texts from the european parliament](https://wt-public.emm4u.eu/Resources/DCEP-2013/DCEP-Download-Page.html), which contains names of places and people, although these are public texts.
* Medical texts that need de-identification, in [this portal]((https://portal.dbmi.hms.harvard.edu/projects/n2c2-nlp/)) you can access some datasets (probably need to register though).

 
# 4. <a name="4-medical"></a>Gathering Insights from Medical Conversations



* [Probing Patient Messages Enhanced by Natural Language Processing: A Top-Down Message Corpus Analysis](https://spj.sciencemag.org/journals/hds/2021/1504854/), Mastorakos et al. 2021
* Classifying patient portal messages using Convolutional Neural Networks, Sulieman et al, 2017. 
* [A comparison of rule-based and machine learning approaches for classifying patient portal messages, Cronin et al, 2017.](https://discovery.biblioteca.uoc.edu/discovery/fulldisplay?docid=cdi_scopus_primary_616938919&context=PC&vid=34CSUC_UOC:VU1&lang=ca&adaptor=Primo%20Central&tab=Everything&query=any%2Ccontains%2CClassifying%20patient%20portal%20messages&offset=0)** **Disponible Online desde la [Biblioteca](https://biblioteca.uoc.edu/es/index.html) de la UOC.
* [Using natural language processing and machine learning to classify health literacy from secure messages: The ECLIPPSE study,](https://www.biorxiv.org/content/10.1101/406876v1.full) 2018
* [Categorising patient concerns using natural language processing techniques](https://informatics.bmj.com/content/bmjhci/28/1/e100274.full.pdf), 2021
* Use of suggested messages for (human) chat operators: [A Framework to Assist Chat Operators of Mental Healthcare Service, 2020. Madeira et al.](https://aclanthology.org/2020.nlposs-1.1/)
* [Classifying Electronic Consults for Triage Status and Question Type](https://aclanthology.org/2020.nlpmc-1.1.pdf). Ding et al, 2020.
* [Summarizing Medical Conversations via Identifying Important Utterances](https://aclanthology.org/2020.coling-main.63.pdf). Song et al, COLING 2020. 


# 5. <a name="5-defects"></a>Identification of Recurrent Defects in Aircraft Maintenance Reports


## Ontologies/Taxonomies

* [ATA](http://www.s-techent.com/ATA100.htm)
* [Ontology-based modeling of aircraft to support maintenance management system](https://www.researchgate.net/publication/284901202_Ontology-based_modeling_of_aircraft_to_support_maintenance_management_system)

## Datasets

* MaintNet: the [resource page](https://people.rit.edu/fa3019/MaintNet/datasets.html) and [the 2020 paper by Akhbardeh et al.](MaintNet: A Collaborative Open-Source Library for Predictive Maintenance Language Resources).

## NLP for aircraft maintenance

   * [Natural Language Processing for aviation safety reports: from classification to interactive analysis](https://www.researchgate.net/publication/283846509_Natural_Language_Processing_for_aviation_safety_reports_from_classification_to_interactive_analysis), Computers in Industry 78, 2015
   
   * [Natural language processing of incident and accident reports : application to risk management in civil aviation](https://tel.archives-ouvertes.fr/tel-01230079/document), Nikola Tulechki, 2015
   
   * [FEATURE-TAK](https://www.dfki.de/fileadmin/user_upload/import/8636_ICCBR2016_paper_37_final.pdf) - Framework for Extraction, Analysis, and Transformation of Unstructured Textual Aircraft Knowledge, Reuss et al. 2016
   * [Applying NLP tools to occurrence reports](https://www.icao.int/safety/iStars/Documents/IUG%20Meeting%201/Presentations/Applying%20Natural%20Language%20Processing%20Tools%20to%20Occurrence%20Reports%20-%20Loren%20Groff.pdf) (presentation), Groff (National Transportation Safety Board), 2018.
   * [Natural Language Processing Based Method for Clustering and Analysis of Aviation Safety Narratives](https://www.mdpi.com/842166), Rose et al., 2020.
   * [Detection of Recurring Defects in Airline Incident Reports](http://rali.iro.umontreal.ca/rali/sites/default/files/publis/report-rali-sept-2020.pdf), Hermelo et al. 2020.
   * [Sequential Pattern Mining Algorithm Based on Text Data: Taking the Fault Text Records as an Example,](https://www.mdpi.com/2071-1050/10/11/4330) Yuan et al 2018
   * [Text Mining-based Research on Aircraft Faults Classification and Retrieval Model](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9153588), Yu et al, 2020. 