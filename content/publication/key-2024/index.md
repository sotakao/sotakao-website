---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Scalable Data Assimilation with Message Passing
subtitle:
authors:
- Oscar Key
- So Takao
- Daniel Giles
- Marc Deisenroth
tags: []
categories: [Gaussian Processes, Distirbuted Computing, Data Assimilation]
date: '2024'
lastmod: 2024-04-19T12:49:14+01:00
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
abstract: Data assimilation is a core component of numerical weather prediction systems. The large quantity of data processed during assimilation requires the computation to be distributed across increasingly many compute nodes, yet existing approaches suffer from synchronisation overhead in this setting. In this paper, we exploit the formulation of data assimilation as a Bayesian inference problem and apply a message-passing algorithm to solve the spatial inference problem. Since message passing is inherently based on local computations, this approach lends itself to parallel and distributed computation. In combination with a GPU-accelerated implementation, we can scale the algorithm to very large grid sizes while retaining good accuracy and compute and memory requirements.
publication: '*Climate Informatics*'
url_pdf: 'https://arxiv.org/pdf/2404.12968.pdf'
---