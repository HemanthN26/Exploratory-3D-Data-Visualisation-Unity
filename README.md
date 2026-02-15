# Exploratory 2D/3D Data Visualisation using Unity

An interactive research oriented visualisation system for exploring high-dimensional datasets through spatial 2D and 3D environments.

---

## Demo


https://github.com/user-attachments/assets/a5498874-f8cc-4f23-9e60-d5b61107b8b3


---

## Overview

This project investigates how spatial interaction in 3D environments influences users understanding of complex data.  
It combines dimensionality reduction, interactive visualisation, and immersive navigation techniques to enable intuitive exploration of high-dimensional datasets.

Instead of traditional static plots, this system allows users to **navigate data as a virtual environment** where clusters, relationships, and outliers can be explored interactively.

---

## Research Goal

The goal is to evaluate whether immersive spatial visualisation improves users ability to:

- perceive cluster structure
- understand similarity relationships
- detect outliers
- explore large datasets efficiently

---

## Research Question

> Does interactive 3D spatial visualisation improve human perception and exploration of high-dimensional data compared to traditional 2D visualisations?

---

## Core Concepts

- Dimensionality reduction using **UMAP**
- Feature extraction using **ResNet50**
- Spatial metaphor based visualisation
- Interactive cluster exploration
- Hierarchical information disclosure

---

## Interaction Design

The system uses a hierarchical spatial interaction model:

| Level | Representation | Interaction |
|------|----------------|-------------|
Clusters | Planets | Click to expand |
Subclusters | Moons | Click to reveal thumbnails |
Data Points | Thumbnails | Click to inspect |

### Design Principles
- Progressive disclosure to reduce visual clutter  
- Spatial grouping to preserve similarity relationships  
- Distance-based relevance cues  
- Direct manipulation interaction  

This structure allows users to explore large datasets without losing global context.

---

## Technology Stack

**Data Processing**
- Python
- TensorFlow
- Scikit-learn
- UMAP

**Visualisation**
- Unity 6 (C#)
- Custom interaction system
- Spatial UI logic

---

## System Pipeline

Raw Data -> Feature Extraction (ResNet50) -> Dimensionality Reduction (UMAP) -> Spatial Mapping -> Unity Interactive Environment -> User Exploration

---

## Current Features

- Interactive 3D cluster exploration
- Spatial navigation of embeddings
- Click based hierarchical interaction
- Distance-aware visualisation logic
- Outlier highlighting
- Dynamic expansion and collapse of clusters

---

## Current Development Focus

- Refining spatial layout accuracy
- Improving interaction responsiveness
- Enhancing visual feedback cues
- Optimising rendering performance
- Preparing controlled user evaluation study

---

## Planned Evaluation Study

A structured user study will be conducted to evaluate the effectiveness of immersive data exploration.

Metrics to be measured:

- Task completion time
- Accuracy of cluster identification
- Outlier detection performance
- Interaction efficiency
- User confidence
- Qualitative usability feedback

---

## Research Relevance

This project is relevant for research fields including:

- Information Visualisation
- Human Computer Interaction
- Visual Analytics
- Immersive Analytics
- XR Interaction Design

---

## Project Status

**Active Research Prototype - Under Development**

New interaction techniques and evaluation experiments are currently being implemented.


