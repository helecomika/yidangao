---
title: Environment Mapping for Large-Scale Teleoperation
summary: Project at Robotic Systems Lab, ETH Zurich
tags:
  - SLAM
  - 3D
  - robot
date: '2021-11-18T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Volumetric Mapping Pipeline
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

Teleoperation for large scale machinery is currently under development and most solutions rely on streaming high-quality raw images to the operator. However, there is no solution available that recovers the depth information which is one of the most important features for the human operator. 


In this project, we propose a volumetric mapping pipeline by fusing real-time data from onboard camera and lidar, that creates a full 3D map around HEAP and renders a 3rd person view of the machine and its surroundings.
