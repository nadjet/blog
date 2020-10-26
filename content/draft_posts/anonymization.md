---
title: "Anonymization"
date: 2020-02-28T12:15:07+01:00
tags: ["anonymization"]
draft: true
---

# Anonymization

## What is anonymization?

Anonymization means the processing of personal data in order to **irreversibly** prevent identification. If the personal information is recoverable, say because:

- it is held in a separate resource, or 
- the information hiding techniques employed make it recoverable, or 
- the data still contains information that makes the person identifiable or partially identifiable, or 
- the different bits of information can be cross-referenced within the dataset or across different datasets to infer the identity of the person. 

then it is not anonymization but pseudonymization.

So whilst pseudonymization somewhat reduces the linkability of the dataset to the identity of the data subject, it is not true anonymization. Achieving true anonymization is difficult even though it is a highly desirable feature since anonymized data do not fall under the European data protection law (i.e., General Data Protection Regulation or GDPR).

When performing anonymization, three criteria must be evaluated in order to evaluate its robustness:

1. Is it still possible to *single out* an individual? 

2. Is it still possible to link records relating to an individual? Indeed, it might be possible to combine different anonymized datasets to infer individuals identities from the information contained within them. So records within a dataset or across a dataset should not be even be *linkable* to a single individual.

3. Can information be *inferred* concerning an individual? For example, given the individuals gender, postcode and date of birth, the individual might become identifiable, if not singled out.

## Anonymization techniques

Anonymization techniques to prevent identification depend on the context and purposes of the processing. In addition, they may need to be combined to avoid the different pitfalls mentioned above, namely, singling out, linkability and inference.

The main anonymization techniques are randomization and generalization.

### Randomization

| technique      | definition                                                                                                      | example                                                                                                                                     | considerations                                                                                                                                                                                                                                |
|----------------|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| noise addition | modifying attributes in the dataset such that they are  less accurate whilst retaining the overall distribution | random modification of an individual's height between +/-10cm of their real height.                                                         | Must be combined with other techniques as not sufficient. Noise must be semantically viable, else an attacker will know that it is noise and discard it as information. If the data attributes are sparse, then de-anonymization is possible. |
| permutation    | shuffling the values of attributes so that they become  artificially linked to different data subjects.         | permuting job title together with salary (if only salary, then a CEO earning 5k and an unemployed  person earning 43k does not make sense). | Must be combined with other techniques as not sufficient. Logically or statistically correlated attributes should be permuted together so as no to break their relation  and make their identification possible by an attacker.               |
|                |                                                                                                                 |                                                                                                                                             |                                                                                                                                                                                                                                               |




##References

[Article 29, GDPR Working Party, 2014](https://aircloak.com/wp-content/uploads/WP29-Opinion-on-Anonymization.pdf)

[Custom NLP Approaches to Data Anonymization](https://towardsdatascience.com/nlp-approaches-to-data-anonymization-1fb5bde6b929), Practical ways for de-identifying real-world private data by Omri Mendels@Microsoft, Medium Article, January 2020.


