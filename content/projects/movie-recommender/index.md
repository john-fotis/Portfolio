---
title: "High-Performance Go Movie Recommender Engine"
date: 2023-06-15
summary: "Concurrently calculated similarity metrics for big data recommendation processing built in Go."
tags:
  - Development
  - Systems
tech_stack:
  - Go
  - Algorithms
  - Big Data
featured: true
status: "Completed"
role: "Backend Developer"
duration: "2 months"
team_size: 1
highlights:
  - "Leveraged Go goroutines for fast parallel similarity calculations"
  - "Supported Jaccard, Dice, Cosine, and Pearson metrics"
  - "Implemented robust Hybrid filtering strategies"
---

A concurrent big-data recommendation engine built in Go, designed to process large user-item interaction datasets with high throughput and a minimal memory footprint.

## Engineering Challenge

Calculating similarity matrices across massive datasets traditionally creates severe computation bottlenecks. This project was engineered to solve that challenge by leveraging Go's native concurrency primitives (goroutines and channels) to evaluate user preferences across multiple dimensional axes simultaneously.

## Algorithmic Capabilities

The engine is capable of dynamically selecting and executing multiple mathematical models to determine relevance:

- **Similarity Metrics Implemented:**
  - Jaccard Index
  - Dice Coefficient
  - Cosine Similarity
  - Pearson Correlation

## Filtering Approaches

To provide highly personalized outputs, the engine utilizes a multi-tiered filtering approach:

1. **User-User Collaborative Filtering:** Identifying peer grouping similarities.
2. **Item-Item Collaborative Filtering:** Mapping relational boundaries between media.
3. **Tag & Title-based Content Filtering:** Deep metadata analysis.
4. **Hybrid Recommendation Strategy:** Weighting the above outputs to deliver a final, normalized recommendation score.

**Repository:** [GitHub - Movie Recommender](https://github.com/john-fotis/Movie-Recommender)
