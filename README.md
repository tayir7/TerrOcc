# TerrOcc: Terrain-Aware Multi-Modal Occupancy Prediction for Off-Road Scene

[![Paper](https://img.shields.io/badge/Paper-Under_Review-orange.svg)](#)
[![Code](https://img.shields.io/badge/Code-Coming_Soon-red.svg)](#)
[![Dataset](https://img.shields.io/badge/Dataset-ORFDOcc_Coming_Soon-blue.svg)](#)

This is the official repository for the paper **"TerrOcc: Terrain-Aware Multi-Modal Occupancy Prediction for Off-Road Scene"**. 

> **🚧 Note:** The paper is currently under review. The source code, pre-trained weights, and our proposed **ORFDOcc** benchmark dataset will be officially released here upon formal acceptance. Stay tuned!

<!-- <p align="center">
  <img src="docs/pipeline.png" width="90%" alt="TerrOcc Pipeline">
</p> -->

## 📢 News
* **[2026-03]** Our paper has been submitted for review. 
* **[2026-03]** Repository created. Code and the ORFDOcc dataset preparation are in progress.

## 💡 Highlights
* **Novel Off-Road Benchmark (ORFDOcc):** We introduce a comprehensive off-road 3D occupancy benchmark featuring fine-grained semantics (*empty, free, low-risk, and lethal*) specifically designed for unstructured environments.
* **Complementary Depth Supervision (CDS):** A novel module that explicitly addresses extreme LiDAR sparsity and geometric voids at long distances by anchoring dense Vision Foundation Model (VFM) depth to physical scale.
* **Terrain-Aware Fusion (TRF):** An adaptive spatial-channel attention mechanism that fuses multi-modal features based on voxel-level geometric energy, preventing representation collapse in wild terrains.

# Demo
## Semantic Occupancy Annotations

### ORFDOcc Dataset
<div align="center">
  <video width="95%" controls preload="metadata">
    <source src="demo/orfd-twoScense.mp4" type="video/mp4">
    你的浏览器不支持视频播放，请 <a href="demo/orfd-twoScense.mp4">点击下载</a> 查看。
  </video>
</div>

<br>

### WildOcc Dataset
<div align="center">
  <video width="95%" controls preload="metadata">
    <source src="demo/Wildocc_twoScense.mp4" type="video/mp4">
    你的浏览器不支持视频播放，请 <a href="demo/Wildocc_twoScense.mp4">点击下载</a> 查看。
  </video>
</div>

---

## TODO List
We are actively working on cleaning up the codebase for public release.

- [ ] Release the proposed **ORFDOcc** dataset.
- [ ] Release data preparation scripts for both ORFDOcc and the public WildOcc dataset.
- [ ] Release the core PyTorch implementation (training & evaluation code).
- [ ] Release pre-trained models.
- [ ] Provide visualization tools for 3D off-road occupancy.

## 📊 Dataset Preview (Coming Soon)
Our codebase supports evaluation on our proposed **ORFDOcc** and the public **WildOcc** dataset. Once the code is released, the expected data structure should be organized as follows:
```text
TerrOcc/
└── data/
    ├── ORFD/                         # Our proposed dataset (Coming Soon)
    │   ├── depth_gt/                 
    │   ├── training/                 # images, lidar, pose, dense_depth, GT_occ...
    │   └── validation/
    └── WildOcc/                      # Public dataset
        ├── depth_gt/
        ├── 00000/                    # raw sensor data, calib, pose, occ_gt...
        └── 00001/
```

## 📜 Citation
Citation information will be updated upon formal publication.

```bibtex
% Coming Soon
@article{terrocc2026,
  title={TerrOcc: Terrain-Aware Multi-Modal Occupancy Prediction for Off-Road Scene},
  author={Anonymous Authors},
  journal={Under Review},
  year={2026}
}
```

## 🤝 Acknowledgement
Many thanks to the open-source community. Our codebase is largely built upon [OpenOccupancy](https://github.com/JeffWang987/OpenOccupancy) and [SurroundOcc](https://github.com/weiyithu/SurroundOcc).
