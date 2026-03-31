---
layout: page
title: "Spoken Georgian Frequency Analysis"
description: "A data mining project that extracts and analyzes YouTube transcripts to build a frequency list based on natural spoken Georgian."
order: 7
tech: [Python, YouTube Transcript API, Filmot, Data Analysis]
category: data
---

## 📌 Project Overview
Most frequency lists for the Georgian language are derived from formal sources like news articles or academic texts. This project aims to bridge the gap between "classroom Georgian" and "street Georgian" by creating a frequency corpus based on **601 YouTube videos** across various genres.

## ⚙️ The Data Pipeline
The project utilizes a multi-stage extraction and cleaning process:
1.  **Discovery & Filtering:** Used **Filmot** to query the YouTube database specifically for Georgian-language content, filtering for metadata that indicates authentic, high-quality speech.
2.  **Transcript Extraction:** Leveraged the `youtube-transcript-api` in Python to programmatically fetch the captions/transcripts for the identified 601-video dataset.
3.  **Frequency Processing:** A custom Python script cleans the raw text (removing timestamps, formatting, and non-alphabetic characters) and calculates the frequency distribution of tokens.

## 📊 Impact & Insights
The resulting dataset provides a more accurate representation of the **spoken lexicon**—including common filler words, conversational particles, and informal verbal forms—which are often missing from traditional dictionaries.

* **Dataset Size:** 601 videos.
* **Primary Output:** A prioritized "spoken" frequency list.
* **Linguistic Value:** Identifies the "High-Yield" vocabulary truly necessary for listening comprehension in non-formal environments.

## 🛠 Technical Stack
* **Python:** Core processing and API interaction.
* **Filmot:** Advanced metadata filtering for video discovery.
* **YouTube Transcript API:** Automated data retrieval.

[← Back to Projects]({{ site.baseurl }}/)
