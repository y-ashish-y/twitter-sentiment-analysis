# Twitter Sentiment Analysis

A three-stage pipeline that collects tweets for a keyword, cleans the raw data, and runs text analysis on the result: word clouds, an inverted index, and sentiment distribution by place.

## Pipeline

| Stage | What it does | Output |
|---|---|---|
| 1. Collect | Search recent tweets for a keyword (e.g. `covid19`) | Raw tweets as JSON, one per line, in `extracted/` |
| 2. Cleanse | Parse and clean the raw tweets | Processed JSON, one per line, in `cleansed/` |
| 3. Analyze | Word counts and word cloud, inverted index for hashtags, mentions and words, sentiment analysis (VADER and TextBlob) by place | `wordcounts/` and plots |

## Contents

| File | Description |
|---|---|
| `Twitter_assignment.ipynb` | Full pipeline notebook, runnable on Google Colab |
| `extracted/`, `cleansed/`, `wordcounts/` | Sample outputs from earlier runs |

## Run

Requires Twitter/X API credentials. **Do not commit them.** Set them in the notebook's environment, or read them from environment variables, before running Stage 1.

```bash
pip install tweepy pandas matplotlib wordcloud nltk gensim spacy textblob vaderSentiment
python -m spacy download en_core_web_sm
```
