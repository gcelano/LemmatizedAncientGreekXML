# LemmatizedAncientGreekXML

This repository contains Ancient Greek texts which have been tokenized, POS-tagged, sentence-splitted, and lemmatized automatically. The texts come from the following repositories, which currently contain most of the Ancient Greek texts freely accessible over the internet:

1. https://github.com/PerseusDL/canonical-greekLit/releases/tag/0.0.4
2. https://github.com/OpenGreekAndLatin/First1KGreek/releases/tag/v1.1

As for the tokenization, POS tagging and sentence splitting, the data rely on those provided in:

1. https://github.com/gcelano/CTSAncientGreekXML
2. https://github.com/gcelano/POStaggedAncientGreekXML

Refer to these repositories for further documentation. In the present repository, the POS tag + the word form of a token have been automatically linked to those contained in Morpheus and MorpheusUnderPhilologic. Since the latter databases also contain lemmata, this allowed their automatic extraction.

The XML structure of each file is self explanatory and meaning of abbreviations are explained at the beginning of each file. For convenience I give an example here:




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



