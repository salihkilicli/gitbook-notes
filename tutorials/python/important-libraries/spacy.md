---
description: >-
  Some of the methods and objects used in SpaCy library (for NLP) will be
  covered here.
---

# SpaCy

## NLP using SpaCy

[SpaCy](https://spacy.io/) is the leading library for NLP,  and one of the most popular Python frameworks. Here I will mention some of the important methods used for Natural Language Processing using SpaCy.

First, we need to specify the model we are using \(simply the language\). Here is a small snippet of loading the "English" language model.

```python
import spacy

nlp = spacy.load('en')
```

After loading the model, we can process a text in English using `nlp` method.

```python
text = nlp('The quick brown fox jumps over the lazy dog.')
```

{% hint style="warning" %}
**Notice:** The sentence above actually uses every letter in the English alphabet at least once.
{% endhint %}

Now, let me introduce some of the most common lingos used in NLP.





