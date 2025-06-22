[![Awesome Logo](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
![Visitors](https://komarev.com/ghpvc/?username=worldbench&repo=survey&label=Hello,%20Visitor%20&color=yellow&style=social)
[![PR's Welcome](https://img.shields.io/badge/PRs-welcome-red.svg?style=flat)](https://github.com/worldbench/survey/pulls)

# :sunglasses: Awesome 3D and 4D World Models



### Table of Contents
- [World Modeling from Video Generation]()
  - [Data Engine]()
  - []()
  - []()
- [World Modeling from Occupancy Generation]()
  - []()
  - []()
  - []()
- [World Modeling from LiDAR Generation]()
  - []()
  - []()
  - []()
- [Datasets & Benchmarks]()
  - []()
  - []()
  - []()
- [Applications]()
  - []()
  - []()
  - []()
- [Other Resources]()
  - [Workshops]()
  - [Tutorials]()
  - [Talks & Seminars]()
- [Acknowledgements]()



## World Modeling from Video Generation

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
| `UniScene` | [![arXiv](https://img.shields.io/badge/arXiv-2412.05435-b31b1b?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2412.05435)<br>UniScene: Unified Occupancy-centric Driving Scene Generation | CVPR 2025 | [![Website](https://img.shields.io/badge/Link-yellow?style=flat-square&logo=gitbook)](https://arlo0o.github.io/uniscene/) | 
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
| `GenAD` |
| `Vista` |
| `DrivingWorld` |
| `DrivingGPT` |
| `Doe-1` |
| `InfinityDrive` |
| `GEM` |
| `GAIA-2` |
| `MaskGWM` |
| `DriVerse` |
| `MiLA` |
| `GeoDrive` |
| `PosePilot` |
| `ProphetDWM` |
| `LongDWM` |
||



## :three:

> :timer_clock: In chronological order, from the earliest to the latest.

| Model | Paper | Venue | Website | GitHub | 
|:-:|:-|:-:|:-:|:-:|
||
| `DriveArena` |
| `MagicDrive3D` |
| `InfiniCube` |
| `DrivingSphere` |
| `DiST-4D` |
| `UniFuture` |
||



## World Modeling from Occupancy Generation




## World Modeling from LiDAR Generation



## Datasets & Benchmarks



## Applications



## Other Resources

### Workshops


### Tutorials


### Talks & Seminars



## Acknowledgements

