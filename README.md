# Political Messaging and Audience Engagement on Social Media

This project analyzes how different political messaging themes influence audience engagement on Facebook posts using reaction dynamics and topic modeling. The workflow combines exploratory analysis, time-series visualization of reactions, and LDA topic modeling to examine which themes are most associated with high engagement.

## Dataset availability

The dataset used in this analysis was provided for academic use and is therefore not included in this repository.

## Overview

### 1) Content types and posting behavior
- Distribution of status types (photo, status, link, video)

### 2) Temporal dynamics of engagement
- Time-series plots for likes, loves, sads, and angrys
- Interpretation of reaction patterns before and after early 2016 (when expanded reactions appear)

### 3) Topic modeling of political messaging (LDA)
- Text preprocessing (tokenization, stopword removal, lemmatization)
- TF-IDF vectorization
- LDA with 10 topics
- Topic interpretation with discussion of overlap and limitations

### 4) Linking topics to engagement
- Topics most associated with high-share posts (shares > median)
- Topics most associated with high-reaction posts (reactions > median)
- Comparison showing similar drivers for both amplification (shares) and engagement volume (reactions)

### 5) Sentiment note
- Reactions are discussed as a rough proxy for audience emotion, with caveats and a suggested next step for validation

## Key takeaways

Engagement is not evenly distributed across themes. Posts centered on campaign messaging, national identity, and political opponents consistently generate higher engagement in both shares and reactions.

Likes remain dominant throughout the dataset, but angry reactions show sharper spikes after early 2016, suggesting stronger emotional responses to certain posts.

Themes linked to high shares are largely the same as those linked to high reactions, indicating consistent drivers of amplification and engagement.

## Repository structure

    political-messaging-engagement/
    ├── notebooks/
    │   └── political_messaging_engagement.ipynb
    ├── data/
    │   └── README.md
    └── README.md

## How to run (locally)

### Install dependencies
- pandas
- matplotlib
- seaborn
- scikit-learn
- nltk

### Download required NLTK resources
- punkt
- stopwords
- wordnet

### Place the dataset in
- `data/Donald Trumps Facebook Statuses.csv`

### Open and run
- `notebooks/political_messaging_engagement.ipynb`

## Notes and limitations

- LDA can show topic overlap on entity-heavy political text.
- Reaction types approximate emotion but do not directly measure sentiment.
- Future work could combine topic modeling with sentiment analysis or contextual embeddings.
