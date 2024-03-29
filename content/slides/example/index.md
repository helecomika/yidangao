﻿` `![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.001.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.002.png)

**Improving 3D Line  ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.003.jpeg)Reconstruction Using  SfM Point Cloud** 

**Yidan Gao** 

*Supervised by Rémi Pautrat and ShaohuiLiu* 19 September 2022, Zürich 

Background – Line Reconstruction

**Advantage**

- Recover scenes lack of textures
- More semantically recognizable

**Challenges**

- Measurements, degeneracy, track computation, Parameterization, etc.

**Use of Known Geometry**

- Depth map, surface normals, etc.

**Advantage**

- **Recover scenes lack of textures**
- **More semantically recognizable ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.004.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.005.jpeg)**

**Challenges** 

- Measurements, degeneracy, track computation, Parameterization, etc. 

**Use of Known Geometry**

- Depth map, surface normals, etc.

Source: scene *ai\_001\_001* from dataset *Hypersim*, reconstruction result with our recent line mapping pipeline

` `12.10.2022 3![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.007.png)
Background – Line Reconstruction

**Advantage ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.008.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.009.png)**

- Recover scenes lack of textures 
- More semantically recognizable 

**Challenges ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.010.png)**

- **Measurements, degeneracy, track computation, ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.011.png)Parameterization, etc.** 

**Use of Known Geometry ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.012.png)**

- Depth map, surface normals, etc. 

Source: scene *Truck* from dataset *Tanks and Temples*, 2D line detection result using LSD

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.013.png)

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.014.png)

Line representation ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.015.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.016.png)4 or 6?![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.017.png)

` `12.10.2022 4![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.007.png)
Background – Line Reconstruction

**Advantage ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.018.jpeg)**

- Recover scenes lack of textures 
- More semantically recognizable 

**Challenges** 

- Measurements, degeneracy, track computation, Parameterization, etc.

Some studies reconstruct line segments from RGB-D images to facilitate camera pose estimation and 

**Use of Known Geometry** robot localization in SLAM. But the line segments 

- **Depth map, surface normals, etc.** themselves are often noisy.

Source:[ https://www.youtube.com/watch?v=PHGFhixKzC4](https://www.youtube.com/watch?v=PHGFhixKzC4)

combined OPLSD with ORB-SLAM from Watanabe lab

` `12.10.2022 5![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.007.png)
Motivations

**Our recent line mapping system**

- fit-and-merge pipeline

**Limitation in practice**

- Demanding acquisition of depth map

**Information from SfM**

- Sparse depth, point track information, etc.

**Our recent line mapping system ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.019.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.020.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.021.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.022.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.023.png)**

- **fit-and-merge pipeline** 

**fitting into correspondence ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.024.png)3D line candidates graph**

**Limitation in practice ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.025.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.026.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.027.png)**

- Demanding acquisition of depth map **pixel depth**➤ **similarity check**➤![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.028.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.029.png)

current image **neighboring views** 

**Information from SfM ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.030.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.031.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.032.png)**

- Sparse depth, point track information, etc. ➤**rgeefionmemeterinct** ➤**mlienreg itnragc iknsto![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.033.png)**

2D lines 3D lines

**aggregating into** image ids **final line reconstruction 3D line proposals** scores

` `12.10.2022 7![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.007.png)
Motivations ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.034.png)

**Our recent line mapping system ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.020.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.021.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.035.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.022.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.023.png)**

- fit-and-merge pipeline 

**fitting into correspondence ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.024.png)3D line candidates graph**

**Limitation in practice ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.025.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.026.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.027.png)**

- **Demanding acquisition of depth map pixel depth**➤ **similarity check**➤![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.029.png)

current image **neighboring views** 

` `12.10.2022 8![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.007.png)
Motivations ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.034.png)

**Information from SfM**

- Sparse depth, point track information, etc.

➤**geometric** ➤**merging into refinement line tracks**

2D lines 3D![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.033.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.030.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.031.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.032.png) lines

**aggregating into** image ids **final line reconstruction 3D line proposals** scores

` `12.10.2022 ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.007.png)
Motivations

**SfM Cloud**

**Our recent line mapping system ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.019.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.020.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.021.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.036.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.023.png)**

- fit-and-merge pipeline 

**fitting into correspondence ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.024.png)3D line candidates graph**

**Limitation in practice ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.025.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.026.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.027.png)**

- Demanding acquisition of depth map **sparse depth**➤ **similarity check**➤![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.028.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.029.png)

