---
title: Improving 3D Line Reconstruction Using SfM Point Cloud
summary: Semester Project at Computer Vision and Geometry Group, ETH Zurich
tags:
  - 3D
date: '2022-10-12T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: 3D Line Reconstruction
  focal_point: Smart


# links:
#   - icon: twitter
#     icon_pack: fab
#     name: Follow
#     url: https://twitter.com/georgecushen
url_code: ''
url_pdf: ''
url_slides: 'https://1drv.ms/p/s!AlfyQGIljYXOd_wqYrThF9uT-bQ?e=uWHDRl&nav=eyJzSWQiOjM1OSwiY0lkIjo0NDgzMzY2ODF9'
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

3D line reconstruction is an useful and effective alternative of the conventional point-based reconstruction, especially for the textureless man-made scenes. Line triangulation however, suffers from many ill-posed problems like degenerated cases
and unmatched endpoints, which largely limits the quality of the resulted reconstruction. 


To meet the challenge, a line mapping system is introduced with a fitnmerge module where depth map can be input to generate 3D line proposals. Our goal for the project is to improve this system so that sparse depth information from point cloud, ideally the Struture-from-Motion (SfM) point cloud, can be used to reconstruct high-quality line structures. 


We propose to use covisible views and depth smaples from neighboring pixels to relax fitting requirements, and we also present point-aided track assignment and aggregation to improve merging accuracy. The key to the success of our modifications lies in making full use of the SfM output, both the point cloud and the point track information, to retrieve 2D - 3D point correspondences, get covisible views and compute point covariance. 


Experiments show significant improvement in completeness and accuracy of the resulted line reconstruction compared to that of
the original system.