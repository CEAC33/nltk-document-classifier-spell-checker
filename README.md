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

<figure><code><b><sup>accessing-texts.py</sup></b></code>

```python
from nltk.book import *

#Access texts by calling out their names
print(text1)

# texts() function
print(texts())

# sents() function
print(sents(), end='\n\n\n')

# access sentences individually
print(sent1)
```
</figure>

### Basic Functions: concordance, similar, dispersion_plot, count

<figure><code><b><sup>basic-functions.py</sup></b></code>
  
```python
from nltk.book import *

# Text

nltk.text.Text

print(type(text2))
# Output: <class 'nltk.text.Text'>

print('\n\n\n')

# BASIC FUNCTIONS FOR SEARCHING TEXT

# concordance function  - inputs --> a single word to search
#                       - outputs--> every occurrence of the word together with some context

text1.concordance("man")

print('\n\n\n')

# similar function - inputs --> a single word to search
#                  - outputs--> all other words which appear in the context of the word provided in the input

text1.similar('woman')

print('\n\n\n')

# common_contexts function - inputs --> a list of words
#                          - outputs--> all the contexts shared by the list of words provided in the input together

text4.common_contexts(['bad','very'])

print('\n\n\n')

# dispersion plot - a graph of texts with the given list of words showing their positions in the text with their
#                   frequency graphically

text4.dispersion_plot(['citizen','democracy','freedom'])

# Counting words in the text

# function -- len()

print(len(text4))

print('\n\n\n')

# count the occurrence of a particular word in the text

print(text4.count('freedom'))

# we can calculate the percentage of a word occurring in the text

print(100 * (text4.count('freedom')/len(text4)))

print('\n\n\n')
```
</figure>

**Dispersion Plot**
![alt text](https://user-images.githubusercontent.com/51218415/73476468-e61b8380-4357-11ea-976a-e9c2db1c1010.png)

### Frequency Distribution with NLTK

<figure><code><b><sup>frequency-distributions.py</sup></b></code>

```python
from nltk.book import *


print('\n\n\n')
distribution_1 = FreqDist(text1)
print(distribution_1, end='\n\n')

words = distribution_1.keys()
print(type(words))
print(words)
words_list = list(words)
print(words_list[:10])

print(distribution_1['whale'])

# plot function

distribution_1.plot(50)
```
</figure>

**Frequency Distribution**
![alt text](
https://user-images.githubusercontent.com/51218415/73483135-92fbfd80-4364-11ea-820d-bbf2fc038fff.png
)

