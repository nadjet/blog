---
title: "Uploading pre-existing datasets in Neo4j: lessons learnt"
date: 2020-03-19T15:56:33+01:00
tags: ["cypher","neo4j"]
draft: false
---

Recently I developed a proof-of-concept to model and query data with Neo4J starting from a pre-existing dataset. I also performed a training session for loading and querying a Neo4j graph database from a pre-existing "toy" dataset. Here is what I learnt from those exercises.  <!--more-->

The POC did not have too much data (+100k concepts and +200k relations) but the modelling requirements were quite complex: duplicate nodes were allowed and so I could not rely on uniqueness constraints to constrain the data.  I ended up creating the graph with relatively complex queries and I wrote some code to sanity check the results, ensuring that the count of nodes and relations created was correct.

After succeding in creating and validating the graph, I realized that I could have saved myself writing such complex queries if I had preprocessed the csv dataset to make it explicit what nodes and relations to create **within** the csv **before** loading the data. 

The toy dataset was about athletes participations to sports events at olympic games between 1896 and 2016. Its queries and dataset can be found in [this](https://github.com/nadjet/neo4j_example) Github repository. The resulting graph was around 400k nodes and +1 million relations.

The database modelled Athlete, Game, Event, Sport, Team, Medal and Participation as nodes. This latter, Participation, is what would be a foreign key table in a relational database, aka, a node to link an athlete's participation to an event on a team at a game with an optional medal. Each node corresponds to a row in the csv. 

Again, it was easier to add an id for the row in the csv since uniqueness constraint on multiple properties [does not seem to be possible](https://stackoverflow.com/questions/22498054/how-to-create-unique-constraint-involving-multiple-properties-in-neo4j) in the Neo4j community edition.



