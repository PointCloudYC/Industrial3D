# Industrial3D

**📄 Paper:** [Industrial3D: A Terrestrial LiDAR Point Cloud Dataset and Cross-Paradigm Benchmark for Industrial Infrastructure](https://arxiv.org/abs/2603.28660) (**Under Review**)

**⚠️ Dataset Status:** Under review. Full dataset and code will be released upon journal paper acceptance. Preview materials (videos, figures) available below.

## Overview

Industrial3D is a large-scale, high-resolution point cloud dataset for industrial Mechanical, Electrical, and Plumbing (MEP) scene understanding. Furthermore, we benchmark 9 representative methods on the Industrial3D across 4 DL paradigms (fully supervised, weakly supervised, unsupervised, and foundation model). 

- **Scale:** 612.7 million labeled points from 7 water treatment facilities
- **Resolution:** 6mm terrestrial laser scanning (TLS)
- **Diversity:** 12 semantic classes (MEP + structural elements)
- **Authenticity:** Real industrial environments with realistic occlusion, noise, and complexity

## Figures

![Graphical Abstract](figures/graphical_abstract_v6.png)

*Figure: Industrial3D graphical abstract showing dataset overview and benchmark framework.*

![Facility Overview](figures/overview.png)

*Figure: Industrial water treatment facility with UAV photography and annotated point cloud examples.*

![Semantic Classes](figures/Industrial3D_example_points.png)

*Figure: All 12 semantic classes in Industrial3D: Duct, Elbow, Flange, I-beam, Pipe, Pump, Reducer, Rectangular beam, Strainer, Tank, Tee, Valve.*

![Scene Gallery](figures/scene_gallery_v1.png)

*Figure: Scene gallery of 4 representative scenes in Industrial3D.*

![Additional Scenes](figures/scene_gallery_more_v1.png)

*Figure: Additional scenes in Industrial3D.*

![Class Distribution](figures/class_distribution_tiers.png)

*Figure: Statistical distribution of 612.7M labeled points across 3 tiers. Industrial3D has a **215:1 class imbalance** (head:tail), 3.5× more severe than S3DIS.*


## Scene Videos

**20 unique rooms** across 13 areas. 4 representative scenes:

| # | Area     | Room            | Split | Video          |
|---|----------|-----------------|-------|----------------|
| 1 | Area 2   | Service Gallery | Train | [Watch ▶](videos/Area_2_service_gallery_gt.mp4) |
| 2 | Area 12  | SPH Pump Room   | Test  | [Watch ▶](videos/Area_12_SPHRoom_1_gt.mp4) |
| 3 | Area 6-1 | 93m Psu         | Test  | [Watch ▶](videos/Area_6_OGB_93m_Psu_Rm_gt.mp4) |
| 4 | Area 3   | 93m Tank        | Train | [Watch ▶](videos/Area_3_OGB_93m_Tank_Area_1_gt.mp4) |

### Scene Previews

![Service Gallery](videos/Area_2_service_gallery_gt.gif)

*Area 2: Service Gallery (Train) - Largest at 79.6M points with highest MEP density*

![SPH Pump Room](videos/Area_12_SPHRoom_1_gt.gif)

*Area 12: SPH Pump Room (Test) - Test set representative with compact equipment*

![93m Psu](videos/Area_6_OGB_93m_Psu_Rm_gt.gif)

*Area 6-1: 93m Psu (Test) - Test set with moderate complexity*

![93m Tank](videos/Area_3_OGB_93m_Tank_Area_1_gt.gif)

*Area 3: 93m Tank (Train) - Large tank structure showing geometric diversity*

**Why these 4:**

- Service Gallery: Largest at 79.6M points with highest MEP density
- SPH Pump Room: Test set representative with compact equipment
- 93m Psu: Test set with moderate complexity
- 93m Tank: Large tank structure showing geometric diversity

**📁 Full dataset coming soon!** All 20 rooms (RGB + ground truth videos and renders) will be uploaded to [Google Drive](https://drive.google.com/drive/folders/1T6viLM-SKrDZBCaoKghgld2pIyRq6XLZ?usp=sharing) upon paper acceptance. **Current preview materials available** (videos, renders). **Stay tuned for the complete collection!**

## Dataset Statistics

| Metric              | Value                      |
|---------------------|----------------------------|
| Total Scanned Area  | 20,000+ m² (estimated)                 |
| Labeled Points      | 612.7 million              |
| Raw Scan Data       | 2.3+ billion points        |
| Point Density       | 6mm TLS resolution         |
| Annotation Effort   | 754 person-hours           |
| Facilities          | 13 type of water treatment facilities   |
| Areas               | 13 areas                   |
| Rooms               | 20 unique rooms/scenes     |

## Benchmark

### Methods Evaluated

**Fully-Supervised (6 methods):**
- KPConv
- PosPool
- RandLA-Net
- ResPointNet++
- PTv3 (Point Transformer V3)
- Boundary-CB

**Weakly-Supervised (1 method):**
- SQN (0.1% labels, 0.01% labels)

**Unsupervised (1 method):**
- GrowSP

**Foundation Models (1 method):**
- Point-SAM (Oracle, One-vs-Rest)

### Key Results

| Paradigm          | Method                     | mIoU   |
|-------------------|----------------------------|--------|
| Fully-Supervised  | Boundary-CB                | 55.74% |
| Fully-Supervised  | KPConv                     | 53.65% |
| Fully-Supervised  | PosPool                    | 53.18% |
| Fully-Supervised  | ResPointNet++              | 52.48% |
| Fully-Supervised  | PTv3                       | 41.90% |
| Fully-Supervised  | RandLA-Net                 | 39.83% |
| Weakly-Supervised | SQN (0.1% labels)          | 44.29% |
| Weakly-Supervised | SQN (0.01% labels)         | 33.16% |
| Unsupervised      | GrowSP                     | 11.73% |
| Foundation Model  | Point-SAM (Oracle)         | 21.08% |
| Foundation Model  | Point-SAM (One-vs-Rest)    | 15.79% |

## 📚 Citation

```bibtex
@article{yin2026industrial3d,
  title={Industrial3D: A Terrestrial LiDAR Point Cloud Dataset and Cross-Paradigm Benchmark for Industrial Infrastructure},
  author={Yin, Chao and Yue, Hongzhe and Han, Qing and Hu, Difeng and Liang, Zhenyu and Lin, Fangzhou and Sun, Bing and Wang, Boyu and Li, Mingkai and Yao, Wei and Cheng, Jack C.P.},
  journal={arXiv preprint arXiv:2603.28660},
  year={2026}
}
```

### Related Work

```bibtex
@article{yin2021,
  title={Automated semantic segmentation of industrial point clouds using ResPointNet++},
  author={Yin, Chao and Wang, Boyu and Gan, Vincent JL and Wang, Mi and Cheng, Jack CP},
  journal={Automation in Construction},
  volume={130},
  pages={103874},
  year={2021},
  publisher={Elsevier},
  doi={10.1016/j.autcon.2021.103874}
}

@article{yin2023,
  title={Label-efficient semantic segmentation of large-scale industrial point clouds using weakly supervised learning},
  author={Yin, Chao and Yang, Bo and Cheng, Jack CP and Gan, Vincent JL and Wang, Boyu and Yang, Ji},
  journal={Automation in Construction},
  volume={148},
  pages={104757},
  year={2023},
  issn = {0926-5805},
  doi={10.1016/j.autcon.2023.104757},
}

@article{Yin2026arXiv,
  title={Resolving Primitive-Sharing Ambiguity in Long-Tailed Industrial Point Cloud Segmentation via Spatial Context Constraints},
  author={Yin, Chao and Han, Qing and Hou, Zhiwei and Liu, Yue and Dai, Anjin and Hu, Hongda and Yang, Ji and Yao, Wei},
  journal={arXiv preprint arXiv:2601.19128},
  eprint={2601.19128},
  year={2026}
}
```