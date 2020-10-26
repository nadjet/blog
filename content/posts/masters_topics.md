---
title: "My projects for Data Science Master Students"
date: 2020-01-10T11:24:13+01:00
tags: ["dbpedia","master"]
draft: false
---

Here are the projects I propose to [Data Science Master](https://estudios.uoc.edu/es/masters-universitarios/data-science/presentacion) students for their final project this semester. They range from text mining, concept mining, question answering to natural language generation. Most of them will be based on DBPedia/Wikipedia datasets.

<!--more-->

## Topic 1: Wikipedia Concept Mining and Geo-visualization

In this work, your goal is to develop an application that takes as input a Wikipedia category such as “Earthquake” or “Oil Spill”, extract all of the concepts associated with that category from DBPedia and geo-visualize them on a map. 

An example interactive map I developed can be found [here](https://nadjet.github.io/environmental_issues/). [This article](https://medium.com/@nadjetba/mining-and-visualizing-dbpedia-environmental-issues-6ecc31ce6a26) explains how it was done and how it can be improved. The objective of your thesis will be to generalize the approach and mine more specific concepts that are more amenable to a fully automated approach.

The resulting geo-visualization would be complementary to the ones provided here for instance:  

[https://ourworldindata.org/natural-disasters](https://ourworldindata.org/natural-disasters)

By working on this project you will learn about (1) knowledge graphs, (2) basic Natural Language Processing (NLP) techniques such as entity extraction and linking, and (3) data visualization.

## Topic 2: Simple Question Answering from Knowledge Graphs

In this work, your goal will be to develop a system that is able to answer simple questions in natural language by looking up properties in a knowledge graph. For example, the answer to the question “When was Mozart born?” can be found by looking up a simple fact which the “date of birth” property of the entity “Mozart”. This information can be found in a Knowledge Graph such as DBPedia which was derived from Wikipedia infoboxes.

To perform Simple QA from KGs, you need to understand what entities are involved and which property you are looking, and to link this information to entities and properties in the KG. So simple QA is normally broken down into 4 steps: 

1. Entity detection: finding entities in the question, such as “Mozart”,
2. Entity linking: linking in an unambiguous way the entities found in the question to the KG entities, e.g., linking “Mozart” to musician “Wolfgang Amadeus Mozart”, 
3. Relation prediction: identifying the relation in the query, such as “date of birth”, and
4. Evidence integration: selecting the best candidate triple, i.e., subject:“Wolfgang Amadeus Mozart”, predicate:“date of birth”, object:?Object, where? Object is the value to retrieve. 

By working on this project you will learn techniques and tasks for text mining and Natural Language Processing (NLP). You will get to implement classification models, to use a curated dataset ([SimpleQuestions](https://github.com/davidgolub/SimpleQA/tree/master/datasets/SimpleQuestions)) and perform evaluation.

## Topic 3: Building a Knowledge Graph about Olympic Medalists from Wikipedia Articles

Companies like Google enhance their search engine results with semantic information that constitutes what is known as the “Knowledge Graph”. In this work, your goal is to build a knowledge graph from information gathered on Olympic Medalists in their corresponding Wikipedia Articles.

Imagine you had to answer the question: “Please tell me what you know about X regarding the Olympic Games”. Your goal would then be to retrieve from the article about X information related to their participating in the Olympic Games: who, when, where, which, what and with whom.  You would need to identify relevant chunks of text, determine what information they convey, i.e., entities and relations between them (such as medal won on a specific year for a specific discipline) and link it to existing concepts. 

All these tasks require using text mining techniques such as entity identification, entity linking and relation extraction. Once you obtain the information, you could represent it as a knowledge graph. Then, depending on the scope of the project you could (1) answer questions such as “How many medals did X win” by mapping the Natural Language questions to, say SPARQL queries, or (2) develop a Natural Language Generation system using a sequence to sequence neural architecture and a dataset consisting of pairs of mined information about a given olympic medalist and the assembled texts snippets used for the mining of that information.

Please note that the Olympic Medalists domain is orientative. You could work on another restricted domain of your choice.

## Topic 4: Mining paragraphs about a given topic in Wikipedia

Your goal in this work is to extract paragraphs of text in Wikipedia articles about a particular topic. For example find in this article which paragraph/section, if any, is about the environment (i.e., section with heading “Relationship with the environment”). You can find this information by looking at section titles (like in the example above) or by doing topic modeling, or by finding links between the articles about the topic and other articles.

By working on this project, you will learn how to exploit different NLP and machine learning techniques to attain your goal. You will also learn how to exploit Wikipedia as a text dataset and its knowledge graph as an additional information source (e.g., to get the links between the articles).

You can do this project on the Wikipedia for the language of your choice (Catalan, Spanish, English, etc).

## Topic 5: Building an ontology about Earrings and an Automatic Earrings Description Generation System

I have this dataset of a few thousand earring product descriptions in English such as:


>These classy diamond stud earrings are an essential accessory that can be worn everyday as well as on special occasions, with almost anything. It will be a favorite in any woman s collection. Elegantly set in a 14k white gold 4 prong basket setting these studs makes it a perfect gift for someone you love."

Your goal will be (1) to build an ontology for earrings (type, material, shape, color, brand, size, etc), (2) to automatically extract product features for each text, (3) and to build a natural language generation system, which, given a dataset of input attribute-values and output texts, can generate naturally sounding texts that preserve the input specification. 

By working on this project, you will learn about ontologies and knowledge representation, dataset preparation and end-to-end  Natural Language Generation (NLG) techniques. See [this](https://medium.com/analytics-vidhya/seq2seq-nlg-the-good-the-bad-and-the-ugly-8de0a05d9da1) medium article where I describe how to perform e2e NLG of restaurant descriptions.

To do this project, it is best if you have some previous knowledge of deep learning.
