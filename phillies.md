---
layout: default
title: Phillies CV Proposal
---

# Computer Vision for Defensive Evaluation in Baseball

[Download Proposal (PDF)](pdf/Phillies_CV_Proposal.pdf)  
[Download Project Outline (PDF)](pdf/Phillies_CV_Outline.pdf)

_**Project Overview**_  
This project explores how **computer vision (CV) techniques can be integrated with traditional baseball analytics models** to improve the evaluation of defensive performance, with an initial focus on the first baseman position.  

The goal is to design a pipeline that extracts **pose estimation and ball-tracking signals** from broadcast video, transforms them into quantitative features, and tests their predictive value when combined with standard play-level defensive metrics.  

The proposal and outline provide:
- A **motivation** for applying CV to defensive evaluation.  
- A description of the **CV tools and methods** (YOLOv8, DeepSORT, pose estimation).  
- Plans for a **feature extraction pipeline** linking CV outputs with play-level datasets.  
- A **research roadmap** for scaling CV-derived features into predictive modeling workflows used by baseball analysts.  

![CV Pipeline Concept](images/cv_pipeline.png)  
*Conceptual diagram of pose estimation and ball-tracking feeding into defensive evaluation models.*  

_**Tools & Techniques**_
- YOLOv8 for object detection  
- DeepSORT for player and ball tracking  
- Pose estimation models for body mechanics  
- Feature engineering for integrating CV signals with play-level data  

## Next Steps

Future work will:  
- Expand testing across multiple defensive positions.  
- Benchmark predictive improvements against models using only non-CV data.  
- Explore scaling the system to real-time applications for scouting and player development.  
- Extend the framework to measure defensive decision-making and reaction times.  

---
