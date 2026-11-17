<p align="center">
  <h1 align="center">LD-AtlasLoc: Long-Distance Monocular Aerial Image Localization with Geo-Referenced Sparse Maps under GNSS-Degraded and Appearance-Changing Conditions</h1>
  <p align="center">
    <strong>Li Dongdong</strong> |
    <strong>Yang Tao</strong> |
    <strong>Qin Shuo</strong> |
    <strong>Zhang Yisu</strong> |
    <strong>Li Jing</strong>
  </p>
  <h3 align="center">
    <a href="https://www.sciencedirect.com/science/article/pii/S092427162600537X">Paper</a> |
    <a href="https://www.youtube.com/watch?v=1-a3fRpCcGE">YouTube Demo</a> |
    <a href="https://v.qq.com/x/page/s32753laghj.html">Tencent Demo</a> 
  </h3>
</p>

<h2 align="center">Qualitative Comparisons</h2>

<h3 align="center">Foggy Scene - Baseline Method</h3>

<p align="center">
  <img src="./media/fog-baseline-hd.gif" alt="Foggy scene baseline localization result" width="100%">
</p>

<h3 align="center">Foggy Scene - LD-AtlasLoc (Ours)</h3>

<p align="center">
  <img src="./media/fog-atlas-loc-hd.gif" alt="Foggy scene Atlas-Loc localization result" width="100%">
</p>

<h3 align="center">Night Scene - Baseline Method</h3>

<p align="center">
  <img src="./media/night-baseline-hd.gif" alt="Night scene baseline localization result" width="100%">
</p>

<h3 align="center">Night Scene - LD-AtlasLoc (Ours)</h3>

<p align="center">
  <img src="./media/night-atlas-loc-hd.gif" alt="Night scene Atlas-Loc localization result" width="100%">
</p>

<br>

## Overview

Accurate, long-distance UAV and eVTOL navigation remains a critical challenge in urban canyons, complex electromagnetic environments, and under GNSS interference. While visual SLAM reduces GNSS reliance, it often suffers from drift and tracking failure under drastic appearance changes (fog, rain, day-night).

**LD-AtlasLoc** is a monocular visual relocalization framework designed for **intermittent GNSS-degraded scenarios**. It bridges the gap between high-precision mapping and robust online localization.


## DEMO
https://github.com/Ldd-slam/LD-AtlasLoc/blob/main/demo.mp4

<video controls width="720">
  <source src="https://github.com/Ldd-slam/LD-AtlasLoc/releases/download/v1.0/demo.mp4" type="video/mp4">
</video>


## Dataset Description






LD-AtlasLoc is constructed to reflect **real-world low-altitude flight constraints**, covering diverse urban and suburban environments. Unlike conventional datasets, it focuses on flight-compliant trajectories and challenging environmental conditions.

<p align="center">
  <img src="./media/dataset-showcase.png" alt="Dataset showcase" width="100%">
</p>


### 🚁 Flight Profile & Compliance
- **Realistic Altitude:** Flights are conducted at **120–150 m**, aligning with typical low-altitude logistics and urban eVTOL operational limits.
- **Compliant Trajectories:** Paths strictly follow **urban roads, green belts, and open areas**, avoiding arbitrary intrusion into dense built-up zones.
- **Safety Constraints:** Collection adheres to real-world regulations, including airspace permissions, safe distances from buildings, and privacy standards.

### 🌦️ Environmental Diversity
The dataset introduces substantial variations to challenge visual robustness:

| Dimension | Conditions Covered |
| :--- | :--- |
| **Season** | Winter ↔️ Spring (significant vegetation changes) |
| **Illumination** | High solar elevation, long building shadows, night vs. day |
| **Weather** | ☀️ Sunny · ☁️ Cloudy · 🌫️ Foggy · 🌧️ Rainy · 🌃 Night |

**Specific Challenges:**
- **Fog:** Severe visibility degradation, with near-total texture loss in most regions.
- **Rain:** Local blur, reflections, and sensor noise.
- **Low-light / Night:** Underexposure, streetlight glare, motion blur, and reduced descriptor discriminability.

### 🏙️ Scene Composition
We cover three representative low-altitude urban environments:

| Scene ID | Description | Key Characteristics |
| :--- | :--- | :--- |
| **City1-Buildings** | Mixed Urban-Suburban | Combination of high-rise and low-rise structures. |
| **City2-Skyscrapers** | Dense Urban Center | **24–30 stories** (up to 120 m). Exhibits severe **Urban Canyon
| **City3-outskirts** | ​Suburban / Rural Fringe | **Sparse vegetation** and **repetitive ground textures** leading to feature scarcity. |


### 1. Data Description​
The compressed files City1-buildings.rar, City2-skyscrapers.rar, and City3-outskirts.rar contain image data. The original resolution of 5472×3648 has been downscaled to 1805×1203.
### 2. RTK-GNSS Information​
Each image retains RTK-GNSS information with centimeter-level accuracy, which can be used for mapping and ground-truth error evaluation.
### 3. Data Collection Details​
Multiple sequences per scene were recorded along the same trajectory across different times. Trajectories are not strictly repeated, with ~20 m deviations in all directions to simulate realistic flight perturbations, thereby enabling robust evaluation of localization across diverse parallax views.

## Dataset Access

- [Baidu Netdisk](https://pan.baidu.com/s/1QL3i6Cz4F0489Y-cX65Z4Q?pwd=3spe/)


## Contact
- [Team Introduction](https://robot-vision.net/) 
- [Personal Email](1051196347@qq.com)


```bibtex
@article{LI2027970,
title = {LD-AtlasLoc: Long-distance monocular aerial image localization with geo-referenced sparse maps under GNSS-degraded and appearance-changing conditions},
journal = {ISPRS Journal of Photogrammetry and Remote Sensing},
volume = {243},
pages = {970-988},
year = {2027},
issn = {0924-2716},
doi = {https://doi.org/10.1016/j.isprsjprs.2026.10.040},
url = {https://www.sciencedirect.com/science/article/pii/S092427162600537X},
author = {Dongdong Li and Tao Yang and Shuo Qin and Yisu Zhang and Jing Li},
}
```
