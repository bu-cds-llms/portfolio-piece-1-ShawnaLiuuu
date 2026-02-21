# From Static Embeddings to Context: Analyzing Self-Attention Mechanisms

## Overview
This project investigates how self-attention transforms static word embeddings into context-sensitive representations. Using pretrained 50-dimensional GloVe embeddings, I apply scaled dot-product self-attention to two structurally similar sentences and visualize attention weight distributions. I further examine the mathematical role of the scaling factor by comparing attention behavior with and without normalization.

## Methods
- Pretrained GloVe embeddings (50-dimensional)
- Manual implementation of scaled dot-product attention
- Comparison of scaled vs unscaled attention
- Heatmap visualization of attention weights
- Analysis of semantic shifts using minimal sentence variation

No learned projection matrices or positional encodings were used to isolate the mechanics of attention.

## Key Results
- Scaled attention produces distributed weight patterns that allow moderate cross-token interaction
- Removing the scaling factor causes attention to collapse toward self-focus
- Static embeddings do not dynamically encode referential shifts (e.g., pronoun resolution)
- The scaling term $$\sqrt(d_k)$$ plays a critical role in preventing softmax saturation

## How to run
1. Install required packages (see below)
2. Open *notebook/Portfolio_Piece_1.ipynb*
3. Run all cells from top to bottom
4. Attention visualizations will be saved in the *outputs/* directory

Note: The first run may take several minutes to download pretrained GloVe embeddings

## Requirements 
- Python 3.9+
- torch
- gensim
- matplotlib
- seaborn
- numpy
