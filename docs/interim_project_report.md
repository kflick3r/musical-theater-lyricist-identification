# Interim Project Report
**Project:** Musical Theatre Lyricist Identification Using NLP

### 1. Project Summary

For my final project, I am exploring whether NLP techniques can identify who wrote a musical theatre song based on its lyrics. The study focuses on four lyricists: Stephen Sondheim, Stephen Schwartz, Jason Robert Brown, and Oscar Hammerstein II.

The main goal is to compare a traditional word-level TF-IDF model with a model using pretrained Transformer embeddings. I am also interested in whether these models learn characteristics of a lyricist's writing style or rely on vocabulary and themes specific to individual musicals.

### 2. Data

I am building a dataset of musical theatre song lyrics, organized by lyricist, musical, and individual song. The current target is six musicals per lyricist, allowing four musicals to be used for training and two to be held out for testing.

I have been collecting lyrics primarily from [AllMusicals](https://www.allmusicals.com/) and [Genius](https://genius.com/). So far, I've focused on collecting and cleaning lyrics from Jason Robert Brown's musicals. I've collected 58 songs containing approximately 19,000 words.

This has involved manually reviewing lyrics against recordings, removing spoken dialogue, character labels, and stage directions while preserving sung repetitions. Since I am creating my dataset from scratch rather than using an existing one, data collection and preprocessing have taken a significant amount of time.

### 3. Approach

I plan to compare two classification approaches:

1. **TF-IDF + Logistic Regression:** Represent each song using word-level TF-IDF features and train a classifier to predict its lyricist.
2. **Pretrained Transformer Embeddings + Logistic Regression:** Generate fixed contextual representations of each song using a pretrained Transformer model and train a classifier using those representations.

I plan to use Python and scikit-learn for TF-IDF vectorization, Logistic Regression, and evaluation, along with Hugging Face Transformers for generating pretrained embeddings.

Both approaches will be evaluated using accuracy, precision, recall, F1-score, and confusion matrices.

I also plan to compare random song-level train/test splits with held-out-musical evaluation. This will help determine whether the models generalize to songs from musicals they have not encountered during training.

### 4. Progress So Far

Most of my work so far has focused on data collection and preprocessing. I've established a process for reviewing individual songs, checking lyrics for accuracy, and excluding tracks that aren't appropriate for lyricist attribution. I've also started looking at song lengths and word counts to get a better understanding of the data.

One challenge has been determining how to handle songs containing very little lyrical material. Several songs in *Parade* contain fewer than 100 words, which may make authorship identification more difficult. For now, I've decided to keep four particularly short songs until I have a better idea of how they might affect the models.

Another consideration is repeated lyrical material across songs within the same musical. Repeated lyrics may provide meaningful stylistic information, but they could also lead to overly optimistic results if similar songs from the same musical appear in both training and testing data.

I have not yet begun classification experiments, as my initial priority has been developing a consistent dataset and preprocessing workflow.

### 5. Next Steps

Over the next two weeks, I plan to continue collecting lyrics for additional musicals and lyricists. I also hope to begin implementing the TF-IDF baseline once I have enough data for some preliminary experiments.

I expect that collecting enough lyrics while keeping the data accurate and consistent will continue to be my biggest challenge.

### 6. Questions or Concerns

My main concern at the moment is collecting enough data to train the models effectively. Since I am building the dataset from scratch, I want to spend sufficient time verifying the lyrics and ensuring the data is accurate and consistent. However, I am also concerned about balancing data quality with the amount of data needed for meaningful classification results.

Given the number of songs available per lyricist, do you think my planned dataset will be sufficient for comparing these two approaches, or should I consider adjusting the scope of the project?