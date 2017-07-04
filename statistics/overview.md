# Overview

The corpus consists of 
* 24540015 tokens
* 1318860 sentences

All tokens have been automatically assigned a POS tag by the Mate tagger (accuracy 88%; the tagger guesses a POS tag even when the word form is not known)

15272085 tokens have a lemma: i.e., non empty ```<l/>```, with at least one ```<l1/>``` and/or at least one ```<l2/>```.

9267127 tokens have no lemmas: i.e., empty ```<l/>``` (803 should be added to this number, which are tokens that exceptionally do not have an ```<l/>``` element: they invariably show an erroneous form "#"). In the majority of cases, lemmas are missing because both Morpheus and PerseusUnderPhilologic do not contain the corresponding word forms. In a few cases, however, they contain the word form but its morphological analysis does not correspond to the one automatically assigned by the tagger (which is therefore to be considered, most likely, wrong):
* of the 9267127 tokens with missing lemmas 657627 are unique word forms (see values in ```<f/>```): Morpheus does not know 580415 of these unique forms, while PerseusUnderPhilologic 555970. 545011 word forms are missing both in Morpheus AND PerseusUnderPhilologic. As a consequence,
112616 (= 657627 - 545011) are unique word forms that are present in Morpheus and/or PerseusUnderPhilologic, but whose lemmas have not been retrieved because their morphological analyses differ from that assigned by the tagger.
