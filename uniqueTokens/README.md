# Unique Values

This directory contains a database of all the unique tokens found in

* https://github.com/gcelano/LemmatizedAncientGreekXML/tree/master/texts

A token is considered unique in its combination of word form AND POS tag (see @v in each <d/> element). 
These unique values have been used to merge Morpheus and PerseusUnderPhilologic databases in order to retrieve lemmas from these latter
(which appear in <e/> and <l/> elements for Morpheus and PerseusUnderPhilologic lemmas respectively). PerseusUnderPhilologic lemmas also show the original POS tag in @r, in that this database presents a POS tag which is slightly different from the Morpheus one (in second position it adds one more value, thus resulting in a 10 character string).

