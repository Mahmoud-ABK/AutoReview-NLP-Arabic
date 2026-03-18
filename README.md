# Automated Reviewer Assignment for Scientific Papers

## Overview

This project implements an intelligent system for automatically assigning scientific papers to the most suitable reviewers using Machine Learning, NLP, and graph-based disambiguation algorithms.

The system processes Arabic and English research papers, extracts metadata using OCR and text mining, builds semantic representations of articles, and recommends reviewers based on expertise similarity.

This project was developed as part of the Data Treatment & Machine Learning project at ISIMM (2025–2026).

---

## Problem

Reviewer assignment in journals and conferences is usually manual, slow, and error-prone.

Challenges:
- Large number of submissions
- Missing metadata
- Reviewer expertise mismatch
- Long assignment time
- Manual search by editors

Goal:
Build an automated recommendation system that matches papers with qualified reviewers.

---

## Pipeline

1. Data Collection
- Web scraping Arabic academic journals
- Download PDF papers
- Extract metadata

2. OCR & Text Extraction
- Extract first pages of PDF
- OCR conversion
- Clean noisy text
- Normalize Arabic text

3. Metadata Extraction
- Abstract detection
- Keyword extraction
- Author normalization
- Language separation

4. Graph Construction
- Build Author–Article graph
- Normalize author names
- Assign unique IDs
- Graph-based augmentation

5. Feature Engineering
- Combine abstract + keywords
- Arabic text preprocessing
- Stopword removal
- Light stemming

6. Vectorization
- TF-IDF representation
- L2 normalization
- Cosine similarity

7. Reviewer Recommendation
- Find nearest articles
- Apply sequential disambiguation algorithm
- Select best reviewer

---

## Sequential Disambiguation Algorithm

The reviewer is selected using a hierarchical filtering strategy:

1. Find nearest article to query
2. Take its authors as candidates
3. Check next nearest articles
4. Keep common authors
5. Stop when one reviewer remains

This ensures:
- topic relevance
- expertise consistency
- stable recommendation

---

## Technologies

- Python
- Scikit-learn
- NLP
- TF-IDF
- Cosine Similarity
- OCR
- Web Scraping
- Regex
- Graph algorithms
- Arabic NLP

---

## Dataset

- 1600+ articles
- 300+ authors
- Arabic & English papers
- PDF corpus

Sources:
- Arab Journals Platform
- Zenodo dataset
- Arabic scientific journals

---

## Results

- Automatic reviewer recommendation
- Reduced assignment time
- Improved matching accuracy
- Works with missing metadata
- Fully automated pipeline


## Author

Ranim Bouraoui  
Engineering Student – Computer Science  
ISIMM – University of Monastir

Project team:
- Fares Aloulou
- Mahmoud Ben Abdelkader
- Ranim Bouraoui
- Rayen Braiek

Academic Year: 2025-2026

---

## Future Work

- Use BERT / AraBERT embeddings
- Add reviewer workload balancing
- Add collaborative filtering
- Improve multilingual support
- Integrate real journal data

---

## License

Academic / Research project
