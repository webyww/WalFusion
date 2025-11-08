# WalFusion

<div align="center">
    <img src="https://github.com/webyww/WalFusion/blob/main/WalFusion.gif" alt="WalFusion" width="400" />


## Main Results
### Nuscenes Detection
| Config                                                                    | mAP        | NDS        | Latency(ms) | FPS  | Model                                                                                          | Log                                                                                            |

| [**WalFusion**]() | 67.4 | 71.3 |-  |16.6 | [baidu]() | [baidu]() |







#### Visualize the predicted result.

- Private implementation. (Visualization remotely/locally)

```shell
python tools/test.py $config $checkpoint --format-only --eval-options jsonfile_prefix=$savepath
python tools/analysis_tools/vis.py $savepath/pts_bbox/results_nusc.json
```


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
@article{huang2023dal,
  title={Detecting As Labeling: Rethinking LiDAR-camera Fusion in 3D Object Detection},
  author={Huang, Junjie and Ye, Yun and Liang, Zhujin and Shan, Yi and Du, Dalong},
  journal={arXiv preprint arXiv:2311.07152},
  year={2023}
}
```
