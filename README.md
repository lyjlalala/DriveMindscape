<div align="center">

# 🚗 DriveMindscape

**A Multimodal Driving Dataset with Aligned Cognition and Behavior**

</div>

---

## 🌟 About the Dataset
**DriveMindscape** is a novel multimodal driving dataset that integrates human behaviors, eye-tracking data, psychophysiological states, and real-time cognitive narrations collected from 34 subjects under carefully designed critical traffic scenarios. 

Current autonomous driving datasets typically lack multi-dimensional cognitive evidence chains (encompassing physiological, mental, and behavioral modalities). DriveMindscape bridges this gap by offering rigorous human-in-the-loop experiment data, providing robust support for interpretable white-box driver cognitive modeling and human-factor safety analysis in long-tail scenarios.

The dataset is publicly available at [this link](https://drive.google.com/drive/folders/19-xw9y8q8kv1JqhTRxBfeI32vovKEE5s?usp=sharing).

---

## ✨ Key Features

- **Multimodal Alignment**: Synchronizes vehicle sensors, control behaviors, 3D eye-tracking vectors, and multi-dimensional emotional scales (SAM & DES).
- **High-Risk Critical Scenarios**: Carefully designs specific traffic safety events (e.g., cut-ins under pressure, blind-spot pedestrians, lane-changing games) to induce high cognitive load and rich cognitive behaviors.
- **First-Person Cognitive Narrations**: Captures genuine decision-making thought processes via post-experiment interviews and Critical Decision Methods (CDM), authentically reconstructing the driver's dynamic thinking without relying on synthetic/post-hoc bias.
- **Formalized Cognitive Knowledge**: Provides formalized ACT-R knowledge chunks and production rules to bridge the gap between internal reasoning and observable actions.
- **Detailed Driver Profiling**: Includes comprehensive metadata for 34 participants, covering demographics, driving styles, and personality traits (MBTI and Big Five).

---

## 🎮 Experimental Platform

The data was collected utilizing a VR-integrated semi-physical driving simulation platform to conduct human-in-the-loop (HITL) experiments.
* **Simulation Environment**: CARLA simulator.
* **Hardware Setup**: 
  * HTC VIVE Pro Eye HMD (with built-in eye-tracking).
  * Logitech G923 racing wheel and pedal set.
  * High-performance graphics workstation (NVIDIA GeForce RTX 4090 GPU).

---

## 🛣️ Critical Scenarios

The dataset focuses on three highly dynamic and complex long-tail scenarios that challenge a driver's situational awareness and decision-making:
1. **Scenario A (Highway Cut-in)**: The ego vehicle follows a lead car on a highway while being pressured by a vehicle behind honking. A front-right vehicle abruptly cuts in, forcing a choice between braking or swerving into a high-speed left lane.
2. **Scenario B (Blind-Spot Pedestrian)**: The ego vehicle prepares to turn right at an intersection when a pedestrian suddenly emerges from a right-side blind spot, forcing a decision between emergency braking or accelerating to pass.
3. **Scenario C (Lane-Changing Game)**: The ego vehicle and a right-lane vehicle both intend to merge into a vacant middle lane to overtake slow traffic, triggering a tactical interaction and game-theoretic decision process.

---

## 🗂️ Data Structure & Composition

The dataset provides synchronous multimodal data streams. Visual sensors are sampled at **10 Hz**, while ego-vehicle states and behaviors are logged at a high frequency of **80 Hz**.

| Category | Content & Description | Format |
| :--- | :--- | :--- |
| **Driver Profile** | Demographics (29 Male, 5 Female), driving experience, driving style, MBTI & Big Five personality trait scores. | `CSV` |
| **Visual Data (10 Hz)** | Front-view RGB, BEV, depth, semantic/instance segmentation, DVS, first-person gaze videos with audio (engine, horn, collision). | `JPG`, `MP4` |
| **Log Data (80 Hz)** | High-frequency ego-vehicle states (location, rotation, velocity, acceleration), dynamic actor bounding boxes, waypoints, control signals (throttle, steering, brake). | `CSV` |
| **Eye Tracking** | Gaze origin/direction, pupil diameter, eye openness, hit points, focused objects (ROIs) based on post-saccadic suppression. | `CSV` |
| **Emotion Data** | SAM (Valence, Arousal, Dominance) & DES (7 specific emotions like Anger, Fear, Surprise) self-assessments. | `CSV` |
| **Cognitive Thought** | Natural language descriptions of decision-making rationales transcribed from semi-structured interviews. | `CSV` |
| **Cognitive Rules** | Formalized ACT-R variables (chunks) and condition-action rules (productions). | `JSON` |

---

## 👥 Contributors


