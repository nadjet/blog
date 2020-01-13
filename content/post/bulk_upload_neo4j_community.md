---
title: "How to bulk upload data into Neo4j Community Edition"
date: 2019-09-28T15:56:33+01:00
tags: ["how_to","knowledge_graphs","neo4j"]
draft: true
---

In this post, I explain how to upload concepts and relations into Neo4J Community Edition. <!--more-->

First you need to download and install Neo4J Community Edition.

In the configuration file `neo4j.conf` under neo4j's `conf` folder, you must ensure that the following line is commented out to allow files to be loaded from anywhere (not just from the neo4J import folder):

`dbms.directories.import=import`

You can start, stop and restart neo4j by running neo4j script under bin folder, respectively as follows: `neo4j start`, `neo4j stop`, and `neo4j restart`.

Next you can access the neo4j graph database in the browser as instructed.

You can upload relations and nodes from a comma separated csv. 

For example, the table below is a snapshot of a csv file containing 2 categories per row, where category1 is *broader than* category2.

	 	 	 	
| category1                                 | category1\_label                           | category2                       | category2\_label                 |
|-------------------------------------------|-------------------------------------------|---------------------------------|---------------------------------|
| Nuclear\_weapons\_testing\_by\_country       | Nuclear weapons testing by country        | Environmental\_issues\_by\_country | Environmental issues by country |
| Environmental\_issues\_in\_Laos              | Environmental issues in Laos              | Environmental\_issues\_by\_country | Environmental issues by country |
| Environmental\_issues\_in\_Madagascar        | Environmental issues in Madagascar        | Environmental\_issues\_by\_country | Environmental issues by country |
| Environmental\_issues\_in\_the\_United\_States | Environmental issues in the United States | Environmental\_issues\_by\_country | Environmental issues by country |
| Land\_surface\_effects\_on\_climate           | Land surface effects on climate           | Desertification                 | Desertification                 |
| Light\_pollution                           | Light pollution                           | Pollution                       | Pollution                       |


To create the broader edges and the category nodes if they do not exist in the graph database, we can execute the following Cypher query (assuming our csv’s full path is `/tmp/broaders.csv`):

```
USING PERIODIC COMMIT LOAD CSV WITH HEADERS FROM "file:/tmp/broaders.csv" AS row 
MERGE (cc1:Category {uri: row.category1,label: row.category1_label}) MERGE (cc2:Category {uri: row.category2,label: row.category2_label}) MERGE (cc1)-[:BROADER]->(cc2);
```

The MERGE keyword allows to match the specified nodes and relations, or to create them if they do not exist.

In the Neo4j browser page, you will see the Category nodes and BROADER relations created.
 

