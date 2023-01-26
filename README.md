## NLP SpaCy Test

#### This is a test of using Python + SpaCy to create summaries of web articles.

### Installation Instructions

```
pip install -r requirements.txt
```

### Useful links

[SpaCy](https://spacy.io/)
[ActiveState - How To Do Text Summarization with Deep Learning and Python](https://www.activestate.com/blog/how-to-do-text-summarization-with-python/)

### Results

-   SpaCy produces summaries by reusing existing sentences - this can result in grammatically poor and confusing summaries.

-   The word frequency model brings out the general key points of an article, but more testing is required to check how it handles scientific literature and regulatory documentation.

-   In particular regulatory documentation would be expected to cause problems because it predominantly consists of labeled data rather than prose.

-   The multilanguage support of spaCy may prove useful for a analysing documentation belonging to a global organisation.

-   Setup and implementation was very simple and would accelerate things for the proof of concept stage.

-   The SpaCy pipeline can by customised - there is a relatively significant component library that uses spaCy in numerous contexts including in the processing of clinical notes, and [biomedical documents](https://spacy.io/universe/project/scispacy). These components could be combined in the pipeline (maybe???), and suggests it would be quite easy to add our own custom component(s).

-   Different spaCy pipelines could be feasibly be triggered on the basis of ML-based document categorisation.

#### Differences between small and large models

-   There was some improvement in one of three of the output summaries when using the `en_core_web_lg` model.

-   The large model is 79 times larger than the small model, for potentially limited gain.

-   Accuracy of predictions does not differ significantly between large and small models (per the spaCy docs):

```
    LAS: 90.07% vs 89.66%
    POS: 96.98% vs 96.78%
    UAS: 91.83% vs 91.53%
    NER F-score: 86.62% vs 85.86%
    NER precision: 87.03% vs 86.33%
    NER recall: 86.20% vs 85.39%

```
