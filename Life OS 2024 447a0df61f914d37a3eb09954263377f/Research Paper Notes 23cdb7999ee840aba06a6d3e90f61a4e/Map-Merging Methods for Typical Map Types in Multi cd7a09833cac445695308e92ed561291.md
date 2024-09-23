# Map-Merging Methods for Typical Map Types in Multiple-Ground-Robot SLAM Solution

Created: March 15, 2024 2:40 PM
Paper Link: https://www.mdpi.com/915990
Status: In progress

**Table of Contents**

# Introduction

The paper aims to review various map merging methods based on types of maps and methods applicable to individual types of maps and find an efficient method based on application requirements.

# Outline

- Multi-Robot SLAM has 3 major tasks to focus on:
    - Determination of Relative Pose:
        
        It is referred to as the acquisition of robot poses concerning a specific robot, before or during the process of collaborative exploration.
        
        With knowle
        
    - Data Exchange (Communication)
    - Map Merging (or Map Fusion)

---

## Types of Maps

**Commonly Used Types:**

- Occupancy Grid Maps
- Feature-based Maps
- Topological Maps

**Rare Types**: (Some Algorithms Exist which use these map types but are not seen commonly due to memory/processing issues)

- Appearance-based Maps
- Random Probability Maps
- Semantic Maps

---

## 1. Occupancy Grid Map Merging

### 1.1 Probability Method

### 1.2 Optimization Method

- **1.2.1 Objective Function Based on Overlapping**
- **1.2.2 Objective Function Based on Occupancy Likelihood**
- **1.2.3 Objective Function Based on Image Registration**

### 1.3 Feature Based Method

### 1.4 Hough-Transform-Based Method

---

## 2. Feature-Based Map Merging

### 2.1 Point-Feature-Based Map Merging

### 2.2 Line-Feature-Based Map Merging

### 2.3 Plane-Feature-Based Map Merging

---

## 3. Topological Map Merging

---

## 4. Appearance-Based Map Merging

---

## 5. Random Probability Map Merging

---

## 6. Semantic Map Merging

---

# Annotated Paper

# Citation

```

@Article{s20236988,
AUTHOR = {Yu, Shuien and Fu, Chunyun and Gostar, Amirali K. and Hu, Minghui},
TITLE = {A Review on Map-Merging Methods for Typical Map Types in Multiple-Ground-Robot SLAM Solutions},
JOURNAL = {Sensors},
VOLUME = {20},
YEAR = {2020},
NUMBER = {23},
ARTICLE-NUMBER = {6988},
URL = {https://www.mdpi.com/1424-8220/20/23/6988},
PubMedID = {33297376},
ISSN = {1424-8220},
ABSTRACT = {When multiple robots are involved in the process of simultaneous localization and mapping (SLAM), a global map should be constructed by merging the local maps built by individual robots, so as to provide a better representation of the environment. Hence, the map-merging methods play a crucial rule in multi-robot systems and determine the performance of multi-robot SLAM. This paper looks into the key problem of map merging for multiple-ground-robot SLAM and reviews the typical map-merging methods for several important types of maps in SLAM applications: occupancy grid maps, feature-based maps, and topological maps. These map-merging approaches are classified based on their working mechanism or the type of features they deal with. The concepts and characteristics of these map-merging methods are elaborated in this review. The contents summarized in this paper provide insights and guidance for future multiple-ground-robot SLAM solutions.},
DOI = {10.3390/s20236988}
}
```