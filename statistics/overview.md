# Overview

The corpus consists of 
* 25750588 tokens
* 1384550 sentences

All tokens have been automatically assigned a POS tag by the Mate tagger (accuracy 88%; the tagger guesses a POS tag even when the word form is not known)

16002732 tokens have a lemma: i.e., non empty ```<l/>```, with at least one ```<l1/>``` and/or at least one ```<l2/>```.

9747856 tokens have no lemmas: i.e., empty ```<l/>```. In the majority of cases, lemmas are missing because both Morpheus and PerseusUnderPhilologic do not contain the corresponding word forms. In a few cases, however, they contain the word form but its morphological analysis does not correspond to the one automatically assigned by the tagger (which is therefore to be considered, most likely, wrong).
