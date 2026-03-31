---
layout: page
title: "Field-to-Flashcard: Automated Data Pipeline"
description: "A custom annotation tool and automation suite that converts raw field recordings into structured audio-visual learning assets."
order: 5
tech: [HTML5 Canvas, Python, FFmpeg, ImageMagick, Shell]
category: data
---

## 📌 Project Overview
Linguistic fieldwork often results in hours of video footage that is difficult to process manually. I developed this workflow to streamline the extraction of high-quality audio-visual pairs from recordings of native speakers. This allows for the rapid creation of digital study assets (like Anki decks) from raw video interviews.

## 🛠 The Annotation Interface
To solve the problem of manual "timestamp hunting," I built a custom **HTML5-based annotation tool**. It allows the user to:
* **Segment Audio:** Visually define the precise start and end points of a spoken word or phrase.
* **Define Spatial Crops:** Use a coordinate-based UI to draw a bounding box around the physical object or picture the speaker is pointing to.
* **Metadata Export:** Save these time and coordinate data points as a structured configuration file for batch processing.

## ⚙️ The Processing Engine
Once the annotation is complete, a series of automated scripts (Python and Shell) handle the heavy lifting:
* **Precision Extraction:** Uses `FFmpeg` to extract audio segments with sub-second accuracy.
* **Automated Cropping:** Processes the video frames using `ImageMagick` or `FFmpeg` filters to generate high-resolution photos based on the user's saved coordinates.
* **Asset Optimization:** Normalizes audio levels and compresses images for immediate compatibility with flashcard apps like **Anki** or relational databases.

## 📈 Impact
This pipeline reduces the time required to process field video, transforming a tedious manual editing task into a streamlined "tag-and-export" workflow. It ensures that every audio clip is perfectly synced with its corresponding visual representation.

[← Back to Projects]({{ site.baseurl }}/)
