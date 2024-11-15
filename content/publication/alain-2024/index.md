---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Gaussian Processes on Cellular Complexes
subtitle:
authors:
- Mathieu Alain
- So Takao
- Xiaowen Dong
- Bastian Rieck
- Emmanuel Noutahi
tags: []
categories: [Gaussian processes, Classification, Edge features, Hodge decomposition]
date: '2024'
lastmod: 2024-11-02T12:49:14+01:00
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
abstract: The problem of classifying graphs is ubiquitous in machine learning. While it is standard to apply graph neural networks or graph kernel methods, Gaussian processes can be employed by transforming spatial features from the graph domain into spectral features in the Euclidean domain, and using them as input points. However, this approach only takes into account features on vertices, whereas some graph datasets also support features on edges. In this work, we present a Gaussian process-based classification algorithm that can leverage one or both vertex and edges features. Furthermore, we take advantage of the Hodge decomposition to better capture the intricate richness of vertex and edge features, which can be beneficial on diverse tasks.
publication: '*NeurIPS 2024 workshop on Bayesian Decision-making and Uncertainty*'
url_pdf: 'https://arxiv.org/pdf/2410.10546'
---