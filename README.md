# Industrial3D: A Large-Scale Industrial MEP Point Cloud Dataset

**The largest publicly available industrial MEP point cloud dataset for complex scene understanding**

**⚠️ Note:** This repository is under active development. The full dataset and benchmark code will be released soon. **Stay tuned!**

## 📊 Overview

Industrial3D is a large-scale, high-resolution point cloud dataset specifically designed for industrial Mechanical, Electrical, and Plumbing (MEP) scene understanding in water treatment facilities. It enables the first comprehensive cross-paradigm benchmark for industrial point cloud segmentation.

## Key Highlights

| Feature | Industrial3D | Prior MEP Datasets |
|---------|--------------|-------------------|
| **Scale** | **612.7M points** | ~92M points |
| **Domain** | Water treatment facilities | Common buildings |
| **Resolution** | 6mm terrestrial LiDAR | Varies |
| **Learning Paradigms** | 4 (FS, WS, US, FM) | Typically 1-2 |

**Legend:** FS = Fully-Supervised, WS = Weakly-Supervised, US = Unsupervised/Self-Supervised, FM = Foundation Models

### What Makes Industrial3D Unique?

1. **Unprecedented Scale**: 6.6× larger than the most comparable MEP dataset
2. **Industrial Domain**: First large-scale dataset targeting water treatment facilities — a critical infrastructure domain
3. **Cross-Paradigm Benchmark**: Comprehensive evaluation across 4 learning paradigms:
   - Fully-supervised learning (FS)
   - Weakly-supervised learning with sparse labels (WS)
   - Self-supervised/unsupervised learning (US)
   - Foundation models with adaptation (FM)
4. **Real-World Complexity**: Authentic industrial environments with realistic occlusion, sensor noise, and scene complexity

## 🏗️ Dataset Statistics

| Metric | Value |
|--------|-------|
| **Total Labeled Points** | 612.7 million |
| **Semantic Classes** | 12 (MEP + structural) |
| **Facilities** | 13 areas from 7 water treatment plants |
| **Scanning Resolution** | 6mm terrestrial LiDAR |
| **Total Scanned Area** | ~11,237 m² |
| **Annotation Effort** | 754 person-hours |
| **Class Imbalance** | 215:1 (long-tail distribution) |

### Dataset Splits

| Split | Areas | Points | Percentage |
|-------|-------|--------|------------|
| **Training** | 1,2,3,4,5,7,8,10,11,13 | 527.8M | 86.1% |
| **Validation** | 9 (OSCG) | 15.1M | 2.5% |
| **Test** | 6, 12 (Psu, SPH) | 84.9M | 13.9% |

## 📈 Benchmark Results

### Fully-Supervised Learning (FS)

| Method | mIoU |
|--------|------|
| ResPointNet++ (boundary-CB) | **54.05%** |
| ResPointNet++ | **54.05%** |
| KPConv | 53.65% |
| PosPool | 53.18% |
| RandLA-Net | 39.83% |

### Weakly-Supervised Learning (WS) - Label-Efficient

| Method | Labeled Data | mIoU |
|--------|--------------|------|
| SQN | 0.1% | **44.29%** |
| SQN | 0.01% | 33.16% |

> **Insight**: With only 0.1% labels, SQN achieves 44.29% mIoU — demonstrating label-efficient learning potential for industrial applications where annotation is costly.

### Self-Supervised Learning (US)

| Method | mIoU |
|--------|------|
| GrowSP | 11.73% |

### Foundation Models: Point-SAM (FM)

| Setting | mIoU |
|---------|------|
| Zero-shot | 35.2% |
| 10% Few-shot | **74.5%** |

> **Insight**: Point-SAM with 10% few-shot adaptation achieves 74.5% mIoU — significantly outperforming fully-supervised methods, showing the promise of foundation models for industrial point clouds.

### Key Takeaways (Current Results)

*Note: Results are current as of dataset release and subject to update as new methods are evaluated.*

- **Challenging Benchmark**: Even the best fully-supervised method reaches only 54.05% mIoU, indicating the dataset's complexity
- **Long-Tail Challenge**: The 215:1 class imbalance (3.5× more severe than S3DIS) poses significant difficulties for all methods
- **Foundation Model Promise**: Few-shot adaptation dramatically improves performance, suggesting a path forward for industrial applications

## Semantic Classes

12 semantic classes including:
- **MEP components**: pipes, valves, fittings, ducts, cable trays, equipment
- **Structural elements**: walls, floors, ceilings, beams, columns

## Comparison with Related Datasets

| Dataset | Domain | Points | Year |
|---------|--------|--------|------|
| Jing et al. (2024) | Common Buildings | 92.1M | 2024 |
| PSNet5 (2021) | Industrial MEP | 80M | 2021 |
| S3DIS | Indoor Offices | ~27M | 2017 |
| **Industrial3D** | **Water Treatment** | **612.7M** | **2025** |

## Related References

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

@article{yin2026boundarycb,
  title={Resolving Primitive-Sharing Ambiguity in Long-Tailed Industrial Point Cloud Segmentation via Spatial Context Constraints},
  author={Yin, Chao and Han, Qing and Hou, Zhiwei and Liu, Yue and Dai, Anjin and Hu, Hongda and Yang, Ji and Yao, Wei},
  journal={arXiv preprint arXiv:2601.19128},
  year={2026}
}
```

## Citation

```bibtex
@article{industrial3d2026,
  title={Industrial3D: A Large-Scale Industrial MEP Point Cloud Dataset},
  author={Yin, Chao and others},
  journal={TO BE DETERMINED},
  year={2025}
}
```

## License

TBD upon dataset release.

## Contact

For questions and inquiries, please open an issue in this repository or contact me via email (cyinac@connect.ust.hk or chaoyin@ust.hk).

---

**🚀 Coming Soon**: Full dataset release, benchmark leaderboard, and evaluation code!
