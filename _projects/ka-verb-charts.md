---
layout: page
title: "Interactive Verb Morphological Dashboard"
description: "A specialized Vue.js interface for comparative linguistic analysis of Georgian verb paradigms."
order: 2
tech: [Vue.js, Google Apps Script, CSS Grid, NLP]
---

# Interactive Verb Morphological Dashboard

## 📌 Project Overview
While computational models can segment Georgian word forms (see [this related project]({{site.baseurl}}/ka-verb-splitter)), human researchers and learners need a way to visualize those segments to identify patterns. This project is a **custom-built web dashboard** designed to take complex morphological data and present it in a highly structured, comparative format.

## ⚙️ Core Features & Linguistic UX
The interface is engineered specifically for the unique challenges of Kartvelian morphology:

* **Synchronized Morphological Alignment:** Verb charts are structured into a master grid that vertically aligns every grammatical slot—from preverbs to roots—allowing for instant visual comparison across different forms.
* **Interactive Cross-Form Highlighting:** Hovering over a specific morpheme automatically illuminates its counterparts across the entire paradigm, making it easy to trace individual markers throughout complex conjugation cycles.
* **Visual Stem & Series Tracking:**
    * **Automated Diffs:** The system detects and color-codes variations between different verb series (e.g., Present vs. Future), clearly isolating stem developments and thematic changes.
    * **Grammatical Anchoring:** Each screeve (grammatical category) is visually distinct, using unique accents to help users stay oriented within the larger verb system.
* **Live Data Integration:** Powered by a Google Apps Script backend, the dashboard dynamically pulls from a relational database that links inflected word forms back to their base lemmas.


## 🛠 Technical Stack
* **Frontend Framework:** Vue.js for reactive state management and search functionality.
* **Styling:** Advanced CSS Grid and custom properties for character-perfect vertical alignment.
* **Backend:** Google Apps Script (GAS) acting as a lightweight API and host.
* **Typography:** Optimized for the **Mkhedruli** script using system fonts for maximum legibility.

## 🔗 The Data Engine
The segmentation data visualized here is powered by a **[CRF-based machine learning model]({{ site.baseurl }}/ka-verb-splitter]. By linking the mathematical accuracy of the CRF with this visual interface, the tool moves beyond simple prediction into true linguistic analysis.

[← Back to Projects]({{ site.baseurl }}/)
