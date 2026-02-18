# Development Log – Interactive 3D Visualization System

## Version 1 – Initial Interaction Model
Interaction design:
- Clicking planet → moons expand
- Clicking moon → thumbnails appear

Observation:
This interaction required multiple steps and reduced navigation efficiency.

---

## Version 2 – Improved Interaction Model
Updated design:
- Clicking planet → user enters cluster space
- Clicking moon → thumbnails appear immediately

Reason for change:
Reduced interaction steps and improved spatial understanding.

## Current Focus
Optimising spatial layout and preparing system for user study evaluation.

---

## Version 3 – Large Dataset Architecture Refactor (Current)

### Trigger
New dataset contains ~12,000 images with higher class diversity.

### Problem Observed
The previous hierarchy (Cluster → Subcluster → Image) caused:

- spatial overcrowding
- difficult navigation
- reduced interpretability
- visual overlap between semantic regions

### Design Decision
Introduce a new abstraction level above clusters to group semantically related clusters.

New hierarchy:

SuperCluster → Cluster → SubCluster → Image

### Implementation Changes
- Extended dataset parser to support additional hierarchy metadata
- Updated prefab generation pipeline
- Modified navigation controller for multi-level traversal
- Optimised activation logic to prevent rendering overload

### Key Constraint Maintained
Embedding geometry must remain unchanged.  
Hierarchy is only used for exploration structure, not spatial transformation.

### Expected Outcome
- Scales to datasets >10k points
- Maintains interpretability
- Improves navigation clarity
- Supports future dataset growth

