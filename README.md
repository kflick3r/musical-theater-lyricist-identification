# Identifying Musical Theater Lyricists Using NLP and Stylometry

My NLP final project exploring whether text classifiers can identify musical theater lyricists based on their song lyrics and generalize to songs from musicals not included in training.

## Research Questions

1. How does TF-IDF with Logistic Regression compare to pretrained Transformer embeddings with Logistic Regression?
2. Can the models recognize a lyricist's writing style across different musicals, or are they mostly learning vocabulary and themes from specific shows?

## Lyricists

- Oscar Hammerstein II
- Stephen Sondheim
- Stephen Schwartz
- Jason Robert Brown

## Planned Approaches

- **Model 1:** TF-IDF + Logistic Regression
- **Model 2:** Pretrained Transformer embeddings + Logistic Regression
- **Optional:** Fine-tune a pretrained Transformer model, such as BERT, if time and data allow.

## Planned Evaluation

Compare accuracy, precision, recall, F1-scores, and confusion matrices using two testing approaches:

- **Random song-level split:** Randomly divide songs into training and testing sets.
- **Held-out-musical split:** Test on songs from musicals not included in training.

I'll also examine which lyricists the models confuse most often and possible reasons for those mistakes.

## Repository Layout

- `docs/`: Project proposal and reports
- `data/`: Dataset documentation
- `notebooks/`: Data exploration and experiments
- `src/`: Python scripts
- `results/`: Model evaluation results

## Project Status

Project proposal completed. Next steps include finding suitable lyric datasets, verifying lyricist credits, and preparing the data for classification.