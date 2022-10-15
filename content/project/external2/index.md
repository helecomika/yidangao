---
title: COLMAPSLAM - An Offline Python SLAM Using COLMAP
summary: Group Project at Computer Vision and Geometry Group, ETH Zurich
tags:
  - SLAM
date: '2022-02-06T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: COLMAPSLAM Pipeline
  focal_point: Smart


# links:
#   - icon: twitter
#     icon_pack: fab
#     name: Follow
#     url: https://twitter.com/georgecushen
# url_code: ''
# url_pdf: ''
# url_slides: 'https://docs.google.com/presentation/d/1Rx4WzfT4DabkQ8hx0j0083zZKl9ZsGW5/edit?usp=sharing&ouid=101736090028508638112&rtpof=true&sd=true'
# url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

We present COLMAPSLAM, an offline python SLAM using COLMAP that is robust, accurate, and highly extensible. The new system is built to leverage the advantages of both COLMAP and ORB-SLAM, the former known for its high-quality reconstruction and the latter for its efficient tracking of sequential data. 


Starting with COLMAP pipeline built with components in Hloc and PyCOLMAP, our approach introduces the keyframe selection, covisibility graph, and loop closure to improve the speed and alleviate scale drift of the vanilla COLMAP. 


Extensive experiments are conducted on standard SLAM benchmarks, including TUM-RGBD (indoor) and KITTI (outdoor) datasets. The results show that COLMAPSLAM achieves a much faster speed than COLMAP, better reconstruction against ORB-SLAM2, and the same level of trajectory accuracy as both.


Our code package will soon be made available for the use and further development of the vision community.