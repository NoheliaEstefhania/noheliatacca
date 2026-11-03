---
title: "Paqocha Analyzer: Audio Concordance & Morphological Breakdown for Quechua"
date: 2025-06-01
links:
  - type: site
    url: https://paqocha-analyzer.vercel.app/
  - type: code
    name: Code & Dataset
    url: https://quechuabase.github.io/SimBigASR2026/
tags:
  - NLP
  - Quechua
  - CALL
  - Morphological Analyzer
---

Designed and deployed a reproducible, low-cost YouGlish-style Computer-Assisted Language Learning (CALL) web platform leveraging the spontaneous-speech corpus of Common Voice Puno Quechua (qxp).

<!--more-->

### Key Contributions:
- Built an automated data ingestion pipeline filtering 1,222 transcribed audio recordings.
- Processed speech data through a deterministic, rule-based morphological analyzer that decomposes agglutinative words into roots and suffixes via iterative right-to-left stripping alongside word-level forced timestamp alignment.
- Interactive web interface with word search, synchronized audio playback, and morphosyntactic visualization: [paqocha-analyzer.vercel.app](https://paqocha-analyzer.vercel.app/).
