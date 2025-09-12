[![Awesome Logo](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![arXiv](https://img.shields.io/badge/arXiv-2509.07996-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2509.07996)
![Visitors](https://komarev.com/ghpvc/?username=worldbench&repo=survey&label=Hello,%20Visitor%20&color=yellow&style=social)
[![PR's Welcome](https://img.shields.io/badge/PRs-welcome-red.svg?style=flat)](https://github.com/worldbench/survey/pulls)

# :sunglasses: Awesome 3D and 4D World Models

| <img width="100%" src="docs/figures/teaser.png"> |
|:-:|

This survey reviews state-of-the-art **3D and 4D world models** - systems that learn, predict, and simulate the geometry and dynamics of real environments from multi-modal signals. 

We unify terminology, scope, and evaluations, and organize the space into three complementary paradigms by representation:
| | |
|:-:|:-|
| <img width="240px" src="docs/figures/icon_videogen.png"> | Learn generative or predictive models from sequential video streams with geometric and temporal constraints. VideoGen focuses on long-horizon consistency, controllability, and scene-level generation, enabling agents to imagine or forecast plausible video rollouts. |
| <img width="240px" src="docs/figures/icon_occgen.png"> | Model 3D/4D occupancy grids that encode geometry and semantics in voxel space. OccGen provides a physics-consistent scaffold for robust perception, forecasting, and simulation, bridging low-level sensor data and high-level reasoning. |
| <img width="240px" src="docs/figures/icon_lidargen.png"> | Leverage point cloud sequences from LiDAR sensors to generate or predict geometry-grounded scenes. LiDARGen emphasizes high-fidelity 3D structure, robustness to environment changes, and applications in safety-critical domains such as autonomous driving. |
| | |

For more details, kindly refer to our [paper](https://huggingface.co/papers/2509.07996) and [project page](https://worldbench.github.io/survey). :rocket:


### :books: Citation 

If you find this work helpful for your research, please kindly consider citing our paper:
```bib
@article{survey_3d_4d_world_models,
    title   = {3D and 4D World Modeling: A Survey},
    author  = {Lingdong Kong and Wesley Yang and Jianbiao Mei and Youquan Liu and Ao Liang and Dekai Zhu and Dongyue Lu and Wei Yin and Xiaotao Hu and Mingkai Jia and Junyuan Deng and Kaiwen Zhang and Yang Wu and Tianyi Yan and Shenyuan Gao and Song Wang and Linfeng Li and Liang Pan and Yong Liu and Jianke Zhu and Wei Tsang Ooi and Steven C. H. Hoi and Ziwei Liu},
    journal = {arXiv preprint arXiv:2509.07996},
    year    = {2025},
}
```



### Table of Contents
- [**0. Background**](#background)
- [**1. Benchmarks \& Datasets**](#1-benchmarks--datasets)
    - [Benchmarks](#benchmarks)
    - [Datasets](#datasets)
- [**2. World Modeling from Video Generation**](#2-world-modeling-from-video-generation)
    - [Data Engines](#one-data-engines)
    - [Action Interpreters](#two-action-interpreters)
    - [Neural Simulators](#three-neural-simulators)
    - [Scene Reconstructors](#four-scene-reconstructors)
- [**3. World Modeling from Occupancy Generation**](#3-world-modeling-from-occupancy-generation)
    - [Scene Representors](#one-scene-representors)
    - [Occupancy Forecasters](#two-occupancy-forecasters)
    - [Autoregressive Simulators](#three-autoregressive-simulators)
- [**4. World Modeling from LiDAR Generation**](#4-world-modeling-from-lidar-generation)
    - [Data Engines](#one-data-engines-1)
    - [Action Forecasters](#two-action-forecasters)
    - [Autoregressive Simulators](#three-autoregressive-simulators-1)
- [**5. Applications**](#5-applications)
    - [Autonomous Driving](#one-autonomous-driving)
    - [Robotics](#two-robotics)
    - [Video Games \& XR](#three-video-games--xr)
    - [Digital Twins](#four-digital-twins)
- [**6. Other Resources**](#6-other-resources)
    - [Workshops](#workshops)
    - [Tutorials](#tutorials)
    - [Talks \& Seminars](#talks--seminars)
- [**7. Acknowledgements**](#7-acknowledgements)



# Background

| | |
|:-:|:-|
| <img width="240px" src="docs/figures/teaser_anni-min.gif"> | World modeling has become a cornerstone of modern AI, enabling agents to understand, represent, and predict dynamic environments. While prior research has focused primarily on 2D images and videos, the rapid emergence of native 3D and 4D representations (e.g., RGB-D, occupancy grids, LiDAR point clouds) calls for a dedicated study. |
| | |


## What Are Native 3D Representations?

Unlike 2D projections, native 3D/4D signals directly encode metric geometry, visibility, and motion in the physical coordinates where agents act. Examples include:
- RGB-D imagery (2D images with depth channels)
- Occupancy grids (voxelized maps of free vs. occupied space)
- LiDAR point clouds (3D coordinates from active sensing)
- Neural fields (e.g., NeRF, Gaussian Splatting)


## What Are World Models in 3D and 4D?

A 3D/4D world model is an internal representation that allows an agent to **imagine**, **forecast**, and **interact** with its environment in the 3D space.
| | |
|:-:|:-|
| <img width="100px" src="docs/figures/icon_generative.gif"> | **Generative World Models:**<br>synthesize plausible 3D/4D worlds under conditions (e.g., text prompts, trajectories). |
| <img width="100px" src="docs/figures/icon_predictive.gif"> | **Predictive World Models:**<br>anticipate the future evolution of 3D/4D scenes given past observations and actions. |
| | |

Together, these models provide the foundation for simulation, planning, and embodied intelligence in complex environments.

| <img width="100%" src="docs/figures/tree.png"> |
|:-:|





# 1. Benchmarks & Datasets

### Benchmarks

| <img width="100px" src="docs/figures/logo_worldbench.gif"> | <img width="100px" src="docs/figures/logo_vbench.jpg"> | <img width="100px" src="docs/figures/logo_worldscore.png"> |
|:-:|:-:|:-:|
| [**WorldBench**](https://github.com/worldbench/evalkit) | [**VBench**](https://github.com/Vchitect/VBench) | [**WorldScore**](https://github.com/haoyi-duan/WorldScore) | 


### Datasets

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | 
|:-:|:-|:-:|:-:|
||
| `KITTI` | Are We Ready for Autonomous Driving? The KITTI Vision Benchmark Suite | CVPR 2012 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://www.cvlibs.net/datasets/kitti/) |
| `NYUv2` | Indoor Segmentation and Support Inference from RGBD Images | ECCV 2012 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://cs.nyu.edu/~fergus/datasets/nyu_depth_v2.html) |
| `CARLA` | [![arXiv](https://img.shields.io/badge/arXiv-1711.03938-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/1711.03938)<br>CARLA: An Open Urban Driving Simulator | CoRL 2017 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://carla.org/) |
| `SemanticKITTI` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/1904.01416)<br>SemanticKITTI: A Dataset for Semantic Scene Understanding of LiDAR Sequences | ICCV 2019 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://semantic-kitti.org/) |
| `nuScenes` | [![arXiv](https://img.shields.io/badge/arXiv-1903.11027-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/1903.11027)<br>nuScenes: A Multimodal Dataset for Autonomous Driving | CVPR 2020 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://www.nuscenes.org/) |
| `Waymo Open` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/1912.04838)<br>Scalability in Perception for Autonomous Driving: Waymo Open Dataset | CVPR 2020 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://waymo.com/open/) |
| `STF` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/1902.08913)<br>Seeing Through Fog Without Seeing Fog: Deep Multimodal Sensor Fusion in Unseen Adverse Weather | CVPR 2020 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/princeton-computational-imaging/SeeingThroughFog) |
| `Virtual KITTI 2` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2001.10773)<br>Virtual KITTI 2 | arXiv 2020 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://europe.naverlabs.com/proxy-virtual-worlds-vkitti-2/) |
| `Argoverse 2` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2301.00493)<br>Argoverse 2: Next Generation Datasets for Self-Driving Perception and Forecasting | NeurIPS 2021 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://www.argoverse.org/av2.html) |
| `Lyft-Level5` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2006.14480)<br>One Thousand and One Hours: Self-Driving Motion Prediction Dataset | CoRL 2021 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/lyft/nuscenes-devkit/) |
| `nuPlan` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2106.11810)<br>nuPlan: A Closed-Loop ML-Based Planning Benchmark for Autonomous Vehicles | CVPRW 2021 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://www.nuscenes.org/nuplan) |
| `PandaSet` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2112.12610)<br>PandaSet: Advanced Sensor Suite Dataset for Autonomous Driving | ITSC 2022 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://pandaset.org/) |
| `OpenCOOD` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2109.07644)<br>OPV2V: An Open Benchmark Dataset and Fusion Pipeline for Perception with Vehicle-to-Vehicle Communication | ICRA 2022 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://mobility-lab.seas.ucla.edu/opv2v/) |
| `KITTI-360` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2109.13410)<br>KITTI-360: A Novel Dataset and Benchmarks for Urban Scene Understanding in 2D and 3D | TPAMI 2022 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://www.cvlibs.net/datasets/kitti-360/) |
| `CarlaSC` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2203.07060)<br>MotionSC: Data Set and Network for Real-Time Semantic Mapping in Dynamic Environments | RA-L 2022 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://umich-curly.github.io/CarlaSC.github.io/) |
| `Robo3D` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2303.17597)<br>Robo3D: Towards Robust and Reliable 3D Perception against Corruptions | ICCV 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/ldkong1205/Robo3D) |
| `OpenOccupancy` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2303.03991)<br>OpenOccupancy: A Large Scale Benchmark for Surrounding Semantic Occupancy Perception | ICCV 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/JeffWang987/OpenOccupancy) |
| `Occ3D-nuScenes` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2304.14365)<br>Occ3D: A Large-Scale 3D Occupancy Prediction Benchmark for Autonomous Driving | NeurIPS 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://tsinghua-mars-lab.github.io/Occ3D/) |
| `OpenDV-YouTube` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.09630)<br>GenAD: Generalized Predictive Model for Autonomous Driving | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/OpenDriveLab/DriveAGI/blob/main/opendv/README.md) |
| `SSCBench` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2306.09001)<br>SSCBench: A Large-Scale 3D Semantic Scene Completion Benchmark for Autonomous Driving | IROS 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/ai4ce/SSCBench) |
| `NAVSIM` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.15349)<br>NAVSIM: Data-Driven Non-Reactive Autonomous Vehicle Simulation and Benchmarking | NeurIPS 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/autonomousvision/navsim) |
| `DrivingDojo` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.10738)<br>DrivingDojo Dataset: Advancing Interactive and Knowledge-Enriched Driving World Model | NeurIPS 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://huggingface.co/datasets/Yuqi1997/DrivingDojo) |
| `EUVS` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.05256)<br>Extrapolated Urban View Synthesis Benchmark | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://ai4ce.github.io/EUVS-Benchmark/) |
| `Pi3DET` | [![arXiv](https://img.shields.io/badge/arXiv-1904.01416-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2507.17665)<br>Perspective-Invariant 3D Object Detection | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://pi3det.github.io) |




# 2. World Modeling from Video Generation

### :one: Data Engines

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `BEVControl` | [![arXiv](https://img.shields.io/badge/arXiv-2308.01661-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2308.01661)<br>BEVControl: Accurately Controlling Street-View Elements with Multi-Perspective Consistency via BEV Sketch Layout | arXiv 2023 | - | - |
| `BEVGen` | [![arXiv](https://img.shields.io/badge/arXiv-2301.04634-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2301.04634)<br>Street-View Image Generation from a Bird's-Eye View Layout | RA-L 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadriverse.github.io/bevgen/) | [![GitHub](https://img.shields.io/github/stars/alexanderswerdlow/BEVGen)](https://github.com/alexanderswerdlow/BEVGen) |
| `MagicDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2310.02601-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2310.02601)<br>MagicDrive: Street View Generation with Diverse 3D Geometry Control | ICLR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://gaoruiyuan.com/magicdrive/) | [![GitHub](https://img.shields.io/github/stars/cure-lab/MagicDrive)](https://github.com/cure-lab/MagicDrive) |
| `Panacea` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.16813)<br>Panacea: Panoramic and Controllable Video Generation for Autonomous Driving | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://panacea-ad.github.io/) | [![GitHub](https://img.shields.io/github/stars/wenyuqing/panacea)](https://github.com/wenyuqing/panacea) |
| `DrivingDiffusion` | [![arXiv](https://img.shields.io/badge/arXiv-2310.07771-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2310.07771)<br>DrivingDiffusion: Layout-Guided Multi-View Driving Scene Video Generation with Latent Diffusion Model | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drivingdiffusion.github.io/) | [![GitHub](https://img.shields.io/github/stars/shalfun/DrivingDiffusion)](https://github.com/shalfun/DrivingDiffusion) |
| `WoVoGen` | [![arXiv](https://img.shields.io/badge/arXiv-2312.02934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.02934)<br>WoVoGen: World Volume-Aware Diffusion for Controllable Multi-Camera Driving Scene Generation | ECCV 2024 | - | [![GitHub](https://img.shields.io/github/stars/fudan-zvg/WoVoGen)](https://github.com/fudan-zvg/WoVoGen) |
| `Delphi` | [![arXiv](https://img.shields.io/badge/arXiv-2406.01349-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.01349)<br>Unleashing Generalization of End-to-End Autonomous Driving with Controllable Long Video Generation | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://westlake-autolab.github.io/delphi.github.io/) | [![GitHub](https://img.shields.io/github/stars/westlake-autolab/Delphi)](https://github.com/westlake-autolab/Delphi) |
| `SimGen` | [![arXiv](https://img.shields.io/badge/arXiv-2406.09386-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.09386)<br>SimGen: Simulator-Conditioned Driving Scene Generation | NeurIPS 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadriverse.github.io/simgen/) | [![GitHub](https://img.shields.io/github/stars/metadriverse/SimGen)](https://github.com/metadriverse/SimGen) |
| `BEVWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2407.05679-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.05679)<br>BEVWorld: A Multimodal World Simulator for Autonomous Driving via Scene-Level BEV Latents | arXiv 2024 | - | - |
| `Panacea+` | [![arXiv](https://img.shields.io/badge/arXiv-2408.07605-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2408.07605)<br>Panacea+: Panoramic and Controllable Video Generation for Autonomous Driving | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://panacea-ad.github.io/) | - |
| `DiVE` | [![arXiv](https://img.shields.io/badge/arXiv-2409.01595-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.01595)<br>DiVE: DiT-Based Video Generation with Enhanced Control | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://liautoad.github.io/DIVE/) | [![GitHub](https://img.shields.io/github/stars/LiAutoAD/DIVE)](https://github.com/LiAutoAD/DIVE) |
| `SyntheOcc` | [![arXiv](https://img.shields.io/badge/arXiv-2410.00337-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.00337)<br>SyntheOcc: Synthesize Geometric-Controlled Street View Images through 3D Semantic MPIs | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://len-li.github.io/syntheocc-web/) | [![GitHub](https://img.shields.io/github/stars/EnVision-Research/SyntheOcc)](https://github.com/EnVision-Research/SyntheOcc) |
| `HoloDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2412.01407-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.01407)<br>HoloDrive: Holistic 2D-3D Multi-Modal Street Scene Generation for Autonomous Driving | arXiv 2024 | - | - |
| `CogDriving` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03520-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03520)<br>Seeing Beyond Views: Multi-View Driving Scene Video Generation with Holistic Attention | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://luhannan.github.io/CogDrivingPage/) | - |
| `UniMLVG` | [![arXiv](https://img.shields.io/badge/arXiv-2412.04842-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.04842)<br>UniMLVG: Unified Framework for Multi-View Long Video Generation with Comprehensive Control Capabilities for Autonomous Driving | arXiv 2024 | - | [![GitHub](https://img.shields.io/github/stars/SenseTime-FVG/OpenDWM)](https://github.com/SenseTime-FVG/OpenDWM) |
| `DrivePhysica` | [![arXiv](https://img.shields.io/badge/arXiv-2412.08410-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.08410)<br>Physical Informed Driving World Model | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadrivescape.github.io/papers_project/DrivePhysica/page.html) | - |
| `DriveDreamer-2` | [![arXiv](https://img.shields.io/badge/arXiv-2403.06845-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.06845)<br>DriveDreamer-2: LLM-Enhanced World Models for Diverse Driving Video Generation | AAAI 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drivedreamer2.github.io/) | [![GitHub](https://img.shields.io/github/stars/f1yfisher/DriveDreamer2)](https://github.com/f1yfisher/DriveDreamer2) |
| `SubjectDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2403.19438-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.19438)<br>SubjectDrive: Scaling Generative Data in Autonomous Driving via Subject Control | AAAI 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://subjectdrive.github.io/) | - |
| `Glad` | [![arXiv](https://img.shields.io/badge/arXiv-2503.00045-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.00045)<br>Glad: A Streaming Scene Generator for Autonomous Driving | ICLR 2025 | - | [![GitHub](https://img.shields.io/github/stars/xb534/Glad)](https://github.com/xb534/Glad) |
| `DualDiff` | [![arXiv](https://img.shields.io/badge/arXiv-2505.01857-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.01857)<br>DualDiff: Dual-Branch Diffusion Model for Autonomous Driving with Semantic Fusion | ICRA 2025 | - | [![GitHub](https://img.shields.io/github/stars/yangzhaojason/DualDiff)](https://github.com/yangzhaojason/DualDiff) |
| `UniScene` | [![arXiv](https://img.shields.io/badge/arXiv-2412.05435-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.05435)<br>UniScene: Unified Occupancy-Centric Driving Scene Generation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://arlo0o.github.io/uniscene/) | [![GitHub](https://img.shields.io/github/stars/Arlo0o/UniScene-Unified-Occupancy-centric-Driving-Scene-Generation)](https://github.com/Arlo0o/UniScene-Unified-Occupancy-centric-Driving-Scene-Generation) |
| `DriveScape` | [![arXiv](https://img.shields.io/badge/arXiv-2409.05463-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.05463)<br>DriveScape: Towards High-Resolution Controllable Multi-View Driving Video Generation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadrivescape.github.io/papers_project/drivescapev1/index.html) | - |
| `PerLDiff` | [![arXiv](https://img.shields.io/badge/arXiv-2407.06109-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.06109)<br>PerLDiff: Controllable Street View Synthesis Using Perspective-Layout Diffusion Models | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://perldiff.github.io/) | [![GitHub](https://img.shields.io/github/stars/LabShuHangGU/PerlDiff)](https://github.com/LabShuHangGU/PerlDiff) |
| `MagicDrive-V2` | [![arXiv](https://img.shields.io/badge/arXiv-2411.13807-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.13807)<br>MagicDrive-V2: High-Resolution Long Video Generation for Autonomous Driving with Adaptive Control | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://gaoruiyuan.com/magicdrive-v2/) | - |
| `Cosmos-Transfer1` | [![arXiv](https://img.shields.io/badge/arXiv-2503.14492-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.14492)<br>Cosmos-Transfer1: Conditional World Generation with Adaptive Multimodal Control | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/dir/cosmos-transfer1/) | [![GitHub](https://img.shields.io/github/stars/nvidia-cosmos/cosmos-transfer1)](https://github.com/nvidia-cosmos/cosmos-transfer1) |
| `DualDiff+` | [![arXiv](https://img.shields.io/badge/arXiv-2503.03689-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.03689)<br>DualDiff+: Dual-Branch Diffusion for High-Fidelity Video Generation with Reward Guidance | arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/yangzhaojason/DualDiff)](https://github.com/yangzhaojason/DualDiff) |
| `CoGen` | [![arXiv](https://img.shields.io/badge/arXiv-2503.22231-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.22231)<br>CoGen: 3D Consistent Video Generation via Adaptive Conditioning for Autonomous Driving | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://xiaomi-research.github.io/cogen/) | - |
| `NoiseController` | [![arXiv](https://img.shields.io/badge/arXiv-2504.18448-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2504.18448)<br>NoiseController: Towards Consistent Multi-View Video Generation via Noise Decomposition and Collaboration | arXiv 2025 | - | - |
| `STAGE` | [![arXiv](https://img.shields.io/badge/arXiv-2506.13138-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.13138)<br>STAGE: A Stream-Centric Generative World Model for Long-Horizon Driving-Scene Simulation | arXiv 2025 | - | - |
||



### :two: Action Interpreters

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `GAIA-1` | [![arXiv](https://img.shields.io/badge/arXiv-2309.17080-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2309.17080)<br>GAIA-1: A Generative World Model for Autonomous Driving | arXiv 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wayve.ai/thinking/scaling-gaia-1/) | - |
| `ADriver-I` | [![arXiv](https://img.shields.io/badge/arXiv-2311.13549-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.13549)<br>ADriver-I: A General World Model for Autonomous Driving | arXiv 2023 | - | - |
| `Drive-WM` | [![arXiv](https://img.shields.io/badge/arXiv-2311.17918-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.17918)<br>Driving into the Future: Multiview Visual Forecasting and Planning with World Model for Autonomous Driving | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drive-wm.github.io/) | [![GitHub](https://img.shields.io/github/stars/BraveGroup/Drive-WM)](https://github.com/BraveGroup/Drive-WM) |
| `DriveDreamer` | [![arXiv](https://img.shields.io/badge/arXiv-2309.09777-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2309.09777)<br>DriveDreamer: Towards Real-World-Driven World Models for Autonomous Driving | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drivedreamer.github.io/) | [![GitHub](https://img.shields.io/github/stars/JeffWang987/DriveDreamer)](https://github.com/JeffWang987/DriveDreamer) |
| `GenAD` | [![arXiv](https://img.shields.io/badge/arXiv-2403.09630-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.09630)<br>GenAD: Generalized Predictive Model for Autonomous Driving | CVPR 2024 | - | [![GitHub](https://img.shields.io/github/stars/OpenDriveLab/DriveAGI)](https://github.com/OpenDriveLab/DriveAGI) |
| `Vista` | [![arXiv](https://img.shields.io/badge/arXiv-2405.17398-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.17398)<br>Vista: A Generalizable Driving World Model with High Fidelity and Versatile Controllability | NeurIPS 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://vista-demo.github.io/) | [![GitHub](https://img.shields.io/github/stars/OpenDriveLab/Vista)](https://github.com/OpenDriveLab/Vista) |
| `InfinityDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2412.01522-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.01522)<br>InfinityDrive: Breaking Time Limits in Driving World Models | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadrivescape.github.io/papers_project/InfinityDrive/page.html) | - |
| `DrivingGPT` | [![arXiv](https://img.shields.io/badge/arXiv-2412.18607-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.18607)<br>DrivingGPT: Unifying Driving World Modeling and Planning with Multi-Modal Autoregressive Transformers | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://rogerchern.github.io/DrivingGPT/) | - |
| `DrivingWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2412.19505-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.19505)<br>DrivingWorld: Constructing World Model for Autonomous Driving via Video GPT | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://huxiaotaostasy.github.io/DrivingWorld/index.html) | [![GitHub](https://img.shields.io/github/stars/YvanYin/DrivingWorld)](https://github.com/YvanYin/DrivingWorld) |
| `GEM` | [![arXiv](https://img.shields.io/badge/arXiv-2412.11198-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.11198)<br>GEM: A Generalizable Ego-Vision Multimodal World Model for Fine-Grained Ego-Motion, Object Dynamics, and Scene Composition Control | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://vita-epfl.github.io/GEM.github.io/) | [![GitHub](https://img.shields.io/github/stars/vita-epfl/GEM)](https://github.com/vita-epfl/GEM) |
| `MaskGWM` | [![arXiv](https://img.shields.io/badge/arXiv-2502.11663-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.11663)<br>MaskGWM: A Generalizable Driving World Model with Video Mask Reconstruction | CVPR 2025 | - | [![GitHub](https://img.shields.io/github/stars/SenseTime-FVG/OpenDWM)](https://github.com/SenseTime-FVG/OpenDWM) |
| `Epona` | [![arXiv](https://img.shields.io/badge/arXiv-2506.24113-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.24113)<br>Epona: Autoregressive Diffusion World Model for Autonomous Driving | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://kevin-thu.github.io/Epona/) | [![GitHub](https://img.shields.io/github/stars/Kevin-thu/Epona)](https://github.com/Kevin-thu/Epona) |
| `VaViM & VaVAM` | [![arXiv](https://img.shields.io/badge/arXiv-2502.15672-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.15672)<br>VaViM and VaVAM: Autonomous Driving through Video Generative Modeling | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://valeoai.github.io/vavim-vavam/) | [![GitHub](https://img.shields.io/github/stars/valeoai/VideoActionModel)](https://github.com/valeoai/VideoActionModel) |
| `MiLA` | [![arXiv](https://img.shields.io/badge/arXiv-2503.15875-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.15875)<br>MiLA: Multi-View Intensive-Fidelity Long-Term Video Generation World Model for Autonomous Driving | arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/xiaomi-mlab/mila.github.io)](https://github.com/xiaomi-mlab/mila.github.io) |
| `GAIA-2` | [![arXiv](https://img.shields.io/badge/arXiv-2503.20523-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.20523)<br>GAIA-2: A Controllable Multi-View Generative World Model for Autonomous Driving | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wayve.ai/thinking/gaia-2) | - |
| `DriVerse` | [![arXiv](https://img.shields.io/badge/arXiv-2504.18576-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2504.18576)<br>DriVerse: Navigation World Model for Driving Simulation via Multimodal Trajectory Prompting and Motion Alignment | arXiv 2025 | - | - |
| `PosePilot` | [![arXiv](https://img.shields.io/badge/arXiv-2505.01729-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.01729)<br>PosePilot: Steering Camera Pose for Generative World Models with Self-Supervised Depth | arXiv 2025 | - | - |
| `ProphetDWM` | [![arXiv](https://img.shields.io/badge/arXiv-2505.18650-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.18650)<br>ProphetDWM: A Driving World Model for Rolling Out Future Actions and Videos | arXiv 2025 | - | - |
| `LongDWM` | [![arXiv](https://img.shields.io/badge/arXiv-2506.01546-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.01546)<br>LongDWM: Cross-Granularity Distillation for Building A Long-Term Driving World Model | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wang-xiaodong1899.github.io/longdwm/) | [![GitHub](https://img.shields.io/github/stars/Wang-Xiaodong1899/Long-DWM)](https://github.com/Wang-Xiaodong1899/Long-DWM) |
||



## :three: Neural Simulators

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `MagicDrive3D` | [![arXiv](https://img.shields.io/badge/arXiv-2405.14475-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.14475)<br>MagicDrive3D: Controllable 3D Generation for Any-View Rendering in Street Scenes | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://gaoruiyuan.com/magicdrive3d/) | [![GitHub](https://img.shields.io/github/stars/flymin/MagicDrive3D)](https://github.com/flymin/MagicDrive3D) |
| `DreamForge` | [![arXiv](https://img.shields.io/badge/arXiv-2409.04003-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.04003)<br>DreamForge: Motion-Aware Autoregressive Video Generation for Multi-View Driving Scenes | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://pjlab-adg.github.io/DriveArena/dreamforge/) | [![GitHub](https://img.shields.io/github/stars/PJLab-ADG/DriveArena)](https://github.com/PJLab-ADG/DriveArena) |
| `Doe-1` | [![arXiv](https://img.shields.io/badge/arXiv-2412.09627-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.09627)<br>Doe-1: Closed-Loop Autonomous Driving with Large World Model | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wzzheng.net/Doe/) | [![GitHub](https://img.shields.io/github/stars/wzzheng/Doe)](https://github.com/wzzheng/Doe) |
| `DrivingSphere` | [![arXiv](https://img.shields.io/badge/arXiv-2411.11252-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.11252)<br>DrivingSphere: Building A High-Fidelity 4D World for Closed-Loop Simulation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yanty123.github.io/DrivingSphere/) | [![GitHub](https://img.shields.io/github/stars/yanty123/DrivingSphere)](https://github.com/yanty123/DrivingSphere) |
| `UMGen` | [![arXiv](https://img.shields.io/badge/arXiv-2503.14945-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.14945)<br>Generating Multimodal Driving Scenes via Next-Scene Prediction | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yanhaowu.github.io/UMGen/) | [![GitHub](https://img.shields.io/github/stars/YanhaoWu/UMGen)](https://github.com/YanhaoWu/UMGen) |
| `DriveArena` | [![arXiv](https://img.shields.io/badge/arXiv-2408.00415-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2408.00415)<br>DriveArena: A Closed-Loop Generative Simulation Platform for Autonomous Driving | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://pjlab-adg.github.io/DriveArena/) | [![GitHub](https://img.shields.io/github/stars/PJLab-ADG/DriveArena)](https://github.com/PJLab-ADG/DriveArena) |
| `InfiniCube` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>InfiniCube: Unbounded and Controllable Dynamic 3D Driving Scene Generation with World-Guided Video Models | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/infinicube/) | [![GitHub](https://img.shields.io/github/stars/nv-tlabs/InfiniCube)](https://github.com/nv-tlabs/InfiniCube) |
| `DiST-4D` | [![arXiv](https://img.shields.io/badge/arXiv-2503.15208-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.15208)<br>DiST-4D: Disentangled Spatiotemporal Diffusion with Metric Depth for 4D Driving Scene Generation | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://royalmelon0505.github.io/DiST-4D/) | [![GitHub](https://img.shields.io/github/stars/royalmelon0505/dist4d)](https://github.com/royalmelon0505/dist4d) |
| `UniFuture` | [![arXiv](https://img.shields.io/badge/arXiv-2503.13587-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.13587)<br>Seeing the Future, Perceiving the Future: A Unified Driving World Model for Future Generation and Perception | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://dk-liang.github.io/UniFuture/) | [![GitHub](https://img.shields.io/github/stars/dk-liang/UniFuture)](https://github.com/dk-liang/UniFuture) |
| `Nexus` | [![arXiv](https://img.shields.io/badge/arXiv-2504.10485-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2504.10485)<br>Decoupled Diffusion Sparks Adaptive Scene Generation | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://opendrivelab.com/Nexus/) | [![GitHub](https://img.shields.io/github/stars/OpenDriveLab/Nexus)](https://github.com/OpenDriveLab/Nexus) |
| `Challenger` | [![arXiv](https://img.shields.io/badge/arXiv-2505.15880-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.15880)<br>Challenger: Affordable Adversarial Driving Video Generation | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://pixtella.github.io/Challenger/) | [![GitHub](https://img.shields.io/github/stars/Pixtella/Challenger)](https://github.com/Pixtella/Challenger) |
| `Cosmos-Drive` | [![arXiv](https://img.shields.io/badge/arXiv-2506.09042-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.09042)<br>Cosmos-Drive-Dreams: Scalable Synthetic Driving Data Generation with World Foundation Models | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/cosmos_drive_dreams/) | [![GitHub](https://img.shields.io/github/stars/nv-tlabs/Cosmos-Drive-Dreams)](https://github.com/nv-tlabs/Cosmos-Drive-Dreams) |
||



### :four: Scene Reconstructors

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `3DGS` | [![arXiv](https://img.shields.io/badge/arXiv-2401.01339-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2401.01339)<br>3D Gaussian Splatting for Real-Time Radiance Field Rendering | TOG 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/) | [![GitHub](https://img.shields.io/github/stars/graphdeco-inria/gaussian-splatting)](https://github.com/graphdeco-inria/gaussian-splatting)
| `StreetGaussian` | [![arXiv](https://img.shields.io/badge/arXiv-2401.01339-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2401.01339)<br>Street Gaussians: Modeling Dynamic Urban Scenes with Gaussian Splatting | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://zju3dv.github.io/street_gaussians) | [![GitHub](https://img.shields.io/github/stars/zju3dv/street_gaussians)](https://github.com/zju3dv/street_gaussians) |
| `4DGF` | [![arXiv](https://img.shields.io/badge/arXiv-2406.03175-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.03175)<br>Dynamic 3D Gaussian Fields for Urban Areas | NeurIPS 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://tobiasfshr.github.io/pub/4dgf/) | [![GitHub](https://img.shields.io/github/stars/tobiasfshr/map4d)](https://github.com/tobiasfshr/map4d) |
| `SCube` | [![arXiv](https://img.shields.io/badge/arXiv-2410.20030-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.20030)<br>SCube: Instant Large-Scale Scene Reconstruction using VoxSplats | NeurIPS 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/scube/) | [![GitHub](https://img.shields.io/github/stars/nv-tlabs/SCube)](https://github.com/nv-tlabs/SCube) |
| `HUGS` | [![arXiv](https://img.shields.io/badge/arXiv-2403.12722-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.12722)<br>HUGS: Holistic Urban 3D Scene Understanding via Gaussian Splatting | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://xdimlab.github.io/hugs_website/) | [![GitHub](https://img.shields.io/github/stars/hyzhou404/HUGS)](https://github.com/hyzhou404/HUGS) |
| `MagicDrive3D` | [![arXiv](https://img.shields.io/badge/arXiv-2405.14475-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.14475)<br>MagicDrive3D: Controllable 3D Generation for Any-View Rendering in Street Scenes | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://gaoruiyuan.com/magicdrive3d/) | [![GitHub](https://img.shields.io/github/stars/flymin/MagicDrive3D)](https://github.com/flymin/MagicDrive3D) |
| `S3Gaussian` | [![arXiv](https://img.shields.io/badge/arXiv-2405.20323-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.20323)<br>S3Gaussian: Self-Supervised Street Gaussians for Autonomous Driving | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wzzheng.net/S3Gaussian/) | [![GitHub](https://img.shields.io/github/stars/nnanhuang/S3Gaussian)](https://github.com/nnanhuang/S3Gaussian/) |
| `VDG` | [![arXiv](https://img.shields.io/badge/arXiv-2406.18198-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.18198)<br>VDG: Vision-Only Dynamic Gaussian for Driving Simulation | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://3d-aigc.github.io/VDG/) | [![GitHub](https://img.shields.io/github/stars/lifuguan/VDG_official)](https://github.com/lifuguan/VDG_official) |
| `UniGaussian` | [![arXiv](https://img.shields.io/badge/arXiv-2411.15355-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.15355)<br>UniGaussian: Driving Scene Reconstruction from Multiple Camera Models via Unified Gaussian Representations | arXiv 2024 | - | - |
| `Stag-1` | [![arXiv](https://img.shields.io/badge/arXiv-2412.05280-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.05280)<br>Stag-1: Towards Realistic 4D Driving Simulation with Video Generation Model | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wzzheng.net/Stag/) | [![GitHub](https://img.shields.io/github/stars/wzzheng/Stag)](https://github.com/wzzheng/Stag) |
| `DrivingRecon` | [![arXiv](https://img.shields.io/badge/arXiv-2412.09043-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.09043)<br>DrivingRecon: Large 4D Gaussian Reconstruction Model For Autonomous Driving | arXiv 2024 | - | [![GitHub](https://img.shields.io/github/stars/EnVision-Research/DriveRecon)](https://github.com/EnVision-Research/DriveRecon) |
| `OccScene` | [![arXiv](https://img.shields.io/badge/arXiv-2412.11183-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.11183)<br>OccScene: Semantic Occupancy-Based Cross-Task Mutual Learning for 3D Scene Generation | arXiv 2024 | - | - |
| `SGD` | [![arXiv](https://img.shields.io/badge/arXiv-2403.20079-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.20079)<br>SGD: Street View Synthesis with Gaussian Splatting and Diffusion Prior | WACV 2025 | - | - |
| `OmniRe` | [![arXiv](https://img.shields.io/badge/arXiv-2408.16760-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2408.16760)<br>OmniRe: Omni Urban Scene Reconstruction| ICLR 2025 |[![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://ziyc.github.io/omnire/) | [![GitHub](https://img.shields.io/github/stars/ziyc/drivestudio)](https://github.com/ziyc/drivestudio) |
| `DriveDreamer4D` | [![arXiv](https://img.shields.io/badge/arXiv-2410.13571-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.13571)<br>DriveDreamer4D: World Models Are Effective Data Machines for 4D Driving Scene Representation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drivedreamer4d.github.io/) | [![GitHub](https://img.shields.io/github/stars/GigaAI-research/DriveDreamer4D)](https://github.com/GigaAI-research/DriveDreamer4D) |
| `DeSiRe-GS` | [![arXiv](https://img.shields.io/badge/arXiv-2411.11921-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.11921)<br>DeSiRe-GS: 4D Street Gaussians for Static-Dynamic Decomposition and Surface Reconstruction for Urban Driving Scenes | CVPR 2025 | - | [![GitHub](https://img.shields.io/github/stars/chengweialan/DeSiRe-GS)](https://github.com/chengweialan/DeSiRe-GS) |
| `SplatAD` | [![arXiv](https://img.shields.io/badge/arXiv-2411.16816-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.16816)<br>SplatAD: Real-Time Lidar and Camera Rendering with 3D Gaussian Splatting for Autonomous Driving | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.zenseact.com/publications/splatad/) | [![GitHub](https://img.shields.io/github/stars/carlinds/splatad)](https://github.com/carlinds/splatad) |
| `ReconDreamer` | [![arXiv](https://img.shields.io/badge/arXiv-2411.19548-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.19548)<br>ReconDreamer: Crafting World Models for Driving Scene Reconstruction via Online Restoration | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://recondreamer.github.io/) | [![GitHub](https://img.shields.io/github/stars/GigaAI-research/ReconDreamer)](https://github.com/GigaAI-research/ReconDreamer/) |
| `FreeSim` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03566-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03566)<br>FreeSim: Toward Free-Viewpoint Camera Simulation in Driving Scenes | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drive-sim.github.io/freesim/) | - |
| `StreetCrafter` | [![arXiv](https://img.shields.io/badge/arXiv-2412.13188-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.13188)<br>StreetCrafter: Street View Synthesis with Controllable Video Diffusion Models | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://zju3dv.github.io/street_crafter/) | [![GitHub](https://img.shields.io/github/stars/zju3dv/street_crafter)](https://github.com/zju3dv/street_crafter) |
| `FlexDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2502.21093-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.21093)<br>FlexDrive: Toward Trajectory Flexibility in Driving Scene Reconstruction and Rendering | CVPR 2025 | - | - |
| `S-NeRF++` | [![arXiv](https://img.shields.io/badge/arXiv-2402.02112-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2402.02112)<br>S-NeRF++: Autonomous Driving Simulation via Neural Reconstruction and Generation | TPAMI 2025 | - | - |
| `InfiniCube` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>InfiniCube: Unbounded and Controllable Dynamic 3D Driving Scene Generation with World-Guided Video Models | ICCV 2025| [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/infinicube/) | [![GitHub](https://img.shields.io/github/stars/nv-tlabs/InfiniCube)](https://github.com/nv-tlabs/InfiniCube) |
| `DiST-4D` | [![arXiv](https://img.shields.io/badge/arXiv-2503.15208-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.15208)<br>Disentangled Spatiotemporal Diffusion with Metric Depth for 4D Driving Scene Generation | ICCV 2025 |[![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://royalmelon0505.github.io/DiST-4D/) | [![GitHub](https://img.shields.io/github/stars/royalmelon0505/dist4d)](https://github.com/royalmelon0505/dist4d) |
| `DreamDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2501.00601-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2501.00601)<br>DreamDrive: Generative 4D Scene Modeling from Street View Images | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://pointscoder.github.io/DreamDrive/) | - |
| `Uni-Gaussians` | [![arXiv](https://img.shields.io/badge/arXiv-2503.08317-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.08317)<br>Uni-Gaussians: Unifying Camera and Lidar Simulation with Gaussians for Dynamic Driving Scenarios | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://zikangyuan.github.io/UniGaussians/) | - |
| `MuDG` | [![arXiv](https://img.shields.io/badge/arXiv-2503.10604-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.10604)<br>MuDG: Taming Multi-Modal Diffusion with Gaussian Splatting for Urban Scene Reconstruction | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://heiheishuang.xyz/mudg/) | [![GitHub](https://img.shields.io/github/stars/heiheishuang/MuDG)](https://github.com/heiheishuang/MuDG) |
| `UniFuture` | [![arXiv](https://img.shields.io/badge/arXiv-2503.13587-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.13587)<br>Seeing the Future, Perceiving the Future: A Unified Driving World Model for Future Generation and Perception | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://dk-liang.github.io/UniFuture/) |[![GitHub](https://img.shields.io/github/stars/dk-liang/UniFuture)](https://github.com/dk-liang/UniFuture)|
| `SceneCrafter` | [![arXiv](https://img.shields.io/badge/arXiv-2503.18108-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.18108)<br>Unraveling the Effects of Synthetic Data on End-to-End Autonomous Driving Humanoid Robots | arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/cancaries/SceneCrafter)](https://github.com/cancaries/SceneCrafter) |
| `ReconDreamer++` | [![arXiv](https://img.shields.io/badge/arXiv-2503.18438-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.18438)<br>ReconDreamer++: Harmonizing Generative and Reconstructive Models for Driving Scene Representation | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://recondreamer-plus.github.io/) | [![GitHub](https://img.shields.io/github/stars/GigaAI-research/ReconDreamer-Plus)](https://github.com/GigaAI-research/ReconDreamer-Plus) |
| `RealEngine` | [![arXiv](https://img.shields.io/badge/arXiv-2505.16902-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.16902)<br>RealEngine: Simulating Autonomous Driving in Realistic Context | arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/fudan-zvg/RealEngine)](https://github.com/fudan-zvg/RealEngine) |
| `GeoDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2505.22421-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.22421)<br>GeoDrive: 3D Geometry-Informed Driving World Model with Precise Action Control | arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/antonioo-c/GeoDrive)](https://github.com/antonioo-c/GeoDrive) |
| `PseudoSimulation` | [![arXiv](https://img.shields.io/badge/arXiv-2506.04218-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.04218)<br>Pseudo-Simulation for Autonomous Driving | arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/autonomousvision/navsim)](https://github.com/autonomousvision/navsim) |
| `Dreamland` | [![arXiv](https://img.shields.io/badge/arXiv-2506.08006-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.08006)<br>Dreamland: Controllable World Creation with Simulator and Generative Models | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadriverse.github.io/dreamland/) | - |
||



# 3. World Modeling from Occupancy Generation

### :one: Scene Representors

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `SSD` | [![arXiv](https://img.shields.io/badge/arXiv-2301.00527-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2301.00527)<br>Diffusion Probabilistic Models for Scene-Scale 3D Categorical Data | arXiv 2023 | - | [![GitHub](https://img.shields.io/github/stars/zoomin-lee/scene-scale-diffusion)](https://github.com/zoomin-lee/scene-scale-diffusion) |
| `SemCity` | [![arXiv](https://img.shields.io/badge/arXiv-2403.07773-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.07773)<br>SemCity: Semantic Scene Generation with Triplane Diffusion | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://sglab.kaist.ac.kr/SemCity/) |[![GitHub](https://img.shields.io/github/stars/zoomin-lee/SemCity)](https://github.com/zoomin-lee/SemCity) |
| `WoVoGen` | [![arXiv](https://img.shields.io/badge/arXiv-2312.02934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.02934)<br>WoVoGen: World Volume-Aware Diffusion for Controllable Multi-Camera Driving Scene Generation | ECCV 2024 | - | [![GitHub](https://img.shields.io/github/stars/fudan-zvg/WoVoGen)](https://github.com/fudan-zvg/WoVoGen) |
| `UrbanDiff` | [![arXiv](https://img.shields.io/badge/arXiv-2403.11697-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.11697)<br>Urban Scene Diffusion through Semantic Occupancy Map | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadriverse.github.io/urbandiff/) | - |
| `DrivingSphere` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>DrivingSphere: Building A High-Fidelity 4D World for Closed-Loop Simulation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yanty123.github.io/DrivingSphere/) | [![GitHub](https://img.shields.io/github/stars/yanty123/DrivingSphere)](https://github.com/yanty123/DrivingSphere) |
| `UniScene` | [![arXiv](https://img.shields.io/badge/arXiv-2412.05435-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.05435)<br>UniScene: Unified Occupancy-Centric Driving Scene Generation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://arlo0o.github.io/uniscene/) | [![GitHub](https://img.shields.io/github/stars/Arlo0o/UniScene-Unified-Occupancy-centric-Driving-Scene-Generation)](https://github.com/Arlo0o/UniScene-Unified-Occupancy-centric-Driving-Scene-Generation) |
| `OccScene` | [![arXiv](https://img.shields.io/badge/arXiv-2412.11183-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.11183)<br>OccScene: Semantic Occupancy-Based Cross-Task Mutual Learning for 3D Scene Generation | arXiv 2024 | - | - |
| `InfiniCube` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>InfiniCube: Unbounded and Controllable Dynamic 3D Driving Scene Generation with World-Guided Video Models | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/infinicube/) | [![GitHub](https://img.shields.io/github/stars/nv-tlabs/InfiniCube)](https://github.com/nv-tlabs/InfiniCube) |
| `Control-3D-Scene` | [![arXiv](https://img.shields.io/badge/arXiv-2503.07152-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.07152)<br>Controllable 3D Outdoor Scene Generation via Scene Graphs | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yuheng.ink/project-page/control-3d-scene/) | [![GitHub](https://img.shields.io/github/stars/yuhengliu02/control-3d-scene)](https://github.com/yuhengliu02/control-3d-scene) |
| `X-Scene` | [![arXiv](https://img.shields.io/badge/arXiv-2506.13558-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.13558)<br>X-Scene: Large-Scale Driving Scene Generation with High Fidelity and Flexible Controllability | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://x-scene.github.io/) | [![GitHub](https://img.shields.io/github/stars/yuyang-cloud/X-Scene)](https://github.com/yuyang-cloud/X-Scene) |
||



### :two: Occupancy Forecasters

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `Emergent-Occ` | [![arXiv](https://img.shields.io/badge/arXiv-2210.01917-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2210.01917)<br>Differentiable Raycasting for Self-supervised Occupancy Forecasting | ECCV 2022 | - | [![GitHub](https://img.shields.io/github/stars/tarashakhurana/emergent-occ-forecasting)](https://github.com/tarashakhurana/emergent-occ-forecasting) |
| `FF4D` | [![arXiv](https://img.shields.io/badge/arXiv-2302.13130-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2302.13130)<br>Point Cloud Forecasting as a Proxy for 4D Occupancy Forecasting | CVPR 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://www.cs.cmu.edu/~tkhurana/ff4d/index.html) | [![GitHub](https://img.shields.io/github/stars/tarashakhurana/4d-occ-forecasting)](https://github.com/tarashakhurana/4d-occ-forecasting) |
| `UniWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2308.07234-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2308.07234)<br>UniWorld: Autonomous Driving Pre-Training via World Models | arXiv 2023 | - | - |
| `UniScene` | [![arXiv](https://img.shields.io/badge/arXiv-2305.18829-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2305.18829)<br>UniScene: Multi-Camera Unified Pre-Training via 3D Scene Reconstruction for Autonomous Driving | arXiv 2023 | - | [![GitHub](https://img.shields.io/github/stars/chaytonmin/UniScene)](https://github.com/chaytonmin/UniScene) |
| `OccWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16038-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.16038)<br>OccWorld: Learning A 3D Occupancy World Model for Autonomous Driving | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wzzheng.net/OccWorld/) | [![GitHub](https://img.shields.io/github/stars/wzzheng/OccWorld)](https://github.com/wzzheng/OccWorld) |
| `Cam4DOcc` | [![arXiv](https://img.shields.io/badge/arXiv-2311.17663-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.17663)<br>Cam4DOcc: Benchmark for Camera-Only 4D Occupancy Forecasting in Autonomous Driving Applications | CVPR 2024 | - | [![GitHub](https://img.shields.io/github/stars/haomo-ai/Cam4DOcc)](https://github.com/haomo-ai/Cam4DOcc) |
| `DriveWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2405.04390-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.04390)<br>DriveWorld: 4D Pre-Trained Scene Understanding via World Models for Autonomous Driving | CVPR 2024 | - | - |
| `OccSora` | [![arXiv](https://img.shields.io/badge/arXiv-2405.20337-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.20337)<br>OccSora: 4D Occupancy Generation Models as World Simulators for Autonomous Driving | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wzzheng.net/OccSora/) | [![GitHub](https://img.shields.io/github/stars/wzzheng/OccWorld)](https://github.com/wzzheng/OccSora) |
| `UnO` | [![arXiv](https://img.shields.io/badge/arXiv-2406.08691-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.08691)<br>UnO: Unsupervised Occupancy Fields for Perception and Forecasting | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://waabi.ai/uno/) | - |
| `LOPR` | [![arXiv](https://img.shields.io/badge/arXiv-2407.21126-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.21126)<br>Self-Supervised Multi-Future Occupancy Forecasting for Autonomous Driving | arXiv 2024 | - | - |
| `FSF-Net` | [![arXiv](https://img.shields.io/badge/arXiv-2409.15841-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.15841)<br>FSF-Net: Enhance 4D Occupancy Forecasting with Coarse BEV Scene Flow for Autonomous Driving | arXiv 2024 | - | - |
| `OccLLaMA` | [![arXiv](https://img.shields.io/badge/arXiv-2409.03272-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.03272)<br>OccLLaMA: An Occupancy-Language-Action Generative World Model for Autonomous Driving | arXiv 2024 | -| - |
| `DOME` | [![arXiv](https://img.shields.io/badge/arXiv-2410.10429-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.10429)<br>DOME: Taming Diffusion Model into High-Fidelity Controllable Occupancy World Model | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://gusongen.github.io/DOME) | [![GitHub](https://img.shields.io/github/stars/gusongen/DOME)](https://github.com/gusongen/DOME) |
| `GaussianAD` | [![arXiv](https://img.shields.io/badge/arXiv-2412.10371-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.10371)<br>GaussianAD: Gaussian-Centric End-to-End Autonomous Driving | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wzzheng.net/GaussianAD) | [![GitHub](https://img.shields.io/github/stars/wzzheng/GaussianAD)](https://github.com/wzzheng/GaussianAD) |
| `DFIT-OccWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2412.13772-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.13772)<br>An Efficient Occupancy World Model via Decoupled Dynamic Flow and Image-Assisted Training | arXiv 2024 | - | - |
| `Drive-OccWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2408.14197-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2408.14197)<br>Driving in the Occupancy World: Vision-Centric 4D Occupancy Forecasting and Planning via World Models for Autonomous Driving | AAAI 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drive-occworld.github.io/) | [![GitHub](https://img.shields.io/github/stars/yuyang-cloud/Drive-OccWorld)](https://github.com/yuyang-cloud/Drive-OccWorld) |
| `PreWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2502.07309-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.07309)<br>Semi-Supervised Vision-Centric 3D Occupancy World Model for Autonomous Driving | ICLR 2025 | - | [![GitHub](https://img.shields.io/github/stars/getterupper/PreWorld)](https://github.com/getterupper/PreWorld) |
| `OccProphet` | [![arXiv](https://img.shields.io/badge/arXiv-2502.15180-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.15180)<br>OccProphet: Pushing Efficiency Frontier of Camera-Only 4D Occupancy Forecasting with Observer-Forecaster-Refiner Framework | ICLR 2025 | - | [![GitHub](https://img.shields.io/github/stars/JLChen-C/OccProphet)](https://github.com/JLChen-C/OccProphet) |
| `RenderWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2409.11356-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.11356)<br>RenderWorld: World Model with Self-Supervised 3D Label | ICRA 2025 | - | - |
| `Occ-LLM` | [![arXiv](https://img.shields.io/badge/arXiv-2502.06419-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.06419)<br>Occ-LLM: Enhancing Autonomous Driving with Occupancy-Based Large Language Models | ICRA 2025 | - | - |
| `EfficientOCF` | [![arXiv](https://img.shields.io/badge/arXiv-2411.14169-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.14169)<br>Spatiotemporal Decoupling for Efficient Vision-Based Occupancy Forecasting | CVPR 2025 | - | - |
| `DIO` | [![arXiv](https://img.shields.io/badge/arXiv-DIO-b31b1b?style=flat-square&logo=arxiv)](https://openaccess.thecvf.com/content/CVPR2025/papers/Diehl_DIO_Decomposable_Implicit_4D_Occupancy-Flow_World_Model_CVPR_2025_paper.pdf)<br>DIO: Decomposable Implicit 4D Occupancy-Flow World Model | CVPR 2025 | - | - |
| `T³Former` | [![arXiv](https://img.shields.io/badge/arXiv-2503.07338-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.07338)<br>Temporal Triplane Transformers as Occupancy World Models | arXiv 2025 | - | - |
| `UniOcc` | [![arXiv](https://img.shields.io/badge/arXiv-2503.24381-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.24381)<br>UniOcc: A Unified Benchmark for Occupancy Forecasting and Prediction in Autonomous Driving | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://huggingface.co/datasets/tasl-lab/uniocc) | [![GitHub](https://img.shields.io/github/stars/tasl-lab/UniOcc)](https://github.com/tasl-lab/UniOcc) |
| `I²World` | [![arXiv](https://img.shields.io/badge/arXiv-2507.09144-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2507.09144)<br>I²-World: Intra-Inter Tokenization for Efficient Dynamic 4D Scene Forecasting | ICCV 2025 | - | [![GitHub](https://img.shields.io/github/stars/lzzzzzm/II-World)](https://github.com/lzzzzzm/II-World) |
| `COME` | [![arXiv](https://img.shields.io/badge/arXiv-2506.13260-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.13260)<br>COME: Adding Scene-Centric Forecasting Control to Occupancy World Model | arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/synsin0/COME)](https://github.com/synsin0/COME) |
||



### :three: Autoregressive Simulators

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `SemCity` | [![arXiv](https://img.shields.io/badge/arXiv-2403.07773-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.07773)<br>SemCity: Semantic Scene Generation with Triplane Diffusion | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://sglab.kaist.ac.kr/SemCity/) |[![GitHub](https://img.shields.io/github/stars/zoomin-lee/SemCity)](https://github.com/zoomin-lee/SemCity) |
| `XCube` | [![arXiv](https://img.shields.io/badge/arXiv-2312.03806-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.03806)<br>XCube: Large-Scale 3D Generative Modeling using Sparse Voxel Hierarchies | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/xcube/) | [![GitHub](https://img.shields.io/github/stars/nv-tlabs/XCube)](https://github.com/nv-tlabs/XCube) |
| `PDD` | [![arXiv](https://img.shields.io/badge/arXiv-2311.12085-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.12085)<br>Pyramid Diffusion for Fine 3D Large Scene Generation | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yuheng.ink/project-page/pyramid-discrete-diffusion) | [![GitHub](https://img.shields.io/github/stars/yuhengliu02/pyramid-discrete-diffusion)](https://github.com/yuhengliu02/pyramid-discrete-diffusion) |
| `OccSora` | [![arXiv](https://img.shields.io/badge/arXiv-2405.20337-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.20337)<br>OccSora: 4D Occupancy Generation Models as World Simulators for Autonomous Driving | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wzzheng.net/OccSora/) | [![GitHub](https://img.shields.io/github/stars/wzzheng/OccWorld)](https://github.com/wzzheng/OccSora) |
| `DynamicCity` | [![arXiv](https://img.shields.io/badge/arXiv-2410.18084-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.18084)<br>DynamicCity: Large-Scale 4D Occupancy Generation from Dynamic Scenes | ICLR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://dynamic-city.github.io/) | [![GitHub](https://img.shields.io/github/stars/3DTopia/DynamicCity)](https://github.com/3DTopia/DynamicCity) |
| `DrivingSphere` | [![arXiv](https://img.shields.io/badge/arXiv-2411.11252-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.11252)<br>DrivingSphere: Building A High-Fidelity 4D World for Closed-Loop Simulation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yanty123.github.io/DrivingSphere/) | [![GitHub](https://img.shields.io/github/stars/yanty123/DrivingSphere)](https://github.com/yanty123/DrivingSphere) |
| `InfiniCube` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>InfiniCube: Unbounded and Controllable Dynamic 3D Driving Scene Generation with World-Guided Video Models | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/infinicube/) | [![GitHub](https://img.shields.io/github/stars/nv-tlabs/InfiniCube)](https://github.com/nv-tlabs/InfiniCube) |
| `X-Scene` | [![arXiv](https://img.shields.io/badge/arXiv-2506.13558-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.13558)<br>X-Scene: Large-Scale Driving Scene Generation with High Fidelity and Flexible Controllability | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://x-scene.github.io/) | [![GitHub](https://img.shields.io/github/stars/yuyang-cloud/X-Scene)](https://github.com/yuyang-cloud/X-Scene) |
| `PrITTI` | [![arXiv](https://img.shields.io/badge/arXiv-2506.19117-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.19117)<br>PrITTI: Primitive-Based Generation of Controllable and Editable 3D Semantic Scenes | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://raniatze.github.io/pritti/) | [![GitHub](https://img.shields.io/github/stars/avg-dev/PrITTI)](https://github.com/avg-dev/PrITTI) |



# 4. World Modeling from LiDAR Generation

### :one: Data Engines

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `DUSty` | [![arXiv](https://img.shields.io/badge/arXiv-2102.11952-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2102.11952)<br>Learning to Drop Points for LiDAR Scan Synthesis | IROS 2021 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://kazuto1011.github.io/dusty-gan/) | [![GitHub](https://img.shields.io/github/stars/kazuto1011/dusty-gan)](https://github.com/kazuto1011/dusty-gan) |
| `LiDARGen` | [![arXiv](https://img.shields.io/badge/arXiv-2209.03954-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2209.03954)<br>Learning to Generate Realistic LiDAR Point Clouds | ECCV 2022 | - | [![GitHub](https://img.shields.io/github/stars/vzyrianov/lidargen)](https://github.com/vzyrianov/lidargen) |
| `DUSty v2` | [![arXiv](https://img.shields.io/badge/arXiv-2210.11750-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2210.11750)<br>Generative Range Imaging for Learning Scene Priors of 3D LiDAR Data | WACV 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://kazuto1011.github.io/dusty-gan-v2/) | [![GitHub](https://img.shields.io/github/stars/kazuto1011/dusty-gan-v2)](https://github.com/kazuto1011/dusty-gan-v2) |
| `UltraLiDAR` | [![arXiv](https://img.shields.io/badge/arXiv-2311.01448-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.01448)<br>UltraLiDAR: Learning Compact Representations for LiDAR Completion and Generation | CVPR 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://waabi.ai/ultralidar/) | - |
| `Copilot4D` | [![arXiv](https://img.shields.io/badge/arXiv-2311.01017-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.01017)<br>Copilot4D: Learning Unsupervised World Models for Autonomous Driving via Discrete Diffusion | ICLR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://waabi.ai/research/copilot-4d) | - |
| `R2DM` | [![arXiv](https://img.shields.io/badge/arXiv-2309.09256-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2309.09256)<br>LiDAR Data Synthesis with Denoising Diffusion Probabilistic Models | ICRA 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://kazuto1011.github.io/r2dm) | [![GitHub](https://img.shields.io/github/stars/kazuto1011/r2dm)](https://github.com/kazuto1011/r2dm) |
| `ViDAR` | [![arXiv](https://img.shields.io/badge/arXiv-2312.17655-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.17655)<br>Visual Point Cloud Forecasting enables Scalable Autonomous Driving | CVPR 2024 | - | [![GitHub](https://img.shields.io/github/stars/OpenDriveLab/ViDAR)](https://github.com/OpenDriveLab/ViDAR) |
| `LiDiff` | [![arXiv](https://img.shields.io/badge/arXiv-2403.13470-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.13470)<br>Scaling Diffusion Models to Real-World 3D LiDAR Scene Completion | CVPR 2024 | - | [![GitHub](https://img.shields.io/github/stars/PRBonn/LiDiff)](https://github.com/PRBonn/LiDiff) |
| `LiDM` | [![arXiv](https://img.shields.io/badge/arXiv-2404.00815-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2404.00815)<br>Towards Realistic Scene Generation with LiDAR Diffusion Models | CVPR 2024 | - | [![GitHub](https://img.shields.io/github/stars/hancyran/LiDAR-Diffusion)](https://github.com/hancyran/LiDAR-Diffusion/tree/8416ddbbda881553088109a66badf71ff11999e0) |
| `RangeLDM` | [![arXiv](https://img.shields.io/badge/arXiv-2403.10094-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.10094)<br>RangeLDM: Fast Realistic LiDAR Point Cloud Generation | ECCV 2024 | - | [![GitHub](https://img.shields.io/github/stars/WoodwindHu/RangeLDM)](https://github.com/WoodwindHu/RangeLDM) |
| `Text2LiDAR` | [![arXiv](https://img.shields.io/badge/arXiv-2407.19628-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.19628)<br>Text2LiDAR: Text-Guided LiDAR Point Cloud Generation via Equirectangular Transformer | ECCV 2024 | - | [![GitHub](https://img.shields.io/github/stars/wuyang98/Text2LiDAR)](https://github.com/wuyang98/Text2LiDAR) |
| `LiDARGRIT` | [![arXiv](https://img.shields.io/badge/arXiv-2404.05505-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2404.05505)<br>Taming Transformers for Realistic LiDAR Point Cloud Generation | arXiv 2024 | - | [![GitHub](https://img.shields.io/github/stars/hamedhaghighi/LidarGRIT)](https://github.com/hamedhaghighi/LidarGRIT) | 
| `BEVWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2407.05679-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.05679)<br>BEVWorld: A Multimodal World Simulator for Autonomous Driving via Scene-Level BEV Latents | arXiv 2024 | - | [![GitHub](https://img.shields.io/github/stars/zympsyche/BevWorld)](https://github.com/zympsyche/BevWorld) | 
| `SDS` | [![arXiv](https://img.shields.io/badge/arXiv-2410.11628-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.11628)<br>Simultaneous Diffusion Sampling for Conditional LiDAR Generation | arXiv 2024 | - | - |
| `DiffSSC` | [![arXiv](https://img.shields.io/badge/arXiv-2409.18092-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.18092)<br>DiffSSC: Semantic LiDAR Scan Completion using Denoising Diffusion Probabilistic Models | IROS 2025 | - | - |
| `HoloDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2412.01407-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.01407)<br>HoloDrive: Holistic 2D-3D Multi-Modal Street Scene Generation for Autonomous Driving | arXiv 2024 | - | - |
| `LOGen` | [![arXiv](https://img.shields.io/badge/arXiv-2412.07385-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.07385)<br>LOGen: Toward LiDAR Object Generation by Point Diffusion | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://nerminsamet.github.io/logen/) | [![GitHub](https://img.shields.io/github/stars/valeoai/LOGen)](https://github.com/valeoai/LOGen) |
| `OLiDM` | [![arXiv](https://img.shields.io/badge/arXiv-2412.17226-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.17226)<br>OLiDM: Object-Aware LiDAR Diffusion Models for Autonomous Driving | AAAI 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yanty123.github.io/OLiDM) | [![GitHub](https://img.shields.io/github/stars/yanty123/OLiDM)](https://github.com/yanty123/OLiDM) |  
| `X-Drive` | [![arXiv](https://img.shields.io/badge/arXiv-2411.01123-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.01123)<br>X-Drive: Cross-Modality Consistent Multi-Sensor Data Synthesis for Driving Scenarios | ICLR 2025 | - | [![GitHub](https://img.shields.io/github/stars/yichen928/X-Drive)](https://github.com/yichen928/X-Drive) |
| `LidarDM` | [![arXiv](https://img.shields.io/badge/arXiv-2404.02903-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2404.02903)<br>LidarDM: Generative LiDAR Simulation in a Generated World | ICRA 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://zyrianov.org/lidardm/) | [![GitHub](https://img.shields.io/github/stars/vzyrianov/lidardm)](https://github.com/vzyrianov/lidardm) |  
| `LiDAR-EDIT` | [![arXiv](https://img.shields.io/badge/arXiv-2412.00592-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.00592)<br>LiDAR-EDIT: LiDAR Data Generation by Editing the Object Layouts in Real-World Scenes | ICRA 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://sites.google.com/view/lidar-edit) | [![GitHub](https://img.shields.io/github/stars/HoAdrian/ICRA2025_lidar_edit)](https://github.com/HoAdrian/ICRA2025_lidar_edit) | 
| `R2Flow` | [![arXiv](https://img.shields.io/badge/arXiv-2412.02241-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.02241)<br>Fast LiDAR Data Generation with Rectified Flows | ICRA 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://kazuto1011.github.io/r2flow/) | [![GitHub](https://img.shields.io/github/stars/kazuto1011/r2flow)](https://github.com/kazuto1011/r2flow) |
| `WeatherGen` | [![arXiv](https://img.shields.io/badge/arXiv-2504.13561-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2504.13561)<br>WeatherGen: A Unified Diverse Weather Generator for LiDAR Point Clouds via Spider Mamba Diffusion | CVPR 2025 | - | [![GitHub](https://img.shields.io/github/stars/wuyang98/weathergen)](https://github.com/wuyang98/weathergen) |
| `LiDPM` | [![arXiv](https://img.shields.io/badge/arXiv-2504.17791-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2504.17791)<br>LiDPM: Rethinking Point Diffusion for Lidar Scene Completion | IV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://astra-vision.github.io/LiDPM/) | [![GitHub](https://img.shields.io/github/stars/astra-vision/LiDPM)](https://github.com/astra-vision/LiDPM) |
| `HERMES` | [![arXiv](https://img.shields.io/badge/arXiv-2501.14729-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2501.14729)<br>HERMES: A Unified Self-Driving World Model for Simultaneous 3D Scene Understanding and Generation | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://lmd0311.github.io/HERMES/) | [![GitHub](https://img.shields.io/github/stars/LMD0311/HERMES)](https://github.com/LMD0311/HERMES) |
| `SuperPC` | [![arXiv](https://img.shields.io/badge/arXiv-2503.14558-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.14558)<br>SuperPC: A Single Diffusion Model for Point Cloud Completion, Upsampling, Denoising, and Colorization | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://sairlab.org/superpc/) | - |
| `3DiSS` | [![arXiv](https://img.shields.io/badge/arXiv-2503.21449-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.21449)<br>Towards Generating Realistic 3D Semantic Training Data for Autonomous Driving |  arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/PRBonn/3DiSS)](https://github.com/PRBonn/3DiSS) |
| `Distill-DPO` | [![arXiv](https://img.shields.io/badge/arXiv-2504.11447-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2504.11447)<br>Diffusion Distillation With Direct Preference Optimization For Efficient 3D LiDAR Scene Completion |  arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/happyw1nd/DistillationDPO)](https://github.com/happyw1nd/DistillationDPO) |
| `DriveX` | [![arXiv](https://img.shields.io/badge/arXiv-2505.19239-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.19239)<br>DriveX: Omni Scene Modeling for Learning Generalizable World Knowledge in Autonomous Driving |  arXiv 2025 | - | - |
| `OpenDWM` | [![arXiv](https://img.shields.io/badge/arXiv-2412.02241-b31b1b?style=flat-square&logo=arxiv)](https://github.com/SenseTime-FVG/OpenDWM)<br>OpenDWM: Open Driving World Models |  arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/SenseTime-FVG/OpenDWM)](https://github.com/SenseTime-FVG/OpenDWM) |
| `SPIRAL` | [![arXiv](https://img.shields.io/badge/arXiv-2505.22643-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.22643)<br>SPIRAL: Semantic-Aware Progressive LiDAR Scene Generation |  arXiv 2025 | - | - |
| `La La LiDAR` | [![arXiv](https://img.shields.io/badge/arXiv-2508.03691-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2508.03691)<br>La La LiDAR: Large-Scale Layout Generation from LiDAR Data |  arXiv 2025 | - | - |
| `Veila` | [![arXiv](https://img.shields.io/badge/arXiv-2508.03690-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2508.03690)<br>Veila: Panoramic LiDAR Generation from a Monocular RGB Image |  arXiv 2025 | - | - |
| `LiDARCrafter` | [![arXiv](https://img.shields.io/badge/arXiv-2508.03692-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2508.03692)<br>LiDARCrafter: Dynamic 4D World Modeling from LiDAR Sequences | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://lidarcrafter.github.io/) | [![GitHub](https://img.shields.io/github/stars/lidarcrafter/toolkit)](https://github.com/lidarcrafter/toolkit) |



### :two: Action Forecasters

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `Copilot4D` | [![arXiv](https://img.shields.io/badge/arXiv-2311.01017-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.01017)<br>Copilot4D: Learning Unsupervised World Models for Autonomous Driving via Discrete Diffusion | ICLR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://waabi.ai/research/copilot-4d) | - |
| `ViDAR` | [![arXiv](https://img.shields.io/badge/arXiv-2312.17655-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.17655)<br>Visual Point Cloud Forecasting enables Scalable Autonomous Driving | CVPR 2024 | - | [![GitHub](https://img.shields.io/github/stars/OpenDriveLab/ViDAR)](https://github.com/OpenDriveLab/ViDAR) |
| `BEVWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2407.05679-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.05679)<br>BEVWorld: A Multimodal World Simulator for Autonomous Driving via Scene-Level BEV Latents | arXiv 2024 | - | [![GitHub](https://img.shields.io/github/stars/zympsyche/BevWorld)](https://github.com/zympsyche/BevWorld) | 
| `HERMES` | [![arXiv](https://img.shields.io/badge/arXiv-2501.14729-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2501.14729)<br>HERMES: A Unified Self-Driving World Model for Simultaneous 3D Scene Understanding and Generation | ICCV 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://lmd0311.github.io/HERMES/) | [![GitHub](https://img.shields.io/github/stars/LMD0311/HERMES)](https://github.com/LMD0311/HERMES) |
| `DriveX` | [![arXiv](https://img.shields.io/badge/arXiv-2505.19239-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.19239)<br>DriveX: Omni Scene Modeling for Learning Generalizable World Knowledge in Autonomous Driving |  arXiv 2025 | - | - |


### :three: Autoregressive Simulators

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `HoloDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2412.01407-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.01407)<br>HoloDrive: Holistic 2D-3D Multi-Modal Street Scene Generation for Autonomous Driving | arXiv 2024 | - | - |
| `LidarDM` | [![arXiv](https://img.shields.io/badge/arXiv-2404.02903-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2404.02903)<br>LidarDM: Generative LiDAR Simulation in a Generated World | ICRA 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://zyrianov.org/lidardm/) | [![GitHub](https://img.shields.io/github/stars/vzyrianov/lidardm)](https://github.com/vzyrianov/lidardm) |  
| `OpenDWM` | [![arXiv](https://img.shields.io/badge/arXiv-2412.02241-b31b1b?style=flat-square&logo=arxiv)](https://github.com/SenseTime-FVG/OpenDWM)<br>OpenDWM: Open Driving World Models |  arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/SenseTime-FVG/OpenDWM)](https://github.com/SenseTime-FVG/OpenDWM) |
| `LiDARCrafter` | [![arXiv](https://img.shields.io/badge/arXiv-2508.03692-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2508.03692)<br>LiDARCrafter: Dynamic 4D World Modeling from LiDAR Sequences | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://lidarcrafter.github.io/) | [![GitHub](https://img.shields.io/github/stars/lidarcrafter/toolkit)](https://github.com/lidarcrafter/toolkit) |



# 5. Applications

### :one: Autonomous Driving

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `OccSora` | [![arXiv](https://img.shields.io/badge/arXiv-2405.20337-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.20337)<br>OccSora: 4D Occupancy Generation Models as World Simulators for Autonomous Driving | arXiv 2024 | - | [![GitHub](https://img.shields.io/github/stars/wzzheng/OccSora)](https://github.com/wzzheng/OccSora) |
| `DFIT-OccWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2412.13772-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.13772)<br>An Efficient Occupancy World Model via Decoupled Dynamic Flow and Image-Assisted Training | arXiv 2024 | - | - |
| `LiDARCrafter` | [![arXiv](https://img.shields.io/badge/arXiv-2508.03692-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2508.03692)<br>LiDARCrafter: Dynamic 4D World Modeling from LiDAR Sequences | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://lidarcrafter.github.io/) | [![GitHub](https://img.shields.io/github/stars/lidarcrafter/toolkit)](https://github.com/lidarcrafter/toolkit) |
| `UniSim` | [![arXiv](https://img.shields.io/badge/arXiv-2308.01898-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2308.01898)<br>UniSim: A Neural Closed-Loop Sensor Simulator | CVPR 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://waabi.ai/research/unisim) | - |
| `Panacea` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.16813)<br>Panacea: Panoramic and Controllable Video Generation for Autonomous Driving | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://panacea-ad.github.io/) | [![GitHub](https://img.shields.io/github/stars/wenyuqing/panacea)](https://github.com/wenyuqing/panacea) |
| `Delphi` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.01349)<br>Unleashing Generalization of End-to-End Autonomous Driving with Controllable Long Video Generation | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://westlake-autolab.github.io/delphi.github.io/) | [![GitHub](https://img.shields.io/github/stars/westlake-autolab/Delphi)](https://github.com/westlake-autolab/Delphi) |
| `DriveDreamer-2` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/pdf/2403.06845)<br>DriveDreamer-2: LLM-Enhanced World Models for Diverse Driving Video Generation | AAAI 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)]() | [![GitHub](https://img.shields.io/github/stars/f1yfisher/DriveDreamer2)](https://github.com/f1yfisher/DriveDreamer2) |
| `Panacea+` | [![arXiv](https://img.shields.io/badge/arXiv-2408.07605-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2408.07605)<br>Panacea+: Panoramic and Controllable Video Generation for Autonomous Driving | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://panacea-ad.github.io/) | - |
| `MiLA` | [![arXiv](https://img.shields.io/badge/arXiv-2503.15875-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.15875)<br>MiLA: Multi-View Intensive-Fidelity Long-Term Video Generation World Model for Autonomous Driving | arXiv 2025 | - | [![GitHub](https://img.shields.io/github/stars/xiaomi-mlab/mila.github.io)](https://github.com/xiaomi-mlab/mila.github.io) |
| `GAIA-2` | [![arXiv](https://img.shields.io/badge/arXiv-2503.20523-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.20523)<br>GAIA-2: A Controllable Multi-View Generative World Model for Autonomous Driving | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wayve.ai/thinking/gaia-2) | - |


### :two: Robotics

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `RoboDreamer` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)]()<br>RoboDreamer: Learning Compositional World Models for Robot Imagination | Arxiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://robovideo.github.io/) | [![GitHub](https://img.shields.io/github/stars/UMass-Embodied-AGI/robodreamer)](https://github.com/UMass-Embodied-AGI/robodreamer) |
| `BEHAVIOR` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.05652v1)<br>BEHAVIOR Robot Suite: Streamlining Real-World Whole-Body Manipulation for Everyday Household Activities | CoRL 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://behavior-robot-suite.github.io/) | [![GitHub](https://img.shields.io/github/stars/behavior-robot-suite/brs-algo)](https://github.com/behavior-robot-suite/brs-algo) |
| `Habitat 2.0` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)]()<br>Habitat 2.0: Training Home Assistants to Rearrange their Habitat | arXiv 2021 | - | - |
| `FMR` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)]()<br>Foundation Models in Robotics: Applications, Challenges, and the Future | IJRR 2024 | - | [![GitHub](https://img.shields.io/github/stars/robotics-survey/Awesome-Robotics-Foundation-Models)](https://github.com/robotics-survey/Awesome-Robotics-Foundation-Models) |
| `VLMPS` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)]()<br>Visual Language Maps for Robot Navigation | ICRA 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://vlmaps.github.io/) | [![GitHub](https://img.shields.io/github/stars/vlmaps/vlmaps)](https://github.com/vlmaps/vlmaps.git) |


### :three: Video Games & XR

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `ILVE` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://doi.org/10.1145/3582437.3587208)<br>Interactive Latent Variable Evolution for the Generation of Minecraft Structures | ICFDG 2021 | - | - |
| `ProcTHOR` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://proceedings.neurips.cc/paper_files/paper/2022/hash/27c546ab1e4f1d7d638e6a8dfbad9a07-Abstract-Conference.html)<br>ProcTHOR: Large-Scale Embodied AI Using Procedural Generation | NeurIPS 2022 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://procthor.allenai.org/) | [![GitHub](https://img.shields.io/github/stars/allenai/procthor)](https://github.com/allenai/procthor) |
| `WorldGPT` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://doi.org/10.1145/3582437.3587208)<br>WorldGPT: Empowering LLM as Multimodal World Model | ACM MM 2024 | - | [![GitHub](https://img.shields.io/github/stars/DCDmllm/WorldGPT)](https://github.com/DCDmllm/WorldGPT) |
| `Text2World` | [![arXiv](https://img.shields.io/badge/arXiv-2502.13092-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.13092)<br>Text2World: Benchmarking Large Language Models for Symbolic World Model Generation | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://text-to-world.github.io/) | [![GitHub](https://img.shields.io/github/stars/Aaron617/text2world)](https://github.com/Aaron617/text2world) |
| `Hunyuan3D 1.0` | [![arXiv](https://img.shields.io/badge/arXiv-2411.02293-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.02293)<br>Hunyuan3D 1.0: A Unified Framework for Text-to-3D and Image-to-3D Generation | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://3d.hunyuan.tencent.com) | [![GitHub](https://img.shields.io/github/stars/Tencent-Hunyuan/Hunyuan3D-1)](https://github.com/Tencent-Hunyuan/Hunyuan3D-1) |
| `Hunyuan3D 2.0` | [![arXiv](https://img.shields.io/badge/arXiv-2501.12202-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2501.12202)<br>Hunyuan3D 2.0: Scaling Diffusion Models for High Resolution Textured 3D Assets Generation | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://3d.hunyuan.tencent.com) | [![GitHub](https://img.shields.io/github/stars/Tencent-Hunyuan/Hunyuan3D-2)](https://github.com/Tencent-Hunyuan/Hunyuan3D-2) |
| `Hunyuan3D 2.1` | [![arXiv](https://img.shields.io/badge/arXiv-2506.15442-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.15442)<br>Hunyuan3D 2.1: From Images to High-Fidelity 3D Assets with Production-Ready PBR Material | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://3d.hunyuan.tencent.com) | [![GitHub](https://img.shields.io/github/stars/Tencent-Hunyuan/Hunyuan3D-2.1)](https://github.com/Tencent-Hunyuan/Hunyuan3D-2.1) |
| `Hunyuan3D 2.5` | [![arXiv](https://img.shields.io/badge/arXiv-2506.16504-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.16504)<br>Hunyuan3D 2.5: Towards High-Fidelity 3D Assets Generation with Ultimate Details | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://3d.hunyuan.tencent.com) | [![GitHub](https://img.shields.io/github/stars/Tencent-Hunyuan/Hunyuan3D-2)](https://github.com/Tencent-Hunyuan/Hunyuan3D-2) |
| `Hunyuan-GameCraft` | [![arXiv](https://img.shields.io/badge/arXiv-2506.17201-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.17201)<br>Hunyuan-GameCraft: High-dynamic Interactive Game Video Generation with Hybrid History Condition | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://hunyuan-gamecraft.github.io/) | [![GitHub](https://img.shields.io/github/stars/Tencent-Hunyuan/Hunyuan-GameCraft-1.0)](https://github.com/Tencent-Hunyuan/Hunyuan-GameCraft-1.0) |
| `HunyuanWorld 1.0` | [![arXiv](https://img.shields.io/badge/arXiv-2507.21809-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2507.21809)<br>HunyuanWorld 1.0: Generating Immersive, Explorable, and Interactive 3D Worlds from Words or Pixels | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://3d.hunyuan.tencent.com/sceneTo3D) | [![GitHub](https://img.shields.io/github/stars/Tencent-Hunyuan/HunyuanWorld-1.0)](https://github.com/Tencent-Hunyuan/HunyuanWorld-1.0) |
| `MGVQ` | [![arXiv](https://img.shields.io/badge/arXiv-2507.07997-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2507.07997)<br>MGVQ: Could VQ-VAE Beat VAE? A Generalizable Tokenizer with Multi-Group Quantization | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)]() | [![GitHub](https://img.shields.io/github/stars/MKJia/MGVQ)](https://github.com/MKJia/MGVQ) |


### :four: Digital Twins

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `DynamicCity` | [![arXiv](https://img.shields.io/badge/arXiv-2410.18084-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.18084)<br>DynamicCity: Large-Scale 4D Occupancy Generation from Dynamic Scenes | ICLR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://dynamic-city.github.io/) | [![GitHub](https://img.shields.io/github/stars/3DTopia/DynamicCity)](https://github.com/3DTopia/DynamicCity) |
| `UrbanScene3D` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/pdf/2107.04286)<br>Capturing, Reconstructing, and Simulating: the UrbanScene3D Datase | ECCV 2022 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://vcc.tech/UrbanScene3D) | [![GitHub](https://img.shields.io/github/stars/Linxius/UrbanScene3D)](https://github.com/Linxius/UrbanScene3D) |
| `GaussianCity` | [![arXiv](https://img.shields.io/badge/arXiv-2406.06526-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.06526v2)<br>GaussianCity: Generative Gaussian Splatting for Unbounded 3D City Generation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://www.codefactor.io/repository/github/hzxie/GaussianCity) | [![GitHub](https://img.shields.io/github/stars/hzxie/GaussianCity)](https://github.com/hzxie/GaussianCity) |
| `UrbanWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2407.11965-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.11965)<br>UrbanWorld: An Urban World Model for 3D City Generation | Arxiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)]() | [![GitHub](https://img.shields.io/github/stars/Urban-World/UrbanWorld)](https://github.com/Urban-World/UrbanWorld) |
| `SceneDiffuser++` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://openaccess.thecvf.com/content/CVPR2025/papers/Tan_SceneDiffuser_City-Scale_Traffic_Simulation_via_a_Generative_World_Model_CVPR_2025_paper.pdf)<br>SceneDiffuser++: City-Scale Traffic Simulation via a Generative World Model | CVPR 2025 |- | - |




# 6. Other Resources

### Workshops
- [`CVPR 2025 Workshop & Challenge | OpenDriveLab`](https://opendrivelab.com/challenge2025/#1x-wm) Track: World Model.
- [`World Model Bench @ CVPR'25`](https://worldmodelbench.github.io/) WorldModelBench: The 1st Workshop on Benchmarking World Models
- [`CVPR 2024 Workshop & Challenge | OpenDriveLab`](https://opendrivelab.com/challenge2024/#predictive_world_model) Track #4: Predictive World Model.


### Tutorials



### Talks & Seminars




# 7. Acknowledgements



