# Exploratory 3D Information Retrieval Visualization System

Research-oriented immersive analytics system for exploring large-scale image embedding datasets through interactive hierarchical 3D environments.

Built using Unity, Python, UMAP, HDBSCAN, and deep visual embeddings.

---

# Demo

<!-- Add demo video or GIF here -->

https://github.com/user-attachments/assets/97244e5b-92ec-4933-a9a9-d7e192c1154a

---

# Visual Overview

### Hierarchical Cluster Exploration

<!-- Add cluster overview screenshot -->
<img width="1122" height="865" alt="image" src="https://github.com/user-attachments/assets/26377f56-c120-46f2-809f-4748361095d4" />


### Embedding Space Visualization

<!-- Add embedding screenshot -->
<img width="680" height="314" alt="image" src="https://github.com/user-attachments/assets/c9b137ea-8117-485d-b9fe-271ba1ca8d12" />


---

# Overview

This project investigates how spatial interaction in 3D environments influences human understanding of high-dimensional data.

Instead of traditional static visualizations, the system enables users to explore embedding spaces as interactive spatial environments where semantic relationships, clusters, and outliers can be navigated directly.

The visualization combines:

* machine learning embeddings
* dimensionality reduction
* hierarchical clustering
* immersive interaction design
* exploratory visual analytics

to create a scalable exploratory information retrieval environment.

---

# Key Features

* Interactive hierarchical 3D exploration
* Geometry-preserving embedding visualization
* Progressive reveal interaction system
* HDBSCAN-based hierarchical clustering
* Outlier-aware visual exploration
* Supports 14,000+ images and 1,500+ hierarchy nodes
* Usability-tested interaction workflow

---

# Interaction Model

The system uses a progressive hierarchical interaction model:

| Level       | Representation | Interaction         |
| ----------- | -------------- | ------------------- |
| Clusters    | Planets        | Enter cluster space |
| Subclusters | Nodes / Moons  | Reveal image groups |
| Images      | Thumbnails     | Inspect samples     |

This interaction strategy reduces visual clutter while maintaining spatial context during exploration.

---

# System Pipeline

Images -> ResNet50 Feature Extraction -> Embedding Generation -> UMAP Dimensionality Reduction -> HDBSCAN Hierarchical Clustering -> Geometry-Preserving Spatial Layout -> Unity Interactive Visualization -> Exploratory User Interaction

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

# Geometry Preservation Strategy

A major challenge in hierarchical embedding visualization is preserving spatial relationships while scaling across multiple hierarchy levels.

To address this, the system implements a geometry-preserving layout strategy using:

* global cluster anchors
* uniform affine transformations
* consistent spatial scaling

This preserves:

* local neighbourhood structure
* pairwise distance relationships
* angular consistency
* k-nearest-neighbour integrity

while maintaining hierarchical readability.

---

# Scalability

The system was initially developed using datasets containing approximately 3,000 images.

The final implementation supports:

* 14,000+ images
* 1,500+ hierarchy nodes

through scalable hierarchical clustering, progressive reveal interaction, and optimized spatial layout strategies.

---

# User Study Summary

A lightweight usability study was conducted to evaluate:

* interaction discoverability
* hierarchy understanding
* spatial similarity perception
* navigation usability

The study showed that users generally:

* quickly understood the interaction model
* perceived nearby images as visually related
* navigated the hierarchy intuitively
* responded positively to progressive reveal interaction

Additional details are available in the user study documentation.

---

# Research Areas

This project intersects multiple research and engineering domains:

* Information Visualization
* Immersive Analytics
* Human-Computer Interaction
* Visual Analytics
* Exploratory Information Retrieval
* XR Interaction Design

---

# Documentation

* [Architecture Details](ARCHITECTURE.md)
* [User Study Summary](USER_STUDY.md)
* [Development Timeline](development_log.md)
* [Future Research Directions](ROADMAP.md)

---

# Project Status

Completed Research Prototype

Key implemented contributions:

* geometry-preserving hierarchical visualization
* immersive spatial exploration workflow
* scalable clustering architecture
* usability-evaluated interaction design

The project demonstrates how immersive visualization techniques can support exploratory analysis and understanding of large-scale embedding datasets through interactive hierarchical spatial environments.





