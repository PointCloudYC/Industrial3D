# Industrial3D: A Large-Scale Industrial MEP Point Cloud Dataset

**⚠️ Note:** This repository is currently under active development. The full dataset and benchmark code will be released upon paper acceptance. **Stay tuned!**

## 📊 Overview

Industrial3D is the first (to our knowledge) large-scale, high-resolution point cloud dataset specifically designed for industrial Mechanical, Electrical, and Plumbing (MEP) scene understanding. It addresses critical gaps in existing 3D datasets by providing:

- **Scale**: Over 610 million expertly labeled points across 13+ large-scale water treatment facilities
- **Resolution**: 6mm terrestrial laser scanning (TLS) for fine-grained component capture
- **Diversity**: 12 specialized MEP and structural classes
- **Authenticity**: Real-world industrial environments with realistic occlusion, noise, and complexity

### 🏗️ Dataset Statistics

- **Total Scanned Area**: ~20,000 m²
- **Labeled Points**: 2.3+ billion 3D points with over 610 expertly labeled points
- **Point Density**: 6mm TLS resolution at 10-meter range
- **Annotation Effort**: 754 person-hours by 5 domain experts
- **Facilities**: 13+ representative water treatment facilities

## 📈 Benchmark

### Methods Evaluated

**Fully-Supervised Methods:**
- ResPointNet++
- KPConv
- PosPool
- ResPointNet++ with Class-Balanced (CB) loss

**Weakly-Supervised Methods:**
- SQN
- CPCM

**Unsupervised Methods:**
- GrowSP (3-stage pipeline: Superpoints, Primitives, Merged Primitives)

**Foundation Models:**
- Point-SAM