current image **neighboring views** 

**Information from SfM ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.030.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.031.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.032.png)**

- **Sparse depth,**  ➤**rgeefionmemeterinct** ➤**mlienreg itnragc iknsto![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.033.png)**
- **point track information, etc.** 2D lines 3D lines

**aggregating into** image ids **final line reconstruction 3D line proposals** scores

` `12.10.2022 9![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.007.png)
Approach

**Explore the use of sparse depth from the point cloud in a successive manner.**

`  `![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.037.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.038.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.039.jpeg)

MVS Point Cloud Sparsified MVS Point Cloud SfM Point Cloud

Source: scene *Truck* in dataset *Tanks and Temples*, we use it as an example to demonstrate our approach

**Line reconstruction using point clouds from dense to sparse**

- MVS Point Cloud
- Sparsified MVS Point Cloud
- SfM Point Cloud

**Line reconstruction using point clouds from dense to sparse**

- **MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.040.jpeg)**
- Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.041.jpeg)
- SfM Point Cloud 

Line triangulation Line fit-and-merge

- Reduction on redundancy and boost in accuracy
- Demonstrate the robustness and extendibility of our current pipeline

**Line reconstruction using point clouds from dense to sparse**

- MVS Point Cloud
- **Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.042.jpeg)**
- SfM Point Cloud 

Line fit-and-merge

**Line reconstruction using point clouds from dense to sparse**

- MVS Point Cloud
- **Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.043.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.044.jpeg)**
- SfM Point Cloud 

Depth images from MVS cloud vs. from sparsified MVS cloud

- Density and quality of the depth tensor decline significantly

**Line reconstruction using point clouds from dense to sparse**

- MVS Point Cloud
- **Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.043.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.044.jpeg)**
- SfM Point Cloud 

Depth images from MVS cloud vs. from sparsified MVS cloud

- **Density** and quality of the depth tensor decline significantly![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.045.png)

Fewer 2D lines fulfil the minimum requirement for fitting, which requires at least 6 sampled points with known depth

**Line reconstruction using point clouds from dense to sparse**

- MVS Point Cloud
- **Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.043.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.044.jpeg)**
- SfM Point Cloud 

Depth images from MVS cloud vs. from sparsified MVS cloud

- Density and **quality** of the depth tensor decline significantly![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.046.png)

Fewer 2D lines fulfil the minimum inlier percentage for the fitted 3D line model, with background points leaking into foreground making the depth tensor noisy

**Line reconstruction using point clouds from dense to sparse ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.047.png)** All line segment detections

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.048.png) Segments after fitting requirement check ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.049.png) Segments after inlier percentage check

- MVS Point Cloud
- **Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.050.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.051.jpeg)**
- SfM Point Cloud 

Filtering visualization on 2D line detections using LSD

- 2D line candidates elimination due to low inlier ratio
- Depth tensor of higher quality is needed

**Line reconstruction using point clouds from dense to sparse**

- MVS Point Cloud
- **Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.052.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.053.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.054.png)**
- SfM Point Cloud 

Depth image before vs. after hidden point removal line fitnmerge with new depth tensor

- Most hidden surface removal methods require surface reconstruction
- HPR operator: extracting the points that reside on the convex hull of a transformed point cloud, amounts to determining the visible points
- Increase in reconstruction completeness using cleaner depth tensor

**Line reconstruction using point clouds from dense to sparse ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.047.png)** All line segment detections

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.048.png) Segments after fitting requirement check ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.049.png) Segments after inlier percentage check

- MVS Point Cloud
- Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.055.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.056.jpeg)
- **SfM Point Cloud** 

Line fit-and-merge Filtering visualization 

- Point visibility inferable from SfM point track information
- Elimination due to low depth density and inlier ratio

**Line reconstruction using point clouds from dense to sparse ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.047.png)** All line segment detections

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.048.png) Segments after fitting requirement check ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.049.png) Segments after inlier percentage check

- MVS Point Cloud
- Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.055.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.056.jpeg)
- **SfM Point Cloud** 

Line fit-and-merge Filtering visualization 

- Point visibility inferable from SfM point track information
- Elimination due to low **depth density** and **inlier ratio![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.057.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.058.png)**

densify the depth tensor allow more outliers make full use of the current depth

**Line reconstruction using point clouds from dense to sparse ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.047.png)** All line segment detections

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.048.png) Segments after fitting requirement check ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.049.png) Segments after inlier percentage check

