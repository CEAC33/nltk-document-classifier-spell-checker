# nltk-document-classifier-spell-checker

## Getting started in NLTK

### Intro to NLP

Natural Language Processing (NLP) is the ability of a computer program to understand human speech as it is spoken.
NLP is a component of Artificial Intelligence (AI)

**Applications**

- Siri
- Cortana
- Google
- Alexa
- Spam Detection
- Chatbots
- Text Analytics

### Technical Requirements

- Python 3

```
pip3 install nltk
```

```
pip3 install matplotlib
```

<figure><code><b><sup>requirements.txt</sup></b></code><pre overflow: auto;><code>
nltk
matplotlib
numpy
</code></pre></figure>

### Installing and Setting Up NLTK

```
$ ipython

In [1]: import nltk

In [2]: nltk.download()
```

Collections > all > Download

### NLTK Accessing Texts

<figure><code><b><sup>accessing-texts.py</sup></b></code><pre lang="python"><code>
from nltk.book import *

#Access texts by calling out their names
print(text1)

# texts() function
print(texts())

# sents() function
print(sents(), end='\n\n\n')

# access sentences individually
print(sent1)
</code></pre></figure>

### Basic Functions: concordance, similar, dispersion_plot, count
