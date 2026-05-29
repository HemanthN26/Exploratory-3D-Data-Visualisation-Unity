# Exploratory 3D Information Retrieval Visualization System

Research-oriented immersive analytics system for exploring large



 image embedding datasets through interactive hierarchical 3D environments.

Built using Unity, Python, UMAP, HDBSCAN, and deep visual embeddings.

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
* Supports 14k+ images and 1500+ hierarchy nodes
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

# Scalability Upgrade

The system was initially developed using datasets containing approximately 3,000 images.

To support larger datasets (14k+ images), the architecture was extended with additional hierarchical abstraction layers and improved layout strategies to maintain:

* spatial readability
* hierarchy clarity
* geometry preservation
* navigation usability

The hierarchy is structural only — embedding coordinates remain unchanged.

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
* [Project Roadmap](ROADMAP.md)

---

# Project Status

Active Research Prototype, Under Development

Current work focuses on:

* scalability improvements
* interaction refinement
* rendering optimization
* immersive navigation design
