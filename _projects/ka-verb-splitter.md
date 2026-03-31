---
layout: page
title: "Georgian Verb Splitter"
description: "A CRF-based NLP tool for morphological segmentation of complex Georgian verb structures."
order: 1
date: 2026-03-17
tech: [Python, Scikit-learn, CRFsuite, NLP]
---

# Georgian Verb Splitter (CRF-Based)

## 📌 Overview
This project addresses the high-complexity task of morphological segmentation for Georgian verbs. This tool automates the splitting of these forms (ie გავაკეთებდი -> გა-ვ-აკეთ-ებ-დი).

> **Key Achievement:** Achieved **~98% word-level accuracy** across a dataset of 13,674 forms derived from ~300 unique lemmas.

## 🛠 Tech Stack
* **Machine Learning:** Conditional Random Fields (CRF) via `sklearn-crfsuite`.
* **Data Processing:** Python, Pandas.
* **Linguistic Framework:** Morphological slot-mapping for Kartvelian languages.

## 🧩 Architecture & Core Logic
The model treats segmentation as a sequence labeling problem. To handle the unique challenges of Georgian orthography and morphology, I implemented a three-state logic for the CRF:

* **I (Inside):** The character belongs within a morpheme.
* **S (Single):** Represents a standard morpheme boundary (split with `-`).
* **N (Null):** Handles the "empty slot" phenomenon (split with `--`), crucial for maintaining the structural integrity of the 5-slot system.

## 📈 Current Performance
* **Dataset Size:** 13,674 verb forms.
* **Accuracy:** ~98% (Word-level).
* **Robustness:** Handles PFSF (Pre-radical/Post-radical) changes and root variations within specific screeves.

## 🚀 Next Steps
* **Visualize Split Forms:** See related project [here]({{site.baseurl}}/projects/ka-verb-charts).
* **Automated Database Splitting:** Using `predict.py` to run batch processing on massive verb form databases.
* **Heuristic Flagging:** Implementing a review system for "irregular" changes (e.g., when a root shifts unexpectedly within a screeve).
* **Human-in-the-loop:** A manual update interface for linguists to review flagged forms.

[← Back to Projects]({{ site.baseurl }}/)
