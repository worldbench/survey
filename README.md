[![Awesome Logo](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
![Visitors](https://komarev.com/ghpvc/?username=worldbench&repo=survey&label=Hello,%20Visitor%20&color=yellow&style=social)
[![PR's Welcome](https://img.shields.io/badge/PRs-welcome-red.svg?style=flat)](https://github.com/worldbench/survey/pulls)

# :sunglasses: Awesome 3D and 4D World Models



### Table of Contents
- [**1. World Modeling from Video Generation**](#1-world-modeling-from-video-generation)
  - [Data Engine]()
  - []()
  - [Closed-Loop Simulator]()
  - [Scene Reconstructor]()
- [**2. World Modeling from Occupancy Generation**](#2-world-modeling-from-occupancy-generation)
  - []()
  - []()
  - []()
- [**3. World Modeling from LiDAR Generation**](#3-world-modeling-from-lidar-generation)
  - []()
  - []()
  - []()
- [**4. Datasets & Benchmarks**](#4-datasets--benchmarks)
  - []()
  - []()
  - []()
- [**5. Applications**](#5-applications)
  - []()
  - []()
  - []()
- [**6. Other Resources**]()
  - [Workshops]()
  - [Tutorials]()
  - [Talks & Seminars]()
- [**7. Acknowledgements**]()



# 1. World Modeling from Video Generation

### :one: Data Engine

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `BEVControl` | [![arXiv](https://img.shields.io/badge/arXiv-2308.01661-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2308.01661)<br>BEVControl: Accurately Controlling Street-View Elements with Multi-Perspective Consistency via BEV Sketch Layout | arXiv 2023 | - | - |
| `BEVGen` | [![arXiv](https://img.shields.io/badge/arXiv-2301.04634-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2301.04634)<br>Street-View Image Generation from a Bird's-Eye View Layout | RA-L 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadriverse.github.io/bevgen/) | [![GitHub](https://img.shields.io/github/stars/alexanderswerdlow/BEVGen)](https://github.com/alexanderswerdlow/BEVGen) |
| `MagicDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2310.02601-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2310.02601)<br>MagicDrive: Street View Generation with Diverse 3D Geometry Control | ICLR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://gaoruiyuan.com/magicdrive/) | [![GitHub](https://img.shields.io/github/stars/cure-lab/MagicDrive)](https://github.com/cure-lab/MagicDrive) |
| `Panacea` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.16813)<br>Panacea: Panoramic and Controllable Video Generation for Autonomous Driving | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://panacea-ad.github.io/) | [![GitHub](https://img.shields.io/github/stars/wenyuqing/panacea)](https://github.com/wenyuqing/panacea) |
| `DrivingDiffusion` | [![arXiv](https://img.shields.io/badge/arXiv-2310.07771-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2310.07771)<br>DrivingDiffusion: Layout-Guided Multi-View Driving Scene Video Generation with Latent Diffusion Model | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drivingdiffusion.github.io/) | [![GitHub](https://img.shields.io/github/stars/shalfun/DrivingDiffusion)](https://github.com/shalfun/DrivingDiffusion) |
| `WoVoGen` | [![arXiv](https://img.shields.io/badge/arXiv-2312.02934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.02934)<br>WoVoGen: World Volume-aware Diffusion for Controllable Multi-camera Driving Scene Generation | ECCV 2024 |
| `Delphi` | [![arXiv](https://img.shields.io/badge/arXiv-2406.01349-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2406.01349)<br>Unleashing Generalization of End-to-End Autonomous Driving with Controllable Long Video Generation | arXiv 2024 | 
| `BEVWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2407.05679-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.05679)<br>BEVWorld: A Multimodal World Simulator for Autonomous Driving via Scene-Level BEV Latents | arXiv 2024 | 
| `PerLDiff` | [![arXiv](https://img.shields.io/badge/arXiv-2407.06109-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.06109)<br>PerLDiff: Controllable Street View Synthesis Using Perspective-Layout Diffusion Models | arXiv 2024 | 
| `Panacea+` | [![arXiv](https://img.shields.io/badge/arXiv-2408.07605-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2408.07605)<br>Panacea+: Panoramic and Controllable Video Generation for Autonomous Driving | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://panacea-ad.github.io/) | 
| `DiVE` | [![arXiv](https://img.shields.io/badge/arXiv-2409.01595-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.01595)<br>DiVE: DiT-Based Video Generation with Enhanced Control | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://liautoad.github.io/DIVE/) | [![GitHub](https://img.shields.io/github/stars/LiAutoAD/DIVE)](https://github.com/LiAutoAD/DIVE) |
| `DreamForge` | [![arXiv](https://img.shields.io/badge/arXiv-2409.04003-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.04003)<br>DreamForge: Motion-Aware Autoregressive Video Generation for Multi-View Driving Scenes | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://pjlab-adg.github.io/DriveArena/dreamforge/) | [![GitHub](https://img.shields.io/github/stars/PJLab-ADG/DriveArena)](https://github.com/PJLab-ADG/DriveArena) |
| `SyntheOcc` | [![arXiv](https://img.shields.io/badge/arXiv-2410.00337-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.00337)<br>SyntheOcc: Synthesize Geometric-Controlled Street View Images through 3D Semantic MPIs | arXiv 2024 | 
| `MagicDrive-V2` | [![arXiv](https://img.shields.io/badge/arXiv-2411.13807-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.13807)<br>MagicDrive-V2: High-Resolution Long Video Generation for Autonomous Driving with Adaptive Control | arXiv 2024 | 
| `HoloDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2412.01407-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.01407)<br>HoloDrive: Holistic 2D-3D Multi-Modal Street Scene Generation for Autonomous Driving | arXiv 2024 |
| `CogDriving` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03520-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03520)<br>Seeing Beyond Views: Multi-View Driving Scene Video Generation with Holistic Attention | arXiv 2024 | 
| `UniMLVG` | [![arXiv](https://img.shields.io/badge/arXiv-2412.04842-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.04842)<br>UniMLVG: Unified Framework for Multi-view Long Video Generation with Comprehensive Control Capabilities for Autonomous Driving | arXiv 2024 | 
| `DrivePhysica` | [![arXiv](https://img.shields.io/badge/arXiv-2412.08410-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.08410)<br>Physical Informed Driving World Model | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadrivescape.github.io/papers_project/DrivePhysica/page.html) | 
| `DriveDreamer-2` | [![arXiv](https://img.shields.io/badge/arXiv-2403.06845-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.06845)<br>DriveDreamer-2: LLM-Enhanced World Models for Diverse Driving Video Generation | AAAI 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drivedreamer2.github.io/) | 
| `SubjectDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2403.19438-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.19438)<br>SubjectDrive: Scaling Generative Data in Autonomous Driving via Subject Control | AAAI 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://subjectdrive.github.io/) | 
| `Glad` | [![arXiv](https://img.shields.io/badge/arXiv-2503.00045-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.00045)<br>Glad: A Streaming Scene Generator for Autonomous Driving | ICLR 2025 | 
| `DualDiff` | [![arXiv](https://img.shields.io/badge/arXiv-2505.01857-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.01857)<br>DualDiff: Dual-branch Diffusion Model for Autonomous Driving with Semantic Fusion | ICRA 2025 | 
| `UniScene` | [![arXiv](https://img.shields.io/badge/arXiv-2412.05435-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.05435)<br>UniScene: Unified Occupancy-Centric Driving Scene Generation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://arlo0o.github.io/uniscene/) | 
| `DriveScape` | [![arXiv](https://img.shields.io/badge/arXiv-2409.05463-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.05463)<br>DriveScape: Towards High-Resolution Controllable Multi-View Driving Video Generation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadrivescape.github.io/papers_project/drivescapev1/index.html) | 
| `DualDiff+` | [![arXiv](https://img.shields.io/badge/arXiv-2503.03689-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.03689)<br>DualDiff+: Dual-Branch Diffusion for High-Fidelity Video Generation with Reward Guidance | arXiv 2025 |  | [![GitHub](https://img.shields.io/github/stars/yangzhaojason/DualDiff)](https://github.com/yangzhaojason/DualDiff) |
| `CoGen` | [![arXiv](https://img.shields.io/badge/arXiv-2503.22231-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.22231)<br>CoGen: 3D Consistent Video Generation via Adaptive Conditioning for Autonomous Driving | arXiv 2025 | 
| `NoiseController` | [![arXiv](https://img.shields.io/badge/arXiv-2504.18448-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2504.18448)<br>NoiseController: Towards Consistent Multi-view Video Generation via Noise Decomposition and Collaboration | arXiv 2025 | 
| `STAGE` | [![arXiv](https://img.shields.io/badge/arXiv-2506.13138-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.13138)<br>STAGE: A Stream-Centric Generative World Model for Long-Horizon Driving-Scene Simulation | arXiv 2025 | 
||



### :two:

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `GAIA-1` | [![arXiv](https://img.shields.io/badge/arXiv-2309.17080-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2309.17080)<br>GAIA-1: A Generative World Model for Autonomous Driving | arXiv 2023 |
| `ADriver-I` | [![arXiv](https://img.shields.io/badge/arXiv-2311.13549-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.13549)<br>ADriver-I: A General World Model for Autonomous Driving | arXiv 2023 |
| `Drive-WM` | [![arXiv](https://img.shields.io/badge/arXiv-2311.17918-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.17918)<br>Driving into the Future: Multiview Visual Forecasting and Planning with World Model for Autonomous Driving | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drive-wm.github.io/) | [![GitHub](https://img.shields.io/github/stars/BraveGroup/Drive-WM)](https://github.com/BraveGroup/Drive-WM) |
| `DriveDreamer` | [![arXiv](https://img.shields.io/badge/arXiv-2309.09777-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2309.09777)<br>DriveDreamer: Towards Real-world-driven World Models for Autonomous Driving | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drivedreamer.github.io/) | 
| `GenAD` | [![arXiv](https://img.shields.io/badge/arXiv-2403.09630-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.09630)<br>GenAD: Generalized Predictive Model for Autonomous Driving | ECCV 2024 | 
| `Vista` | [![arXiv](https://img.shields.io/badge/arXiv-2405.17398-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.17398)<br>Vista: A Generalizable Driving World Model with High Fidelity and Versatile Controllability | NeurIPS 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://vista-demo.github.io/) | [![GitHub](https://img.shields.io/github/stars/OpenDriveLab/Vista)](https://github.com/OpenDriveLab/Vista) |
| `InfinityDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2412.01522-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.01522)<br>InfinityDrive: Breaking Time Limits in Driving World Models | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadrivescape.github.io/papers_project/InfinityDrive/page.html) | 
| `DrivingGPT` | [![arXiv](https://img.shields.io/badge/arXiv-2412.18607-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.18607)<br>DrivingGPT: Unifying Driving World Modeling and Planning with Multi-Modal Autoregressive Transformers | arXiv 2024 |  |
| `DrivingWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2412.19505-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.19505)<br>DrivingWorld: Constructing World Model for Autonomous Driving via Video GPT | arXiv 2024 |  | [![GitHub](https://img.shields.io/github/stars/YvanYin/DrivingWorld)](https://github.com/YvanYin/DrivingWorld) |
| `GEM` | [![arXiv](https://img.shields.io/badge/arXiv-2412.11198-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.11198)<br>GEM: A Generalizable Ego-Vision Multimodal World Model for Fine-Grained Ego-Motion, Object Dynamics, and Scene Composition Control | CVPR 2025 |  |  |
| `MaskGWM` | [![arXiv](https://img.shields.io/badge/arXiv-2502.11663-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.11663)<br>MaskGWM: A Generalizable Driving World Model with Video Mask Reconstruction | CVPR 2025 |  |  |
| `GAIA-2` | [![arXiv](https://img.shields.io/badge/arXiv-2503.20523-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.20523)<br>GAIA-2: A Controllable Multi-View Generative World Model for Autonomous Driving | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wayve.ai/thinking/gaia-2) |  |
| `MiLA` | [![arXiv](https://img.shields.io/badge/arXiv-2503.15875-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.15875)<br>MiLA: Multi-View Intensive-Fidelity Long-Term Video Generation World Model for Autonomous Driving | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/xiaomi-mlab/mila.github.io) |  |
| `DriVerse` | [![arXiv](https://img.shields.io/badge/arXiv-2504.18576-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2504.18576)<br>DriVerse: Navigation World Model for Driving Simulation via Multimodal Trajectory Prompting and Motion Alignment | arXiv 2025 | 
| `PosePilot` | [![arXiv](https://img.shields.io/badge/arXiv-2505.01729-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.01729)<br>PosePilot: Steering Camera Pose for Generative World Models with Self-Supervised Depth | arXiv 2025 |
| `ProphetDWM` | [![arXiv](https://img.shields.io/badge/arXiv-2505.18650-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.18650)<br>ProphetDWM: A Driving World Model for Rolling Out Future Actions and Videos | arXiv 2025 | 
| `GeoDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2505.22421-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2505.22421)<br>GeoDrive: 3D Geometry-Informed Driving World Model with Precise Action Control | arXiv 2025 |  | [![GitHub](https://img.shields.io/github/stars/antonioo-c/GeoDrive)](https://github.com/antonioo-c/GeoDrive) |
| `LongDWM` | [![arXiv](https://img.shields.io/badge/arXiv-2506.01546-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.01546)<br>LongDWM: Cross-Granularity Distillation for Building A Long-Term Driving World Model | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://wang-xiaodong1899.github.io/longdwm/) |  |
||



## :three: Closed-Loop Simulator

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `MagicDrive3D` | [![arXiv](https://img.shields.io/badge/arXiv-2405.14475-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.14475)<br>MagicDrive3D: Controllable 3D Generation for Any-View Rendering in Street Scenes | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://flymin.github.io/magicdrive3d) |  |
| `DriveArena` | [![arXiv](https://img.shields.io/badge/arXiv-2408.00415-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2408.00415)<br>DriveArena: A Closed-Loop Generative Simulation Platform for Autonomous Driving | arXiv 2024 |  | [![GitHub](https://img.shields.io/github/stars/PJLab-ADG/DriveArena)](https://github.com/PJLab-ADG/DriveArena) |
| `InfiniCube` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>InfiniCube: Unbounded and Controllable Dynamic 3D Driving Scene Generation with World-Guided Video Models | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/infinicube/) |  |
| `Doe-1` | [![arXiv](https://img.shields.io/badge/arXiv-2412.09627-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.09627)<br>Doe-1: Closed-Loop Autonomous Driving with Large World Model | arXiv 2024 |  | [![GitHub](https://img.shields.io/github/stars/wzzheng/Doe)](https://github.com/wzzheng/Doe) |
| `DrivingSphere` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>DrivingSphere: Building A High-Fidelity 4D World for Closed-Loop Simulation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yanty123.github.io/DrivingSphere/) |  |
| `UniFuture` | [![arXiv](https://img.shields.io/badge/arXiv-2503.13587-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.13587)<br>Seeing the Future, Perceiving the Future: A Unified Driving World Model for Future Generation and Perception | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://github.com/dk-liang/UniFuture) |  |
| `DiST-4D` | [![arXiv](https://img.shields.io/badge/arXiv-2503.15208-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.15208)<br>DiST-4D: Disentangled Spatiotemporal Diffusion with Metric Depth for 4D Driving Scene Generation | arXiv 2025 | 
||



### :four: Scene Reconstructor

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `StreetGaussian` | [![arXiv](https://img.shields.io/badge/arXiv-2401.01339-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2401.01339)<br>Street Gaussians: Modeling Dynamic Urban Scenes with Gaussian Splatting | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://zju3dv.github.io/street_gaussians) | [![GitHub](https://img.shields.io/github/stars/zju3dv/street_gaussians)](https://github.com/zju3dv/street_gaussians) |
||



# 2. World Modeling from Occupancy Generation

### :one: 

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `SSD` | [![arXiv](https://img.shields.io/badge/arXiv-2301.00527-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2301.00527)<br>Diffusion Probabilistic Models for Scene-Scale 3D Categorical Data | arXiv 2023 | 
| `WoVoGen` | [![arXiv](https://img.shields.io/badge/arXiv-2312.02934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.02934)<br>WoVoGen: World Volume-aware Diffusion for Controllable Multi-camera Driving Scene Generation | ECCV 2024 |
| `UrbanDiff` | [![arXiv](https://img.shields.io/badge/arXiv-2403.11697-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.11697)<br>Urban Scene Diffusion through Semantic Occupancy Map | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://metadriverse.github.io/urbandiff/) |  |
| `DrivingSphere` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>DrivingSphere: Building A High-Fidelity 4D World for Closed-Loop Simulation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yanty123.github.io/DrivingSphere/) |  |
| `UniScene` | [![arXiv](https://img.shields.io/badge/arXiv-2412.05435-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.05435)<br>UniScene: Unified Occupancy-Centric Driving Scene Generation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://arlo0o.github.io/uniscene/) |  |
||



### :two: Occupancy Forecasting

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `UniWorld` |
| `Cam4DOcc` | [![arXiv](https://img.shields.io/badge/arXiv-2311.17663-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.17663)<br>Cam4DOcc: Benchmark for Camera-Only 4D Occupancy Forecasting in Autonomous Driving Applications | CVPR 2024 |  | [![GitHub](https://img.shields.io/github/stars/haomo-ai/Cam4DOcc)](https://github.com/haomo-ai/Cam4DOcc) |
| `DriveWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2405.04390-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.04390)<br>DriveWorld: 4D Pre-Trained Scene Understanding via World Models for Autonomous Driving | CVPR 2024 |  |  |
| `OccWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2311.16038-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.16038)<br>OccWorld: Learning A 3D Occupancy World Model for Autonomous Driving | ECCV 2024 |  | [![GitHub](https://img.shields.io/github/stars/wzzheng/OccWorld)](https://github.com/wzzheng/OccWorld) |
| `OccSora` | [![arXiv](https://img.shields.io/badge/arXiv-2405.20337-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2405.20337)<br>OccSora: 4D Occupancy Generation Models as World Simulators for Autonomous Driving | arXiv 2024 |  | [![GitHub](https://img.shields.io/github/stars/wzzheng/OccWorld)](https://github.com/wzzheng/OccSora) |
| `LOPR` | [![arXiv](https://img.shields.io/badge/arXiv-2407.21126-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.21126)<br>Self-Supervised Multi-Future Occupancy Forecasting for Autonomous Driving | arXiv 2024 | 
| `FSF-Net` | [![arXiv](https://img.shields.io/badge/arXiv-2409.15841-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.15841)<br>FSF-Net: Enhance 4D Occupancy Forecasting with Coarse BEV Scene Flow for Autonomous Driving | arXiv 2024 | 
| `DOME` | [![arXiv](https://img.shields.io/badge/arXiv-2410.10429-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.10429)<br>DOME: Taming Diffusion Model into High-Fidelity Controllable Occupancy World Model | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://gusongen.github.io/DOME) |  |
| `GaussianAD` | [![arXiv](https://img.shields.io/badge/arXiv-2412.10371-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.10371)<br>GaussianAD: Gaussian-Centric End-to-End Autonomous Driving | arXiv 2024 |  | [![GitHub](https://img.shields.io/github/stars/wzzheng/GaussianAD)](https://github.com/wzzheng/GaussianAD) |
| `DFIT-OccWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2412.13772-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.13772)<br>An Efficient Occupancy World Model via Decoupled Dynamic Flow and Image-Assisted Training | arXiv 2024 | 
| `Drive-OccWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2408.14197-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2408.14197)<br>Driving in the Occupancy World: Vision-Centric 4D Occupancy Forecasting and Planning via World Models for Autonomous Driving | AAAI 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://drive-occworld.github.io/) |  |
| `RenderWorld` | [![arXiv](https://img.shields.io/badge/arXiv-2409.11356-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.11356)<br>RenderWorld: World Model with Self-Supervised 3D Label | ICRA 2025 |  |  |
| `Occ-LLM` | [![arXiv](https://img.shields.io/badge/arXiv-2502.06419-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2502.06419)<br>Occ-LLM: Enhancing Autonomous Driving with Occupancy-Based Large Language Models | ICRA 2025 |  |  |
| `EfficientOCF` | [![arXiv](https://img.shields.io/badge/arXiv-2411.14169-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2411.14169)<br>Spatiotemporal Decoupling for Efficient Vision-Based Occupancy Forecasting | CVPR 2025 |  |  |
| `T3Former` | [![arXiv](https://img.shields.io/badge/arXiv-2503.07338-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.07338)<br>Temporal Triplane Transformers as Occupancy World Models | arXiv 2025 |  |  |
| `UniOcc` | [![arXiv](https://img.shields.io/badge/arXiv-2503.24381-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2503.24381)<br>UniOcc: A Unified Benchmark for Occupancy Forecasting and Prediction in Autonomous Driving | arXiv 2025 |  | [![GitHub](https://img.shields.io/github/stars/tasl-lab/UniOcc)](https://github.com/tasl-lab/UniOcc) |
| `COME` | [![arXiv](https://img.shields.io/badge/arXiv-2506.13260-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.13260)<br>COME: Adding Scene-Centric Forecasting Control to Occupancy World Model | arXiv 2025 |  | [![GitHub](https://img.shields.io/github/stars/synsin0/COME)](https://github.com/synsin0/COME) |
||



### :three: 

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `SemCity` | [![arXiv](https://img.shields.io/badge/arXiv-2403.07773-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.07773)<br>SemCity: Semantic Scene Generation with Triplane Diffusion | CVPR 2024 |
| `XCube` | [![arXiv](https://img.shields.io/badge/arXiv-2312.03806-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.03806)<br>XCube: Large-Scale 3D Generative Modeling using Sparse Voxel Hierarchies | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/xcube/) | [![GitHub](https://img.shields.io/github/stars/nv-tlabs/XCube)](https://github.com/nv-tlabs/XCube) |
| `PDD` | [![arXiv](https://img.shields.io/badge/arXiv-2311.12085-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.12085)<br>Pyramid Diffusion for Fine 3D Large Scene Generation | ECCV 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://yuheng.ink/project-page/pyramid-discrete-diffusion) | [![GitHub](https://img.shields.io/github/stars/yuhengliu02/pyramid-discrete-diffusion)](https://github.com/yuhengliu02/pyramid-discrete-diffusion) |
| `InfiniCube` | [![arXiv](https://img.shields.io/badge/arXiv-2412.03934-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.03934)<br>InfiniCube: Unbounded and Controllable Dynamic 3D Driving Scene Generation with World-Guided Video Models | arXiv 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://research.nvidia.com/labs/toronto-ai/infinicube/) |  |
| `DynamicCity` | [![arXiv](https://img.shields.io/badge/arXiv-2410.18084-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2410.18084)<br>DynamicCity: Large-Scale 4D Occupancy Generation from Dynamic Scenes | ICLR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://dynamic-city.github.io/) |  |
| `X-Scene` | [![arXiv](https://img.shields.io/badge/arXiv-2506.13558-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2506.13558)<br>X-Scene: Large-Scale Driving Scene Generation with High Fidelity and Flexible Controllability | arXiv 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://x-scene.github.io/) |  |



# 3. World Modeling from LiDAR Generation

### :one: 

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `DUSty-GAN` | [![arXiv](https://img.shields.io/badge/arXiv-2102.11952-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2102.11952)<br>Learning to Drop Points for LiDAR Scan Synthesis | IROS 2021 | 
| `LiDARGen` | [![arXiv](https://img.shields.io/badge/arXiv-2209.03954-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2209.03954)<br>Learning to Generate Realistic LiDAR Point Clouds | ECCV 2022 |
| `DUSty-GAN v2` | [![arXiv](https://img.shields.io/badge/arXiv-2210.11750-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2210.11750)<br>Generative Range Imaging for Learning Scene Priors of 3D LiDAR Data | WACV 2023 | 
| `UltraLiDAR` | [![arXiv](https://img.shields.io/badge/arXiv-2311.01448-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.01448)<br>UltraLiDAR: Learning Compact Representations for LiDAR Completion and Generation | CVPR 2023 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://waabi.ai/ultralidar/) |  |
| `Copilot4D` | [![arXiv](https://img.shields.io/badge/arXiv-2311.01017-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2311.01017)<br>Copilot4D: Learning Unsupervised World Models for Autonomous Driving via Discrete Diffusion | ICLR 2024 | 
| `R2DM` | [![arXiv](https://img.shields.io/badge/arXiv-2309.09256-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2309.09256)<br>LiDAR Data Synthesis with Denoising Diffusion Probabilistic Models | ICRA 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://kazuto1011.github.io/r2dm) |  |
| `LiDM` | [![arXiv](https://img.shields.io/badge/arXiv-2404.00815-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2404.00815)<br>Towards Realistic Scene Generation with LiDAR Diffusion Models | CVPR 2024 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://lidar-diffusion.github.io/) |  |
| `ViDAR` | [![arXiv](https://img.shields.io/badge/arXiv-2312.17655-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2312.17655)<br>Visual Point Cloud Forecasting enables Scalable Autonomous Driving | CVPR 2024 |
| `RangeLDM` | [![arXiv](https://img.shields.io/badge/arXiv-2403.10094-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2403.10094)<br>RangeLDM: Fast Realistic LiDAR Point Cloud Generation | ECCV 2024 | 
| `Text2LiDAR` | [![arXiv](https://img.shields.io/badge/arXiv-2407.19628-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2407.19628)<br>Text2LiDAR: Text-guided LiDAR Point Cloud Generation via Equirectangular Transformer | ECCV 2024 | 
| `BEVWorld` |
| `HoloDrive` | [![arXiv](https://img.shields.io/badge/arXiv-2412.01407-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.01407)<br>HoloDrive: Holistic 2D-3D Multi-Modal Street Scene Generation for Autonomous Driving | arXiv 2024 |
| `LiDARGRIT` |
| `SDS` |
| `OLiDM` |
| `X-Drive` |
| `R2Flow` |
| `LidarDM` |
| `WeatherGen` |
| `HERMES` |
| `DriveX` |
| `SPIRAL` |




# 4. Datasets & Benchmarks




# 5. Applications




# 6. Other Resources

### Workshops


### Tutorials


### Talks & Seminars




# 7. Acknowledgements



