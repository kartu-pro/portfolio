---
layout: page
title: "Automated Lemma & Morph-Tagging Pipeline"
description: "An automated ETL pipeline using Google Apps Script and LLMs to lemmatize and tag high-frequency word forms."
order: 3
date: 2026-03-19
tech: [Google Apps Script, LLM API, JSON, SQL/Tables, Python]
category: data
---

## 📌 Overview
Manually tagging a corpus for lemmatization and grammatical features is a massive bottleneck in linguistic research. This project automates that process by targeting the most "impactful" words in a corpus and using Large Language Models (LLMs) to perform morphological analysis.

## ⚙️ The Pipeline Architecture
The system functions as a continuous ETL (Extract, Transform, Load) pipeline:

1.  **Frequency Analysis:** Using Python, I generate a frequency list of all word forms in the corpus.
2.  **Pareto Filtering:** To optimize API costs and processing time, the script automatically filters out "long-tail" infrequent forms, focusing only on the top 80% of the corpus volume.
3.  **Automated Trigger:** A **Google Apps Script** runs on a time-based trigger to fetch untagged forms.
4.  **LLM Inference:** The script calls an LLM API with a strict system prompt to return a structured **JSON** response.
5.  **Relational Storage:** Data is parsed and saved into two synchronized tables:
    * **Lemmas Table:** Stores the dictionary headword.
    * **Forms Table:** Stores the specific inflected form linked to its lemma with associated grammatical tags.



## 🛠 Tech Stack
* **Automation:** Google Apps Script (JavaScript-based).
* **Intelligence:** OpenAI/Gemini/Grok API (JSON Mode).
* **Data Prep:** Python (Pandas) for frequency distribution.
* **Storage:** Google Sheets / Relational Tables.

## 🧩 Key Challenges
* **Challenge:** Ensuring the LLM doesn't "hallucinate" linguistic tags or return malformed strings.
* **Solution:** Implemented strict JSON schema validation and a retry logic within the Apps Script to ensure every database entry maintains relational integrity.

## 📈 Results
* **Efficiency:** Automated what would typically take a human linguist months of manual entry.
* **Coverage:** Successfully captured the "core" of the language by prioritizing high-frequency tokens.
* **Data Integrity:** Created a clean, relational dataset ready for use in dictionary building or downstream NLP tasks.

[← Back to Projects]({{ site.baseurl }}/)
