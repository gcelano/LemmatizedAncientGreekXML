# Lemmatized Ancient Greek Texts 1.2.1

This repository contains Ancient Greek texts which have been tokenized, POS-tagged, sentence-splitted, and lemmatized automatically. The texts come from the following repositories, which currently contain most of the Ancient Greek texts freely accessible over the internet:

1. https://github.com/PerseusDL/canonical-greekLit/releases/tag/0.0.236
2. https://github.com/OpenGreekAndLatin/First1KGreek/releases/tag/1.1.1802

As for the tokenization, POS tagging and sentence splitting, the data rely on those provided in:

1. https://github.com/gcelano/POStaggedAncientGreekXML/releases/tag/v1.2.0

Refer to these repositories for further documentation. In the present repository, the POS tag + the word form of a token have been automatically linked to those contained in Morpheus and MorpheusUnderPhilologic. Since the latter databases also contain lemmata, this allowed their automatic extraction.

The XML structure of each file is self-explanatory and solutions of abbreviations are provided at the beginning of each file. For convenience I give an example here:

```xml
  <s n="2">
    <t p="4" n="1" a="[1]" o="p-s---mn-" u="1">
      <f>ὃς</f>
      <l i="234">
        <l1 o="pr-s---mn-">ὅς</l1>
      </l>
    </t>
    <t p="4" n="2" a="[1]" o="p-p---fa-" u="2">
      <f>τάσδε</f>
      <l i="5901">
        <l1 o="pd-p---fa-">ὅδε</l1>
        <l2>ὅδε</l2>
      </l>
    </t>
   
    <!-- further t elements -->
   
   </s>
```
Read the above xml fragment this way:

* ```s``` element: sentence element, where ```@n``` is the sentence number
* ```t``` element: token element, which contains a number of values providing its morphological analysis:
  * ```@p```: passage-level cts urn
  * ```@n```: position of the token in ```@p```
  * ```@a```: nth occurrence of that token in ```@p```
  * ```@o```: morphological analysis of the token as provided automatically by the Mate tagger (this analysis follows the Morpheus format)
  * ```@u```: position of the token within the s(entence) element
  * ```f``` element: the <mark>word form</mark> of the token
  * ```l``` element: possible lemmata extracted from Morpheus (```<l2/>```) and PerseusUnderPhilologic (```<l1/>```) found by matching their word forms ```AND``` POS tags with those found in the present database. in ```<l1/>``` ```@o``` contains the original PerseusUnderPhilologic POS tag, which can be more informative than the Morpheus one. For example, ὃς in the above example is analyzed in PerseusUnderPhilologic as a relative provoun (```o="pr-s---mn-"```: see "r" in second position). Similarly, ὅδε is analyzed as a demonstative pronoun, while Morpheus simply treats it as a pronoun. One token may have more than one  ```<l1/>``` and/or ```<l2/>``` elements associated.

Meaning of abbreviations in t/@o (this value is the one used in Morpheus):

* 1:  part of speech
  * ```n```: noun
  * ```v```: verb
  * ```t```: participle
  * ```a```: adjective
  * ```d```: adverb
  * ```l```: article
  * ```g```: particle
  * ```c```: conjunction
  * ```r```: preposition
  * ```p```: pronoun
  * ```m```: numeral
  * ```i```: interjection
  * ```e```: exclamation
  * ```u```: punctuation

2: person
  * ```1```: first person
  * ```2```: second person
  * ```3```: third person

* 3: number
  * ```s```: singular
  * ```p```: plural
  * ```d```: dual

* 4: tense
  * ```p```: present
  * ```i```: imperfect
  * ```r```: perfect
  * ```l```: pluperfect
  * ```t```: future perfect
  * ```f```: future
  * ```a```: aorist

* 5: mood
  * ```i```: indicative
  * ```s```: subjunctive
  * ```o```: optative
  * ```n```: infinitive
  * ```m```: imperative
  * ```p```: participle

* 6: voice
  * ```a```: active
  * ```p```: passive
  * ```m```: middle
  * ```e```: medio-passive

* 7: gender
  * ```m```: masculine
  * ```f```: feminine
  * ```n```: neuter

* 8: case
  * ```n```: nominative
  * ```g```: genitive
  * ```d```: dative
  * ```a```: accusative
  * ```v```: vocative
  * ```l```: locative

* 9: degree
  * ```c```: comparative
  * ```s```: superlative

The meaning of abbreviations in t/l/l1/@o (used in MorpheusUnderPhilologic) is the same as that in Morpheus (see above) except for the first two
characters. Read them like this:

* ```ae```: proper adjective (e.g., Ἀθηναῖος). 
* ```ne```: proper noun (eg., Ζεύς)
* ```d-```: adverb" (eg., οὐ)
* ```dd```: demonstrative adverb (eg., ταύτῃ)
* ```de```: proper name adverb (eg., Ἀθήναζε)
* ```di```: interrogative adverb (eg., ποῦ)
* ```dr```: relative adverb (eg., οἷ)
* ```dx```: indefinite adverb (eg., που)
* ```c-```: conjunction (eg., καί)
* ```r-```: preposition 
* ```p-```: pronoun
* ```pa```: definite article
* ```pc```: reciprocal pronoun (eg., ἀλλήλους)
* ```pd```: demonstrative pronoun (eg., οὗτος)
* ```pi```: interrogative pronoun (eg., τίς)
* ```pk```: reflexive pronoun (eg., σεαυτόν)
* ```pp```: personal pronoun (eg., με)
* ```pr```: relative pronoun (eg., ὅς) 
* ```ps```: possessive pronoun (eg., ἐμός)
* ```px```: indefinite pronoun (eg., τις)
* ```m-```: numeral
* ```i-```: interjection (eg., ὀτοτοί)
* ```e```: exclamation
* ```y```: math term or abbrev for all of Euclid's ΑΒΓ geometrical figures
* ```g-```: particle
* ```gm```: modal particle" (eg., κε)

# Changelog

In  the present version (1.2.1): 

* lemmas are corrected: if a Morpheus lemma (<l2/>) is the same as a MorpheusUnderPhilologic lemma (<l1/>), it is deleted.
* documentation is improved: meaning of abbreviations in @o published

# License
<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.



