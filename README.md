# Industrial3D: A Large-Scale Industrial MEP Point Cloud Dataset

**⚠️ Note:** This repository is currently under active development. The full dataset and benchmark code will be released upon paper acceptance. **Stay tuned!**

## 📊 Overview

Industrial3D is the first (to our knowledge) large-scale, high-resolution point cloud dataset specifically designed for industrial Mechanical, Electrical, and Plumbing (MEP) scene understanding. It addresses critical gaps in existing 3D datasets by providing:

- **Scale**: Over 610 million expertly labeled points across 13+ large-scale water treatment facilities
- **Resolution**: 6mm terrestrial laser scanning (TLS) for fine-grained component capture
- **Diversity**: 12 specialized MEP and structural classes
- **Authenticity**: Real-world industrial environments with realistic occlusion, noise, and complexity

## 🖼️ Dataset Preview

![Facility Overview](figures/overview.png)

*Figure: Industrial water treatment facility with UAV photography and annotated point cloud examples.*

![Semantic Classes](figures/Industrial3D_example_points.png)

*Figure: All 12 semantic classes in Industrial3D: Pipe, Cable Tray, Duct, Valve, Instrument, Support, Equipment, Handrail/Grating, Beam, Column, Wall, Floor.*

### 🏗️ Dataset Statistics

- **Total Scanned Area**: ~20,000 m²
- **Labeled Points**: 2.3+ billion 3D points with over 610 expertly labeled points
- **Point Density**: 6mm TLS resolution at 10-meter range
- **Annotation Effort**: 754 person-hours by 5 domain experts
- **Facilities**: 13 areas from 7 water treatment facilities
- **Rooms**: 20 unique rooms/scenes across 13 areas

## 📏 Dataset Scale

![Class Distribution](figures/class_distribution_tiers.pdf)

*Figure: Statistical distribution of 612.7M labeled points across 3 tiers. Industrial3D has a **215:1 class imbalance** (head:tail), 3.5× more severe than S3DIS.*

## 🏭 Dataset Diversity

![Scene Gallery](figures/scene_gallery_v1.pdf)

*Additional Scenes:* [scene_gallery_more_v1.pdf](figures/scene_gallery_more_v1.pdf)

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

## 🎥 Scene Videos

**20 unique rooms** across 13 areas. 4 representative scenes shown below. All videos available on [Google Drive](https://drive.google.com/drive/folders/PLACEHOLDER).

| # | Area | Room | Split | Video |
|---|------|------|-------|-------|
| 1 | Area 2 | Service Gallery | Train | [Watch Video](https://drive.google.com/file/d/PLACEHOLDER) |
| 2 | Area 12 | SPH Pump Room | Test | [Watch Video](https://drive.google.com/file/d/PLACEHOLDER) |
| 3 | Area 6-1 | 93m Psu | Test | [Watch Video](https://drive.google.com/file/d/PLACEHOLDER) |
| 4 | Area 3 | 93m Tank | Train | [Watch Video](https://drive.google.com/file/d/PLACEHOLDER) |

**Rationale for 4 representatives:**
- Service Gallery: Largest (79.6M points), highest MEP density
- SPH Pump Room: Test set representative, compact equipment
- 93m Psu: Test set, moderate complexity
- 93m Tank: Large tank structure, geometric diversity

**All 20 rooms** available on [Google Drive](https://drive.google.com/drive/folders/PLACEHOLDER) with detailed metadata.

## 📚 Citation

**Paper:** [Industrial3D: A Terrestrial LiDAR Point Cloud Dataset and Cross-Paradigm Benchmark for Industrial Infrastructure](https://arxiv.org/abs/2603.28660)

**BibTeX:**

```bibtex
@article{yin2026industrial3d,
  title={Industrial3D: A Terrestrial LiDAR Point Cloud Dataset and Cross-Paradigm Benchmark for Industrial Infrastructure},
  author={Yin, Chao and Yue, Hongzhe and Han, Qing and Hu, Difeng and Liang, Zhenyu and Lin, Fangzhou and Sun, Bing and Wang, Boyu and Li, Mingkai and Yao, Wei and Cheng, Jack C.P.},
  journal={arXiv preprint arXiv:2603.28660},
  year={2026}
}
```

**Links:**
- arXiv: https://arxiv.org/abs/2603.28660
- ISPRS Journal: Submitted (under review)
