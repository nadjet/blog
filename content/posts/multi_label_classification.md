---
title: "Multi-label classification"
date: 2019-04-05T18:07:41+01:00
tags: ["deep_learning","fastai"]
draft: false
---

I have trained a classifier with fine tuned embedding language model that assigns content labels to basic restaurant descriptions using the [fastai](https://www.fast.ai/) library. 
<!--more-->

So you have a text like:

```
The three star coffee shop, The Eagle, gives families a mid-priced dining experience featuring a variety of wines and cheeses. Find The Eagle near Burger King.
```

And the output are the following labels:

```
eatType[coffee shop],
food[French],
priceRange[moderate],
customerRating[3/5],
kidsFriendly[yes]
```

This is the dataset used for the e2e Natural Language Challenge which consists of 50k <text,content labels> pairs. 

It achieves an F-score of 92% for individual labels thanks to the gradual unfreezing of the layers.

You can find out more in my kaggle kernel [here](https://www.kaggle.com/nadjetba/text-to-meaning-with-multi-label-classification).
