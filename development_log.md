# Development Timeline – Exploratory 3D Information Retrieval Visualization System

This document tracks the iterative design, interaction, and architectural evolution of the exploratory 3D visualization framework developed for large-scale image embedding datasets.

---

# v0.1 Initial Prototype

## Goal

Develop an interactive 3D visualization environment for exploring clustered image embeddings using Unity.

The first prototype focused on:

* loading embedding coordinates
* visualizing clustered structures in 3D
* testing spatial interaction concepts
* evaluating hierarchical exploration ideas

---

## Initial Interaction Model

The original interaction flow was designed as:

Planet → Expand Subclusters → Reveal Images

Interaction behaviour:

* clicking a planet expanded its child subclusters
* clicking a subcluster revealed image thumbnails
* exploration occurred primarily through expansion/collapse interactions

---

## Observations

While functional, several usability limitations were identified:

* interaction required multiple expansion steps
* navigation flow felt fragmented
* users lost spatial orientation during repeated expansion
* exploration became visually cluttered at deeper levels

These observations motivated a redesign of the interaction workflow.

---

# v0.2 Hierarchical Navigation Redesign

## Interaction Redesign

The interaction system was redesigned to improve:

* navigation clarity
* spatial understanding
* exploratory flow
* immersion during interaction

---

## Updated Interaction Flow

The updated interaction model became:

Planet → Enter Cluster Space → Reveal Subclusters → Reveal Images

Updated behaviour:

* selecting a planet transitions the camera into the cluster space
* subclusters become the primary exploration units
* selecting a subcluster reveals associated image thumbnails directly

---

## Motivation

The redesign aimed to:

* reduce interaction friction
* preserve spatial context during navigation
* improve hierarchy comprehension
* create a more immersive exploratory experience

---

## Result

The updated interaction model significantly improved:

* exploration fluidity
* user orientation
* hierarchy readability
* interaction discoverability

The system began to feel more like navigating an environment rather than expanding interface elements.

---

# v0.3 Embedding Pipeline Integration

## Goal

Integrate machine learning embeddings into the visualization pipeline to support semantic image exploration.

---

## Feature Extraction

Image embeddings were generated using:

* ResNet50 feature extraction

The embeddings captured high-level semantic visual similarity relationships between images.

---

## Dimensionality Reduction

UMAP was introduced to project high-dimensional embeddings into lower-dimensional spaces suitable for:

* clustering
* spatial visualization
* interactive exploration

---

## Dual-UMAP Strategy

A dual-UMAP pipeline was implemented:

### Higher-Dimensional UMAP

Used for:

* clustering quality
* semantic separation
* neighbourhood preservation

### 3D UMAP

Used for:

* visualization layout
* spatial interaction
* immersive exploration

This separation improved clustering reliability while maintaining interpretable spatial layouts.

---

# v0.4 Hierarchical Clustering System

## Goal

Generate a scalable hierarchical structure for large image collections.

---

## HDBSCAN Hierarchy Generation

HDBSCAN clustering was introduced to recursively divide embeddings into:

* top-level clusters
* subclusters
* image groups

The resulting hierarchy formed a tree-like exploration structure.

Hierarchy representation:

* clusters → planets
* subclusters → nodes/moons
* leaf nodes → image thumbnails

---

## Hierarchy Refinement Operations

Several structural refinement operations were implemented:

### Persistence Chain Pruning

Removed weak redundant cluster chains.

### Branch-Only Collapse

Collapsed unnecessary intermediate nodes.

### KNN-Based Noise Rescue

Recovered noisy samples using local neighbourhood relationships.

### Hierarchy Validation

Prevented orphan nodes and invalid hierarchy connections.

---

## Result

The hierarchy became:

* more stable
* more readable
* easier to navigate
* structurally consistent

---

# v0.5 Geometry Preservation Improvements

## Problem

Earlier recursive layout approaches introduced:

