---
layout: page
title: "GeoDrills: Georgian Grammar Trainer"
description: "A modular morphological training app for Georgian, featuring multi-modal drilling from multiple-choice to active production."
order: 4
tech: [Vue.js, JSON, CSS3 Animations, GitHub Pages]
category: apps
link_demo: "https://kartu-pro.github.io/GeoDrills-mvp/App.html?drill=c3225131-0470-5a69-bcca-ab81947f0d04"
---


## 📌 Overview
Mastering Georgian requires high-repetition drilling of complex morphological shifts (like syncope in nouns or versionizer changes in verbs). **GeoDrills** is a prototype web application designed to move students from passive recognition to active production through targeted, high-frequency practice.

## 🎯 Modular Drill Architecture
The app is built on a "drill-down" hierarchy, allowing users to isolate specific linguistic pain points:
* **Category Selection:** Focus on broad parts of speech (Verbs, Nouns) or phonological patterns (Sounds).
* **Targeted Scoping:** Drill down into specific grammatical "situations," such as the Future Tense or Syncopating Nouns.
* **Progressive Difficulty:**
    - **Level 1 (Passive):** Multiple-choice recognition.
    - **Level 2 (Active):** Text-entry "type the answer" for morphological production.
    - **Level 3 (Translate/Produce):** Contextual translation and pronunciation-focused exercises.

## ✨ Interactive Features
* **Optimized Input Workflow:** High-speed keyboard support allows users to navigate the entire drill (e.g., using `Enter` to submit and advance) without ever leaving the "home row," facilitating a deep flow state during repetitive study.
* **Non-Blocking Background Fetch:** To eliminate transition latency, the app pre-fetches the next linguistic module and its associated assets in the background while the user is still interacting with the current question, resulting in a "zero-load" experience between items.
* **Active Production Validation:** The UI provides a side-by-side contrastive analysis of "User Typed" vs. "Target Form," using character-level diffing to help students catch subtle orthographic or morphological errors instantly.
* **Mobile-First Design:** Engineered with a responsive layout to allow for "micro-learning" sessions on the go.

## 🛠 Technical Implementation
The app utilizes a Google Sheets/Apps Script to serve structured JSON drill sets, which a Vue.js frontend consumes and displays, making it easy to scale the curriculum without modifying the core application logic.

## 🚀 Live Demo
**[🌐 Try the GeoDrills MVP]({{ page.link_demo }})** *(Note: This is an MVP; certain drill modules are currently in development.)*

[← Back to Projects]({{ site.baseurl }}/)
