# YouTube NLP Analysis Project

**Linguistic, Thematic, and Sentiment Analysis of Titles of Popular YouTube Videos in Kazakhstan Using NLP**

## Project Description

This project analyzes popular YouTube video titles using Natural Language Processing (NLP). The main focus is on linguistic, thematic, and sentiment patterns in YouTube content related to Kazakhstan.

The project uses the YouTube Data API v3 to collect video metadata, including video titles, categories, publication dates, regions, view counts, like counts, and comment counts. The collected data is processed using Python, and several NLP methods are applied, including language detection, sentiment analysis, rule-based content classification, word cloud visualization, and topic modeling.

The project supports a scientific article about digital communication, multilingual online content, sentiment patterns, and thematic trends in Kazakhstan’s YouTube environment.

## Research Objective

The objective of this project is to analyze how popular YouTube video titles in Kazakhstan differ in terms of language, sentiment, thematic vocabulary, and emotionally charged or technology-related content.


## Data Source

Data was collected using the **YouTube Data API v3**.

The project collected metadata from popular YouTube videos using:

- `videos.list`
- `chart="mostPopular"`
- `regionCode="KZ"` for Kazakhstan
- additional comparative regions: `RU` and `US`
- selected YouTube category IDs

## Selected YouTube Categories

The analysis focuses on the following categories:

| Category ID | Category Name |
|---:|---|
| 25 | News & Politics |
| 22 | People & Blogs |
| 27 | Education |
| 28 | Science & Technology |
| 26 | Howto & Style |
| 24 | Entertainment |
| 23 | Comedy |

These categories were selected because their titles are more suitable for linguistic, thematic, and sentiment analysis than categories dominated by music videos, trailers, or gaming clips.

## Dataset

The dataset contains video-level metadata, including:

- video ID
- video title
- channel title
- publication date
- region
- category ID
- category title
- view count
- like count
- comment count
- detected language
- sentiment score
- sentiment label
- content type
- topic modeling results

The final collected dataset contains **715 unique videos** after deduplication.

## Methodology

The project follows this pipeline:

```text
YouTube Data API v3
        ↓
Video metadata collection
        ↓
Text preprocessing
        ↓
Language detection
        ↓
Translation of non-English titles
        ↓
Sentiment analysis using VADER
        ↓
Rule-based content classification
        ↓
Topic modeling using LDA
        ↓
Visualization and interpretation