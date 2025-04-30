# Political Affiliation Scoring from Twitter Follow Networks

This project was developed as part of a master's dissertation focused on estimating political affiliation strength using only Twitter (X) **follow data**. The goal was to understand how **network structure** reflects political alignment — particularly the **strength of loyalty** to Republican or Democrat parties — using a combination of classical network science and neural embedding techniques.

## 🔍 Project Goals

- Construct a **shared-following network** of U.S. politicians.
- Detect **party communities** using graph-based community detection.
- Develop and test various **metrics** (e.g. internal/external degrees, PageRank, HITS, betweenness, etc.) to score party loyalty strength.
- Compare **manual network metrics** with **neural graph embeddings**.
- Evaluate each method against ground-truth affiliation scores derived from voting records.

---

## 📁 Notebooks Overview

| Notebook | Purpose |
|----------|---------|
| `argmax_ga.ipynb` | Implements a genetic algorithm to optimize loyalty metrics (not used in final dissertation). |
| `community_split.ipynb` | Explores various graph-based community detection methods (e.g., Louvain, Kernighan-Lin). |
| `weighted_graph.ipynb` | Analyzes how edge weights (based on shared follow count) impact community structure. |
| `network_analysis.ipynb` | Performs general structural analysis (e.g., degree distribution, density, clustering). |
| `improve_network.ipynb` | Filters the bipartite network (e.g., by removing low-degree nodes) to reduce noise. |
| `old_affiliation_score.ipynb` | Early version of affiliation scoring logic (not used in final work). |
| `link_length_network.ipynb` | Experimental notebook testing a link-length-based metric (not used but conceptually interesting). |
| `new_affiliation_score.ipynb` | Core notebook for the dissertation’s **network science-based** loyalty metrics. |
| `neural_embedding_affiliation_score.ipynb` | Uses **Node2Vec** + **PCA** to generate neural embeddings and correlate them to affiliation scores. |

---

## 🧰 Requirements

This project uses the following Python packages:

- `pandas`
- `numpy`
- `networkx`
- `community` (for Louvain community detection)
- `matplotlib`
- `seaborn`
- `scikit-learn` (`sklearn`)
- `torch` (for some embedding experimentation)

You can install all dependencies with:

```bash
pip install pandas numpy networkx python-louvain matplotlib seaborn scikit-learn torch