- MVS Point Cloud
- Sparsified MVS Point Cloud ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.055.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.056.jpeg)
- **SfM Point Cloud** 

Line fit-and-merge Filtering visualization 

- Point visibility inferable from SfM point track information
- Elimination due to low depth density and inlier ratio
- **New pipeline: more greedy fitting and more robust merging**

` `12.10.2022 21![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)
Approach – Improving 3D Line Reconstruction Using SfM Point Cloud

**Greedy fitting**

- **Generating more / eliminating less 3D line proposals from 2D line detections**

**Greedy fitting** – **Parameter Tuning**

- Minimum inlier percentage: 90% ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.059.png) 40%
- Noisy points account for larger percentage given sparse depth
- RANSAC estimation proves to be effective with up to 90% outliers
- Minimum supporting views: 4![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.060.png)3
- Fewer views pass the fitting check given sparse depth
- Point visibility filtering guarantees the general accuracy of 3D line proposals

**Greedy fitting** – **Covisible Views**

- Densify depth tensor using point observations from covisible views
- SfM detects and matches features with highest confidence for accurate camera pose estimations
- Views with large observation overlaps can recover 2D correspondences that SfM fails to register

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.061.jpeg) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.062.jpeg)

Depth images before vs. after adding observations from covisible views

**Greedy fitting** – **Neighboring Pixels**

- Use better the known depth by considering also the neighboring pixels during point depth sampling
- General depth continuity
- Error in camera pose estimation, line detection, pixel approximation, etc.
- Original sampled pixels
  - Additional neighboring pixels

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.063.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.064.png)

Pixel sampling from 2D line detections

**Robust merging**

- The original merging operates on endpointsof lines, unstable due to sparse depth and greedy fitting
- Input point cloudhas more information than the lines it fits into
- **Incorporate inlier pointsin the fitted line models to merge more robustly**

**Robust merging** – **Point-Aided Merging**

- The correspondence graph is built upon self ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.065.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.066.png)and cross-view similarity measurements, which involves angle (2D, 3D), overlap (2D, 3D), perpendicular distance in 2D and *InnerSeg* distance in 3D

**Robust merging** – **Point-Aided Merging**

- Overlap for 3D lines is sensitive to the configuration ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.065.jpeg)of endpoints
- 2D line detectors are prone to redundant detections![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.067.png)
- Generally shorter 3D lines fitted from sparse depth leads to smaller than actual overlapping ratio

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.068.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.069.png)

**Robust merging** – **Point-Aided Merging**

- **Overlap check:** > 20% line overlap ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.070.png)

**Or > 30% inlier point overlap ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.071.png)**

- Recover more 3D lines that belong to the same line track
- The aggregated line can have more support and better accuracy

**Robust merging** – **WTLS Aggregation**

- The aggregated line is re-estimated using SVD ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.065.jpeg)from only the endpointsof the supporting 3D lines
- Prone to error in the sparse depth setting and less minimum supporting views
- Inlier points and their uncertainties can be exploited to generate more robust and accurate aggregation

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.072.png)

**Robust merging** – **WTLS Aggregation**

- Point uncertainty from SfM model
- Point covariance from motion-only BA

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.073.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.074.png)

- Uncertainty as directional projection of covariance

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.075.png)

**Robust merging** – **WTLS Aggregation**

- Weighted total least squares line fitting
- Weight assignment ➣ Problem formulation

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.076.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.077.png)

- Distance computation where and denote two points on the new ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.078.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.079.png)fitted infinite line. The new endpoints are decided as ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.080.png)the two outermost point projections on the new direction. ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.081.png)

` `12.10.2022 32![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)

Experiments – Settings

- Dataset: Tanks and Temples

➣A benchmark for image-based 3D reconstruction widely used for evaluating MVS

- Line detector: LSD
  - Suitable for outdoor scenes
- SfM pipeline: COLMAP

➣A robust and accurate incremental SfM and MVS reconstruction pipeline

- Provide SfM point cloud, neighboring views, 2D and 3D point correspondences, as well as the dense MVS cloud for evaluation

` `12.10.2022 33![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)
Experiments – Ablation study

- Qualitative results
- Quantitative results
- Analysis
- **Qualitative results ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.082.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.083.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.084.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.085.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.086.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.087.png)**
- Quantitative results ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.088.jpeg) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.089.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.090.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.091.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.092.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.093.png)
- Analysis ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.094.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.095.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.096.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.097.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.098.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.099.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.100.png)

