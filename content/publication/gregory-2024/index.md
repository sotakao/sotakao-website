---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Scalable interpolation of satellite altimetry data with probabilistic machine learning
subtitle:
authors:
- William Gregory
- Ronald MacEachern
- So Takao
- Isobel Lawrence
- Carmen Nab
- Marc Peter Deisenroth
- Michel Tsamados
tags: []
categories: [Gaussian processes, Remote sensing]
date: '2024'
lastmod: 2024-04-08T12:49:14+01:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: 'Smart'
  preview_only: true

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
publishDate: '2024'
publication_types:
- '2'
abstract: In this work, we present a new open-source Python programming library for performing efficient interpolation of non-stationary satellite altimetry data, using scalable Gaussian Process (GP) techniques. We showcase the library, GPSat, by using data from the CryoSat-2, Sentinel-3A, and Sentinel-3B radar altimeters, to generate complete maps of daily 50 km 2-gridded Arctic sea ice radar freeboard. Relative to a previous GP interpolation scheme, we find that GPSat offers a 504× computational speedup, with less than 4 mm difference on the derived freeboards, on average. We then demonstrate the scalability of GPSat through freeboard interpolation at 5 km 2 grid resolution, and Sea-Level Anomalies (SLA) at the resolution of the altimeter footprint. Validation of this novel high resolution radar freeboard product shows strong agreement with airborne data, with a linear correlation of 0.66. Footprint-level SLA interpolation also shows improvements in predictive skill over linear regression, which is a standard approach used in sea ice altimetry data processing. We suggest that GPSat could overcome the computational bottlenecks faced in many altimetry-based interpolation routines. This could in turn lead to improved observational estimates of ocean topography and sea ice thickness, and also further critical understanding of ocean and sea ice variability over short spatio-temporal scales.
publication: '*Nature Communications*'
url_pdf: 'https://www.nature.com/articles/s41467-024-51900-x'
---