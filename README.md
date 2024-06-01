# Overview
This project involves building a basic translation system using Python. The system translates sentences from English to Turkish or from Azerbaijani to Turkish using a combination of preprocessing techniques and machine translation models.

## Libraries Used
nltk: Natural Language Toolkit for text processing and NLP tasks.

numpy: For numerical operations, particularly used in the similarity calculation.

re: For regular expression operations to preprocess text.

sklearn: For vectorizing text data and calculating TF-IDF scores.

pydub: For handling audio file operations and performing audio manipulations.

```bash
import nltk
import numpy as np
import re

nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
nltk.download('wordnet')
```

## Part 1: Text Preprocessing
Define Regex Patterns for Contractions:

```python
replacement_patterns = [
    (r'won\'t', 'will not'),
    (r'can\'t', 'cannot'),
    # Additional patterns...
]
```

Function to Apply Regex Patterns:

```python
def apply_regex_patterns(text, replacement_patterns):
    for pattern, replacement in replacement_patterns:
        text = re.sub(pattern, replacement, text)
    return text
```

Read and Preprocess English-Turkish Corpus:

```python
with open("english_turkish_corpus_final.txt", "r", encoding="utf-8") as file:
    for line in file:
        line = line.strip()
        if line:
            english, turkish = line.split("*")
            # Further preprocessing steps...
```

Read and Preprocess Turkish-Azerbaijani Corpus:

```python
with open("turkish_azerbaijani_corpus_final.txt", "r", encoding="utf-8") as file:
    for line in file:
        line = line.strip()
        if line:
            turkish2, azerbaijani = line.split("*")
            # Further preprocessing steps...
```

## Part 2: Translation Process

Find Optimal Match for Translation:

```python
def find_optimal_match(input_sentence, src_sentences, target_sentences):
    # Use TF-IDF vectorizer to convert sentences to vectors...
    return optimal_sentences
```
-- Uses TF-IDF vectorization to find the most similar sentences in the corpus to the input sentence.

Convert Sentences to Aligned Sentences:

```python
def convert_to_aligned_sents(parallel_sentences):
    aligned_sents = []
    for initial_tokens, target_tokens in parallel_sentences:
        # Create aligned sentences...
    return aligned_sents
```
-- Converts the similar sentence pairs to aligned sentence objects for training the IBM Model.

Translate Sentence Using IBM Model 1:

```python
def remove_repeating_variables(array):
    unique_variables = []
    for item in array:
        if item not in unique_variables:
            unique_variables.append(item)
    return ' '.join(unique_variables)
```

Remove Repeating Variables:

```python
def remove_repeating_variables(array):
    unique_variables = []
    for item in array:
        if item not in unique_variables:
            unique_variables.append(item)
    return ' '.join(unique_variables)
```

# Conclusion
This project leverages machine learning and NLP techniques to create a basic translation system, showcasing how text preprocessing, vectorization, and model training can be combined to perform language translation.
