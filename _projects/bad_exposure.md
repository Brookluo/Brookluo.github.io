---
layout: page
title: A Self-Supervised Learning Method for Bad Exposure Identification
description: Identifying bad exposures in the DECaLS survey using machine learning
# img: assets/img/project/wiro-lae-coadd-D.png
importance: 1
category: research
related_publications: false
---

## Abstract

Recent advancements in machine learning provide new venues to efficiently process large volumes of data, such as exposures in many astronomical imaging campaigns.
These large campaigns usually consist of hundreds of thousands of exposures, whose qualities are essential to any downstream tasks, such as target selections.
Bad exposures in these campaign datasets can be detrimental to the scientific results relying on them.

In this work, we focus on using machine learning algorithms to identify bad exposures from the Dark Energy Spectroscopic Instrument (DESI) Legacy Imaging Surveys with new exposures from the Dark Energy Camera Legacy Survey (DECaLS).

Our bad exposure identification pipeline takes a Vision Transformer (ViT) based approach. In particular, we use a pretrained ViT with DINOv2 framework.
The original ViT was trained with ImageNet, and then we used that trained ViT's backbone to generate the representation of an image, that is, vector embedding.
An embedding is the features of an image presented in a high-dimensional parameter space.
We then use a k-Nearest Neighbor (kNN) algorithm to classify the embeddings after dimension reduction and assign labels to these images based on the embeddings with labels.

## The 3D interactive plot for clustering results

Here presented is the 3D interactive tSNE plots for the clustering of the embeddings.
The original dimension of the embedding vector is 786, which is then reduced to 15 by principle component analysis (PCA). T-SNE algorithm is used to reduce the dimension to 3 (or 2 in the 2D viz) for the visualization.


<div class="l-page">
  <iframe src="{{ 'assets/plotly/all_3D_interactive.html' | relative_url }}" frameborder='0' scrolling='no' height="500px" width="100%" style="border: 1px dashed grey;"></iframe>
</div>

Click on this link to access the full interactive plot: [Interactive Plot](https://brookluo.github.io/assets/plotly/all_3D_interactive.html)


