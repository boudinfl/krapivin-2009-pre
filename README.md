# Preprocessed Krapivin keyphrase extraction benchmark dataset

This dataset was introduced in:

 - **Large dataset for keyphrases extraction.**
   Krapivin, M., Autaeu, A., & Marchese, M. (2009). 
   *University of Trento.*

The dataset is split into three directories:

  * `references`: reference keyphrases for evaluation
  * `test`: test set
  * `src`: scripts and archive from which the dataset is built

Each input file is processed using the Stanford CoreNLP suite v3.6.0.
We use the default parameters and perform tokenization, sentence splitting and
Part-Of-Speech (POS) tagging. Files are in XML format.

Reference keyphrases are in json format and named according to the following
rules:

    test.author.[stem]?.json

Stemming (if applied), is performed with nltk Porter algorithm (English).

Below is a toy example of reference file:

    {
        "doc-1": [
            [
                "target detect"
            ],
            [
                "number of sensor",
                "sensor number"
            ]
        ],
        ...
    }