---
title: "How to install DBPedia Spotlight Locally"
date: 2019-09-21T06:24:17+01:00
tags: ["how_to","knowledge_graphs","dbpedia"]
draft: false
---

In this post I explain how to install on [DBPedia Spotlight](https://www.dbpedia-spotlight.org/) on your local computer. DBPedia Spotlight is a tool that annotates mentions of DBPedia concepts in text. It is not in active development but can still be useful for Proof-of-Concept Demonstrators. <!--more-->

Download the jar from [here](https://sourceforge.net/projects/dbpedia-spotlight/files/spotlight/) and the English model from [here](https://sourceforge.net/projects/dbpedia-spotlight/files/2016-10/en/model/).

Untar the English model: `tar xzf en.tar.gz`

Run with Java 1.8 with enough RAM, by typing in the following command:

```
java -Xms8g -jar dbpedia-spotlight-nightly-build.jar /path/to/model/en http://localhost:2222/rest
```

(assuming you downloaded a jar of that name)

You will get a message that says:

```
  Server started in /execution/path listening on http://localhost:2222/rest
```

Now you can call DBPedia Spotlight locally, for example:

```
curl http://localhost:2222/rest/candidates --data-urlencode "text=The president of United States" --data "confidence=0"  --data "support=0"
```

