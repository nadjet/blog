---
title: "Seq2seq Natural Language Generation"
date: 2019-12-31T14:33:22+01:00
tags: ["NLG","deep_learning","fastai"]
draft: true
---

I implemented a seq2seq Natural Language Generator using the [fastai](https://www.fast.ai/) library and the [2017 e2e NLG challenge](http://www.macs.hw.ac.uk/InteractionLab/E2E/) [dataset](https://github.com/tuetschek/e2e-dataset).
<!--more-->

The code can be found [here](https://github.com/nadjet/e2e_nlg) and a detailed article on medium [here](https://medium.com/analytics-vidhya/seq2seq-nlg-the-good-the-bad-and-the-ugly-8de0a05d9da1).

To summarize, on the plus side, I was able to generate reasonably sounding short texts that verbalize most of the input using a sequential model without any of the usual NLG paraphernalia (ordering, sentence planning, lexicalization, linguistic realization, etc). 

On the downside, the resulting texts were linguistically not very varied, which is a known limitation of these types of models. 

Also, I did not find that attention improved the results compared with vanilla seq2seq. And, whilst data augmentation improved the test set results on bleu metric, neural sampling based beam search with reranking did not.
