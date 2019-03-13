# Distinct-N
Distinct-N, most notably distinct-1 and distinct-2, is metric that measures the
diversity of a sentence. It focuses on the number of *distinct* n-gram of a sentence and thus
penalizes sentences with lots of repeated words. The metric is free of any *reference* or *ground truth*
sentence and devotes totally to the property of a sentence (generated by the system).
It is proposed by Jiwei Li et.al in the paper *A Diversity-Promoting Objective Function for Neural Conversation Models.pdf*.

# Definitions
The original paper coined *Distinct-N* as:

    We report degree of diversity by calculating the number of distinct unigrams and bigrams in generated responses.
    The value is scaled by total number of generated tokens to avoid favoring long sentences
    
which is exactly what we have mentioned before.

# Usage
```bash
$ python distinct_metric.py -n N_NGRAMS PREDICTION
```


where `N_GRAMS` is the length of token sequence to count as unique within one sentence.
`PREDICTION` is the prediction or response your model generates with one utterance (sentence) per line.


# Dependencies
It only depends on `numpy==1.13.1`.