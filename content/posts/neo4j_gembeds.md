---
title: "Node similarity with graph embeddings using Node2Vec"
date: 2020-03-22T13:33:00+01:00
tags: ["neo4j","node2vec"]
draft: false
---

I computed graph embeddings on Athletes in a graph modelling [Olympic Games](https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results) in [Neo4j](https://neo4j.com/). I was then able to compute the most similar Athletes to any given Athlete using [Node2Vec](https://github.com/VHRanger/nodevectors). I could then visually appreciate this similarity by looking at the corresponding subgraph subsuming the related nodes and their edges.  <!--more-->

The repository with the code and the example subgraphs can be found [here](https://github.com/nadjet/gembeds_neo4j).

An interesting future application to accompany this analysis would be to verbalize nodes similarities and differences with a template-based Natural Language Generation system.