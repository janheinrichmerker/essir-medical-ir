# Notes

Important things to consider:
- location
- maybe time of the study / patient
- Stemming?
- What’s considered as stopwords ? (some columns contain ‘\n’ ‘\r’ symbols for example, are they included in stopwords?)


Ideas for our pipeline:
- re-formulate query based on relevant docs.
- candidate retrieval: BM25
- re-ranking with neural models: monoBERT or monoT5?
- classification: distinguish eligible from non-eligible studies

- 2 stages:
  - candidate retrieval:
    - BM25
    - disable stemming?
  - re-ranking with neural models:
    - monoBERT or monoT5?
- 2 pipelines:
  - then rank-fuse in the end: RRF
  - Relevance-oriented
    - don’t yet distinguish eligibility, only care about relevance
  - Eligibility oriented
    - mapping all labels ‘relevant’ / “highly relevant” to just “relevant”
    - Train a classifier:
      - train/test split over the 2021 version of the TRECclinical trial from last year (https://ir-datasets.com/clinicaltrials.html#clinicaltrials/2021/trec-ct-2021)
      - Try to train a SVM(???) and see if the classification score can be used as additional signal