**PT** Parameter Tuning **CV** Covisible Views **NP** Neighboring Pixels

**PM** Point-Aided Merging ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.101.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.102.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.103.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.104.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.105.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.106.png)**WA** WTLS Aggregation 

- Lines are colored based  ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.107.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.108.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.109.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.110.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.111.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.112.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.113.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.101.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.102.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.103.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.106.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.105.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.104.png)on the inlier ratio when  evaluated with threshold  
  - 10mm 
- darker lines correspond  to higher inlier ratio,  indicating better precision Original PT PT+CV PT+CV+NP PT+CV+NP+PM PT+CV+NP+PM+WA
- **Qualitative results ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.082.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.083.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.084.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.085.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.086.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.087.png)**
- Quantitative results ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.088.jpeg) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.089.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.090.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.091.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.092.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.093.png)
- Analysis ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.094.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.095.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.096.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.097.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.098.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.099.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.100.png)

**PT** Parameter Tuning **CV** Covisible Views **NP** Neighboring Pixels

**PM** Point-Aided Merging ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.101.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.102.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.103.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.104.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.105.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.106.png)**WA** WTLS Aggregation 

- Lines are colored based  ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.107.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.108.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.109.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.110.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.111.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.112.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.113.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.101.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.102.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.103.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.106.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.105.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.104.png)on the inlier ratio when  evaluated with threshold  
  - 10mm 
- darker lines correspond  to higher inlier ratio,  indicating better precision Original PT PT+CV PT+CV+NP PT+CV+NP+PM PT+CV+NP+PM+WA
- **Qualitative results ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.082.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.083.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.084.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.085.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.086.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.087.png)**
- Quantitative results ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.088.jpeg) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.089.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.090.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.091.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.092.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.093.png)
- Analysis ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.094.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.095.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.096.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.097.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.098.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.099.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.100.png)

**PT** Parameter Tuning **CV** Covisible Views **NP** Neighboring Pixels

**PM** Point-Aided Merging ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.101.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.102.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.103.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.104.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.105.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.106.png)**WA** WTLS Aggregation 

- Lines are colored based  ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.107.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.108.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.109.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.110.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.111.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.112.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.113.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.101.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.102.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.103.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.106.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.105.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.104.png)on the inlier ratio when  evaluated with threshold  
  - 10mm 
- darker lines correspond  to higher inlier ratio,  indicating better precision Original PT PT+CV PT+CV+NP PT+CV+NP+PM PT+CV+NP+PM+WA
- Qualitative results ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.114.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.115.jpeg)
- **Quantitative results** Scene *Caterpillar* Scene *Truck*
- Analysis ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.116.jpeg)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.117.jpeg)

Scene *Barn* Scene *Church*

**PT** Parameter Tuning ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.118.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.119.jpeg)

**CV** Covisible Views and represent  ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.120.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.121.png)**NP** Neighboring Pixels length recall and inlier percentage **PM** Point-Aided Merging at threshold respectively ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.122.png)

**WA** WTLS Aggregation 

Scene *Courthouse*

- Qualitative results ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.123.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.124.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.125.png)
- Quantitative results 
- **Analysis ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.126.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.127.png)**

**PT** Parameter Tuning ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.128.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.118.png)**CV** Covisible Views ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.129.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.130.png)

**NP** Neighboring Pixels ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.131.png)**PM** Point-Aided Merging **WA** WTLS Aggregation 

` `12.10.2022 40![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)

Conclusion 

- Explored line reconstruction using point clouds of different density levels
- Proposed new fitting and merging methods using sparse SfM point cloud, by exploiting covisible views, 2D – 3D point correspondences, point covariance, etc., from SfM input
- Conducted experiments on scenes of different scales, and significantly improved both completeness and accuracy of the line reconstruction results

` `12.10.2022 41![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)

Future Work 

- More advanced merging method to reduce redundancy and increase accuracy
- Minimum parametrization for infinite lines
- More integrated similarity measurement
- Incorporate lines from fitnmergeinto line triangulation pipeline

` `12.10.2022 42![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.006.png)

` `![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.132.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.002.png)

![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.133.png)  ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.134.png) ![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.135.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.136.png)![](Aspose.Words.13c2cc07-7d3d-444b-bb6a-f23c0f9974a4.137.png)

Improving 3D Line Reconstruction Using SfM Point Cloud

**Yidan Gao**

Master student in Mechanical Engineering yidgao@student.ethz.ch

Supervised by Rémi Pautrat and Shaohui Liu

