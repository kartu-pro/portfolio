---
layout: page
title: "Spoken Georgian Frequency Analysis"
description: "A data mining project that extracts and analyzes YouTube transcripts to build a frequency list based on natural spoken Georgian."
order: 8
tech: [Python, YouTube Transcript API, Filmot, Data Analysis]
category: data
---

## 📌 Project Overview
Most frequency lists for the Georgian language are derived from formal sources like news articles or academic texts. This project bridges the gap between formal written Georgian and everyday spoken speech by extracting and analyzing transcript data from **600 YouTube videos** to map real-world lexical usage.

## 📊 Dataset & Corpus Statistics
* **Videos Scraped:** 600
* **Total Tokens (Words):** 1,841,941
* **Unique Word Forms:** 208,053
* **Top 10 Words:** Account for **15.6%** of all spoken occurrences (286,748 tokens).
* **Top 1,000 Words:** Provide **61.0%** text coverage (1,122,704 tokens).
* **80% Coverage Target:** Reached at **10,011 unique words** (~4.8% of total unique forms).

## ⚙️ Pipeline & Architecture
1. **Discovery & Ingestion:** Identified videos via **Filmot** and fetched raw transcript JSON files via `youtube_transcripts.py`.
2. **Token Normalization:** `counts.py` strips non-alphabetic noise, cleans formatting, and generates the final token frequency database (`results.tsv`).
3. **Analytics & Visualization:** `plot.py` and `tables.py` produce linear/logarithmic cumulative coverage graphs and target percentage tables.

## 🛠 File Structure & Outputs
* `transcripts/`: Raw JSON transcript files keyed by YouTube Video ID.
* `videos.csv`: Metadata index of included videos.
* `results.tsv`: Tab-separated frequency list (`word\tcount`).
* `youtube_transcripts.py`, `counts.py`, `plot.py`, `tables.py`: Core ETL and analysis scripts.

## 🚀 Future Roadmap
* **Lemmatization:** Map inflected word forms back to their dictionary headwords to convert the surface-form frequency corpus into a lemma-based list.

[← Back to Projects]({{ site.baseurl }}/)
