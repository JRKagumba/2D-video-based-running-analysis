# 2D Video Based Running Analysis 

## Overview

This project aims to create a gait event detection algorithm that does not require conventional methods such as motion capture or force plates and is applicable to a wide range of athletes and gait patterns. The algorithm combines elements of coordinate-based, velocity-based, and probabilistic approaches through a data-driven
model. A time series model is created, using coordinate and velocity-based features to predict
the likelihood of an event in a series of frames. 


## Background and Motivation

Standard video is an inexpenive alternative to motion-capture for motion monitoring.  Current computational methods as well as large publicly available datasets enable pose estimation algorithms such as OpenPose, PoseNet and UniPose to produce estimates of body posture from standard video across varying lighting, activity, age, skin color, and angleof-view.  Pose estimation software outputs estimates of the two-dimensional (2D) image-plane positions of joints (e.g., ankles and knees) and other anatomical locations in each frame of a video. These estimates of 2D planar projections are too noisy and biased, due to manually annotated ground truth and planar projection errors, to be used directly for extracting clinically meaningful information such as three-dimensional (3D) gait metrics.

The motivation for this project was to create an inexpensive solution to produce state-of-the-art biomechanical gait analysis. The dataset consits of videos shot at the same angle and the NFL provides each individual performers body metrics (i.e height, weight). Given this information, it is possible to produce a state-of-the-art gait analytics.  This project uses a few machine learning models to learn complex, and potentially nonlinear, relationships between inputs.  The method used capitalizes on 2D pose estimates from video to predict quantitative gait metrics commonly used in clinical gait analysis.

## Goals

1. Develop a working model
2. Deploy a web application to allow for live interaction
3. Configure a mobile application to allow for real-time gait event detection

## Datasets

The project used publicly available NFL combine videos of athletes performing the 40 yard dash. The datasets are available in their [raw](https://drive.google.com/drive/folders/15UjFBfslOEZuyPIMUAsSGkER2M6ijU5D?usp=sharing) and [processes](https://drive.google.com/drive/folders/1aMwJaAWk4UOqKriprPE-glR-ie6KSkDb?usp=sharing) formats. Relevant player body metrics from the combine (i.e height, weight...) are also used. The dataset consits of 20 individuals from the following 6 different football positions :

- Defensive Backs
- Defensive Linemen
- Offensive Linemen
- Quarterbacks
- Runningbacks
- Wide Receivers

![image](https://user-images.githubusercontent.com/63820705/188670279-756403b2-7d65-4ef3-a450-0d80be916606.png)

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

### :white_check_mark: Phase 1 :
Develop pre-processing pipeline and model that can take a video of the correct format as input and output a gait report

### :white_square_button: Phase 2 :
Create a web app/dashboard that allows users to interact with videos and data

### :white_square_button: Phase 3 : 
Configure a mobile application to allow for real-time gait event detection and analysis


## Reference

- [Computer Vision and Gait Analysis - Paper #1](https://www.researchgate.net/publication/351176461_Human_Gait_Analysis_Using_Machine_Learning_A_Review)
- [Computer Vision and Gait Analysis - Paper #2](https://dl.acm.org/doi/10.1145/3474121)
- [Computer Vision and Gait Analysis - Blog Post](https://towardsdatascience.com/diy-stride-analysis-driven-by-machine-learning-to-compare-the-next-generation-of-running-shoes-1a33ddfcf706)
- [Motion Capture Based Gait Analysis - Paper #1](https://pubmed.ncbi.nlm.nih.gov/31900980/)
- [Motion Capture Based Gait Analysis - Paper #2](https://pubmed.ncbi.nlm.nih.gov/29920155/)
