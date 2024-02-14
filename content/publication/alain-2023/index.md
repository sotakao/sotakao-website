---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Gaussian Processes on Cellular Complexes
subtitle:
authors:
- Mathieu Alain
- So Takao
- Brooks Paige
- Marc Deisenroth
tags: []
categories: [Gaussian processes, Algebraic topology, Cellular complexes]
date: '2023'
lastmod: 2023-11-02T12:49:14+01:00
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
abstract: In recent years, there has been considerable interest in developing machine learning models on graphs in order to account for topological inductive biases. In particular, recent attention was given to Gaussian processes on such structures since they can additionally account for uncertainty. However, graphs are limited to modelling relations between two vertices. In this paper, we go beyond this dyadic setting and consider polyadic relations that include interactions between vertices, edges and one of their generalisations, known as cells. Specifically, we propose Gaussian processes on cellular complexes, a generalisation of graphs that captures interactions between these higher-order cells. One of our key contributions is the derivation of two novel kernels, one that generalises the graph Mat\'ern kernel and one that additionally mixes information of different cell types.
publication: 'Preprint'
url_pdf: 'https://arxiv.org/pdf/2311.01198.pdf'
---