# Supplemental Material for IMLH 2021 Submission
This is a temporary location for hosting additional material during the double-blind review process of IMLH 2021. 

## Code 
A standalone script for our document perturbation method is provided in `input_perturbation.py` - it can perform token replacement using either an embedding matrix (e.g., for a HuggingFace Transformer model like our BigBird classifier) or a Gensim word2vec-style object containing word vectors. These techniques are used in the Jupyter notebook titled `metric-implementation-with-perturbation-anonymized.ipynb`, along with some EDA done during the development process. This notebook is where we implement a generalized local Lipschitz and calculate on a subset of documents, in addition to the same process for infidelity (via the Captum library).

## Supplemental Figures and Notes
### Dataset Statistics
We use the mortality prediction task introduced in van Aken et al. (2021) as the basis for our experiments in explainability. The following table provides descriptive statistics of the simulated admission notes forming this task dataset.

| Component | Value |
| ----- | ----- |
| # Training Observations   | 33,989 |
| # Validation Observations | 4,918 |
| # Test Observations       | 9,829 |
| Class Imbalance           | 10.52\% positive |
| Document Length (Average) | 396.6 words |
| Document Length (95th Percentile) | 809.0 words |
| Document Length (99th Percentile) | 1,054.2 words |