* geometric distortion
* inconsistent neighbourhood relationships
* unstable scaling between hierarchy levels
* loss of spatial fidelity

Maintaining embedding-space integrity became a major architectural challenge.

---

# Candidate K Layout Strategy

To preserve structural fidelity, the system introduced:

## Global Anchor + Uniform Planet Scale

Instead of independently normalizing child groups, all entities inside a cluster are positioned relative to a single cluster anchor using:

* translation
* uniform affine scaling

This prevents recursive distortion across hierarchy levels.

---

# Geometry Preservation Goals

The updated layout preserves:

* local neighbourhood relationships
* pairwise distance ratios
* angular relationships
* k-nearest-neighbour structure

---

# Outcome

The Candidate K layout achieved:

* significantly improved structural fidelity
* stable hierarchy scaling
* improved visual consistency
* perfect within-cluster k-NN preservation (1.000 overlap)

---

# v0.6 Visual Refinement & Readability Improvements

## Goal

Improve readability and reduce overlap within dense embedding regions.

---

## Visual Improvements

Several rendering refinements were introduced:

### Logarithmic Node Radius Scaling

Reduced excessive node size growth.

### Depth-Based Size Reduction

Improved hierarchy readability across levels.

### Sibling-Local Radius Capping

Reduced overlap between neighbouring cluster spheres.

### Adaptive Image Quad Sizing

Adjusted thumbnail size based on local density.

---

## Result

The visualization became:

* easier to interpret
* less visually cluttered
* more scalable for dense datasets
* more readable during navigation

---

# v0.7 Large Dataset Scalability Refactor

## Trigger

Scaling from approximately:

* 3,000 images
  to
* 14,000+ images

introduced several challenges:

* increased spatial density
* cluster overlap
* navigation complexity
* rendering overhead
* reduced readability

---

## Architectural Direction

The system architecture was extended to support:

* larger hierarchy structures
* scalable traversal
* improved spatial organization
* future large-scale dataset expansion

Additional hierarchy abstraction layers were investigated to maintain readability and interaction clarity at scale.

---

## Scalability Goals

The refactor focused on:

* preserving embedding geometry
* maintaining hierarchy clarity
* reducing rendering overload
* improving exploration usability
* supporting future dataset growth

---

# v0.8 User Study & Evaluation

## Goal

Evaluate:

* interaction discoverability
* hierarchy understanding
* spatial similarity perception
* exploratory usability

through lightweight user testing.

---

## Study Structure

The evaluation included:

* observer-based usability analysis
* participant feedback questionnaires
* free exploration tasks
* navigation and similarity identification tasks

Six participants took part in the evaluation.

---

## Findings

The study showed that:

* users quickly recognized the system as interactive
* hierarchical exploration was generally intuitive
* nearby images were consistently perceived as semantically related
* progressive reveal interaction improved exploration clarity

Participants responded positively to:

* layered hierarchy interaction
* spatial grouping of similar images
* immersive exploratory navigation

---

## Observed Challenges

Some usability limitations were identified during:

* deep hierarchy traversal
* orientation recovery
* backward navigation between hierarchy levels

These observations provide opportunities for future refinement.

---

# Final System Summary

The final system combines:

* machine learning embeddings
* dimensionality reduction
* hierarchical clustering
* geometry-preserving spatial layout
* immersive interaction design
* exploratory information retrieval
* usability-focused visualization

within a scalable 3D visual analytics framework.

---

# Final System Capabilities

The completed system supports:

* 14,000+ images
* 1,500+ hierarchy nodes
* hierarchical semantic exploration
* progressive reveal interaction
* geometry-preserving embedding visualization
* immersive spatial navigation

---

# Current Project Status

Completed Research Prototype

The project successfully demonstrates how immersive spatial visualization can support exploratory analysis and understanding of large-scale embedding datasets through hierarchical interaction and geometry-preserving visual analytics.
