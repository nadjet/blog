---
title: "Sentence similarity with Bert vs SBert"

date: 2020-10-22T21:48:00+01:00

tags: ["bert", "similarity"]

draft: false
---

We can compute the similarity between two sentences by calculating the similarity between their embeddings. 

A popular approach is to perform the mean or max averaging of the sentence word embeddings. 

Another approach, which is faster and more performant, is to use SBert models. <!--more-->

In this [repository](https://github.com/nadjet/sentence_similarity), I present some code I wrote to compute sentence similarity using both approaches, for comparison.

More similar sentences were found using SBert, which was also faster by threefold with my small dataset of 600+ sentences and 10 queries.

For more explanation, there is a detailed [readme](https://github.com/nadjet/sentence_similarity/blob/master/README.md).

