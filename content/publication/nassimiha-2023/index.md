---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Short-term Prediction and Filtering of Solar Power Using State-Space Gaussian Processes
subtitle:
authors:
- Sean Nassimiha
- Peter Dudfield
- Jack Kelly
- Marc Deisenroth
- So Takao
tags: []
categories: [Gaussian processes, solar PV modelling]
date: '2023'
lastmod: 2023-03-30T15:12:17+01:00
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
publishDate: '2023'
publication_types:
- '2'
abstract: Short-term forecasting of solar photovoltaic energy (PV) production is important for powerplant management. Ideally these forecasts are equipped with error bars, so that downstream decisions can account for uncertainty. To produce predictions with error bars in this setting, we consider Gaussian processes (GPs) for modelling and predicting solar photovoltaic energy production in the UK. A standard application of GP regression on the PV timeseries data is infeasible due to the large data size and non-Gaussianity of PV readings. However, this is made possible by leveraging recent advances in scalable GP inference, in particular, by using the state-space form of GPs, combined with modern variational inference techniques. The resulting model is not only scalable to large datasets but can also handle continuous data streams via Kalman filtering.
publication: '*NeurIPS 2022 workshop on Tackling Climate Change with Machine Learning*'
url_pdf: 'https://arxiv.org/pdf/2302.00388'
---