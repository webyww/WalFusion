# WalFusion

<div align="center">
    <img src="https://github.com/webyww/WalFusion/blob/main/WalFusion.gif" alt="WalFusion" width="1200"/>
</div>

## Project Overview

**WalFusion** is a state-of-the-art LiDAR-camera fusion framework for 3D object detection in autonomous driving. It leverages multi-modal information to achieve high accuracy while maintaining real-time performance.

### Key Features

- 🔹 **High Detection Accuracy:** Achieves competitive mAP and NDS on NuScenes benchmark.
- 🔹 **Efficient Fusion:** Effectively combines LiDAR and camera features.
- 🔹 **Real-time Inference:** Optimized for fast inference with minimal latency.
- 🔹 **Flexible Visualization:** Supports remote or local result visualization.
- 🔹 **Built on Open Source:** Integrates ideas from CenterPoint, BEVFusion, Lift-Splat-Shoot, and more.

---

## Main Results

### NuScenes Detection

| Config          | mAP  | NDS  | Latency (ms) | FPS  | Model      | Log       |
|-----------------|------|------|--------------|------|-----------|----------|
| **WalFusion**   | 67.4 | 71.3 | -            | 16.6 | [baidu]() | [baidu]() |

---

### Visualize Predicted Results

> Private implementation. Visualization can be done remotely or locally.

```bash
# Format results
python tools/test.py $config $checkpoint --format-only --eval-options jsonfile_prefix=$savepath

# Visualize predictions
python tools/analysis_tools/vis.py $savepath/pts_bbox/results_nusc.json



## Acknowledgement

This project is not possible without multiple great open-sourced code bases. We list some notable examples below.

- [open-mmlab](https://github.com/open-mmlab)
- [CenterPoint](https://github.com/tianweiy/CenterPoint)
- [Lift-Splat-Shoot](https://github.com/nv-tlabs/lift-splat-shoot)
- [BEVFusion](https://github.com/mit-han-lab/bevfusion)
- [BEVDet](https://github.com/mit-han-lab/bevfusion)


## Bibtex

If this work is helpful for your research, please consider citing the following BibTeX entries.

```
```
