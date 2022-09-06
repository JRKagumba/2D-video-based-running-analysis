# 2D Video Based Running Analysis 

## Overview

This project aims to create a gait event detection algorithm that does not require conventional methods such as motion capture or force plates and is applicable to a wide range of athletes and gait patterns. The algorithm combines elements of coordinate-based, velocity-based, and probabilistic approaches through a data-driven
model. A time series model is created, using coordinate- and velocity-based features to predict
the likelihood of an event in a series of frames. 


## Background and Motivation

Standard video is an inexpenive alternative to motion-capture for motion monitoring.  Current computational methods as well as large publicly available datasets enable pose estimation algorithms such as OpenPose, PoseNet and UniPose to produce estimates of body posture from standard video across varying lighting, activity, age, skin color, and angleof-view.  Pose estimation software outputs estimates of the two-dimensional (2D) image-plane positions of joints (e.g., ankles and knees) and other anatomical locations in each frame of a video. These estimates of 2D planar projections are too noisy and biased, due to manually annotated ground truth and planar projection errors, to be used directly for extracting clinically meaningful information such as three-dimensional (3D) gait metrics.

To overcome these limitations, this project uses a few machine learning models to learn complex, and potentially nonlinear, relationships between inputs and outputs which have been shown to be an effective tool for making robust predictions. The method used capitalizes on 2D pose estimates from video to predict quantitative gait metrics commonly used in clinical gait analysis,

## Goals

1. Develop a working model
2. Deploy a web application to allow for live interaction
3. Configure a mobile application to allow for real-time gait event detection

## Datasets

The project used publicly available NFL combine videos of athletes performing the 40 yard dash. The datasets are available in their [raw](https://drive.google.com/drive/folders/15UjFBfslOEZuyPIMUAsSGkER2M6ijU5D?usp=sharing) and [processes](https://drive.google.com/drive/folders/1aMwJaAWk4UOqKriprPE-glR-ie6KSkDb?usp=sharing) formats. The dataset consits of 20 individuals from the following 6 different football positions :

- Defensive Backs
- Defensive Linemen
- Offensive Linemen
- Quarterbacks
- Runningbacks
- Wide Receivers

Sample Video:
https://user-images.githubusercontent.com/63820705/188669073-5d7fc0c4-9dbb-4fca-b9dc-9e0a12fd2dc6.mp4

## Practical Applications

#### Clinical
  - Automatic annotation provides more consistent data and reduces the variance of individual annotators as well as between annotators
  
#### Research
  - Motion data collected in a laboratory may fail to capture how individuals move in natural settings
  - The ability to accurately and efficiently extract multiple gait cycles from a trial allows the identification of more gait cycles, generating more data for further analysis
  
#### Financial
  - Motion capture hardware is expensive, recording a simple video is much more financially feasible
  - Payment of human annotators is often required to pre-process motion capture data
  

## Milestones

## Reference
