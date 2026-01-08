# 🌊 WalFusion  
**Wavelet-based LiDAR–Camera Fusion for Real-Time 3D Object Detection**

<div align="center">
  <img src="https://github.com/webyww/WalFusion/blob/main/WalFusion.gif" width="700"/>
</div>

<p align="center">
  <strong>LiDAR–Camera Fusion · Real-Time · Embedded-Friendly · BEV-based</strong>
</p>

---

## 🔍 Introduction

**WalFusion** is a lightweight and efficient **LiDAR–camera fusion framework** for **3D object detection in autonomous driving**.  
The framework focuses on addressing **cross-modal feature misalignment** while maintaining **real-time performance on embedded platforms**.

WalFusion introduces a **wavelet-based multi-scale feature encoding and fusion strategy**, enabling robust geometric–semantic interaction between LiDAR and camera modalities in the BEV space.

---

## ✨ Key Contributions

- 🧠 **Wavelet-based Feature Encoding**  
  Introduces a wavelet transform to extract **multi-scale spatial–frequency features**, improving cross-modal alignment.

- 🔗 **Efficient Multi-modal Fusion**  
  Combines LiDAR geometry and camera semantics in BEV with **low fusion overhead**.

- ⚡ **Real-Time Deployment**  
  Optimized for embedded inference, achieving real-time FPS on **NVIDIA Orin-X**.

- 📦 **End-to-End Detection Pipeline**  
  Built upon mature open-source detection frameworks, ensuring stability and reproducibility.

---

## 🏗️ Framework Overview

WalFusion follows a **BEV-based fusion paradigm**:

1. **LiDAR branch** extracts geometric BEV features  
2. **Camera branch** lifts image features into BEV space  
3. **Wavelet Depth Encoder** performs multi-scale encoding  
4. **Wavelet Fusion Decoder** aligns and fuses multi-modal features  
5. **Detection head** predicts 3D bounding boxes

> The design emphasizes **lightweight computation** and **deployment feasibility**.

---

## 📊 Experimental Results

### 🔹 nuScenes 3D Detection Benchmark

| Method        | mATE↓ | mASE↓ | mAOE↓ | mAVE↓ | mAAE↓ | mAP↑ | NDS↑ | Latency (ms) | FPS |pth|json|
|--------------|------|------|------|------|------|------|------|-------------|------|------|------|
| **WalFusion** | 26.7 | 25.1 | 25.9 | 24.3 | 12.7 | 70.0 | 73.5 | 47.22 | 16.6 |------|[Google](https://drive.google.com/file/d/1zRW_BGLjztT3T6djr5FensXHawVGe9gB/view?usp=drive_link)|
| **WalFusion** | 26.7 | 25.1 | 25.9 | 24.3 | 12.7 | 70.0 | 73.5 | 47.22 | 16.6 |------|[Google](https://drive.google.com/file/d/1zRW_BGLjztT3T6djr5FensXHawVGe9gB/view?usp=drive_link)|

📌 *Latency is measured on NVIDIA Orin-X.*

---

## 👀 Visualization

Predicted results can be visualized **locally or remotely**.

```bash
# Format prediction results
python tools/test.py $CONFIG $CHECKPOINT \
  --format-only \
  --eval-options jsonfile_prefix=$SAVEPATH

# Visualize nuScenes predictions
python tools/analysis_tools/vis.py \
  $SAVEPATH/pts_bbox/results_nusc.json
```
---

## 📚 Acknowledgements

This project is built upon several excellent open-source works.  
We sincerely thank the authors and contributors for making their code and ideas publicly available.

- [OpenMMLab](https://github.com/open-mmlab)  
- [CenterPoint](https://github.com/tianweiy/CenterPoint)  
- [Lift-Splat-Shoot](https://github.com/nv-tlabs/lift-splat-shoot)  
- [BEVFusion](https://github.com/mit-han-lab/bevfusion)  
- [BEVDet](https://github.com/mit-han-lab/bevdet)

