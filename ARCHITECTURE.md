# System Architecture

## Overview

The system is an interactive 3D exploratory visualization framework designed for large-scale image embedding datasets. It combines machine learning embeddings, dimensionality reduction, hierarchical clustering, and immersive spatial interaction to support exploratory information retrieval.

The architecture is designed around three major goals:

* preserve embedding-space geometry
* support scalable hierarchical exploration
* maintain interaction clarity for large datasets

---

# Processing Pipeline

Images -> ResNet50 Feature Extraction -> High-Dimensional Embeddings -> UMAP Dimensionality Reduction -> HDBSCAN Hierarchical Clustering -> Hierarchy Cleaning & Validation -> Candidate K Spatial Layout -> Unity 3D Visualization System -> Interactive Exploration

---

# Embedding Generation

Feature extraction is performed using ResNet50 to generate semantic image embeddings from the dataset.

These embeddings capture high-level visual similarity relationships between images and form the basis for clustering and visualization.

---

# Dual-UMAP Pipeline

A dual-UMAP strategy was implemented:

## Higher-Dimensional UMAP

Used for:

* clustering quality
* neighbourhood preservation
* semantic structure separation

## 3D UMAP

Used for:

* visualization layout
* spatial interaction
* immersive exploration

This separation improves clustering stability while maintaining interpretable spatial layouts.

---

# Hierarchical Clustering

The hierarchy is generated using HDBSCAN clustering.

The dataset is recursively divided into clusters and subclusters, producing a tree-like hierarchy.

Hierarchy structure:

* top-level clusters -> planets
* deeper clusters -> subclusters/nodes
* leaf nodes -> image thumbnails

---

# Hierarchy Refinement

Several hierarchy-cleaning operations were introduced to improve structural consistency and readability:

## Persistence Chain Pruning

Removes weak redundant cluster chains.

## Branch-Only Collapse

Eliminates unnecessary intermediate hierarchy nodes.

## KNN-Based Noise Rescue

Reassigns noisy points using local neighbourhood relationships.

## Hierarchy Validation

Prevents orphan nodes and invalid hierarchy connections.

---

# Spatial Layout Strategy

## Challenge

A major challenge was preserving original embedding geometry while avoiding severe overlap and distortion during hierarchical visualization.

Earlier recursive normalization approaches introduced:

* geometric distortion
* neighbourhood inconsistency
* distance warping

---

# Candidate K Layout Strategy

To preserve spatial integrity, the system introduced:

## Global Anchor + Uniform Planet Scale

Every entity inside a cluster is positioned relative to a single cluster anchor using a uniform affine transformation:

* translation
* uniform scaling

No independent recursive normalization is applied to child groups.

---

# Geometry Preservation

The layout preserves:

* local neighbourhood relationships
* pairwise distance ratios
* angular relationships
* k-nearest-neighbour structure

The approach achieved:

* perfect within-cluster k-NN preservation (1.000 overlap)
* significantly improved structural fidelity compared to earlier recursive approaches

---

# Visual Refinements

Several readability improvements were introduced:

* logarithmic node radius scaling
* depth-based size reduction
* sibling local radius capping
* adaptive image quad sizing

These refinements reduce overlap and improve visual clarity for dense datasets.

---

# Interaction System

The visualization uses a progressive reveal interaction model.

## Exploration Flow

1. top-level planets are displayed
2. selecting a planet reveals child clusters
3. deeper interaction progressively reveals image thumbnails

This approach reduces visual clutter while preserving global context.

---

# Scalability

The system currently supports:

* 14,000+ images
* 1,500+ hierarchy nodes

The architecture is being extended to support larger embedding datasets through additional hierarchy abstraction layers and optimized rendering strategies.

---

# Technology Stack

## Data Processing

* Python
* TensorFlow
* Scikit-learn
* UMAP
* HDBSCAN

## Visualization

* Unity 6
* C#
* Custom interaction systems
* Spatial UI logic

---

# Research Areas

This project intersects multiple research and engineering domains:

* Information Visualization
* Immersive Analytics
* Human-Computer Interaction
* Visual Analytics
* Exploratory Information Retrieval
* XR Interaction Design
