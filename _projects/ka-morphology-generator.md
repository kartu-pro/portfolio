---
layout: page
title: "Python Morphology Generator"
description: "A programmatic engine for generating exhaustive Georgian word forms from minimal linguistic inputs."
order: 6
tech: [Python, OOP, Morphology, NLP]
---

## 📌 Project Overview
Georgian morphology is notoriously complex, featuring high levels of inflection and agglutination. This project is a **computational grammar engine** that automates the generation of complete word paradigms. By providing minimal "seed" data, the engine applies internal rules to produce every valid form of a noun, adjective, or verb.

## ⚙️ Core Logic & Inputs
The engine is designed to be highly efficient, requiring only the "unpredictable" parts of a word to build the full set of forms:
* **Nouns & Adjectives:** Accepts a lemma and a boolean for `hasSyncopation` to generate all 14 case forms (singular/plural) plus common postpositional attachments.
* **Verbs:** Uses a structured input of `root`, `preverb`, `pfsf` (Passive/Future Stem Formant), and `type (1-4)` to navigate the complex Georgian conjugation system.

## 📊 Structured Output
Instead of returning simple strings, the generator outputs a **list of (label, value) pairs**. 
* **Example:** `('PREVERB', 'გა'),  ('ROOT', 'აკეთ'), ('PFSF', 'ებ') [Future, 2s]`.
* **Interoperability:** This structured data can be easily piped into visualization tools (like the Verb Dashboard), joined into full word forms for datasets, or used to train machine learning models.

## 🛠 Future Roadmap
* **Advanced Verb Logic:** Implementing root-vowel changes (apophony) between different screeve series.
* **Extended Postpositions:** Expanding the library of clitics and postpositions for more granular noun declension.
* **Inverse Processing:** Developing a **Lemmatizer** mode to reverse the process—taking an inflected form and identifying its base root and grammatical markers.

## 🔗 The Pipeline Role
This generator can serve as the "Backbone" logic for other Georgian language projects.

[← Back to Projects]({{ site.baseurl }}/)
