---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Actually Sparse Variational Gaussian Processes
subtitle:
authors:
- Harry Jake Cunningham
- Daniel Augusto de Souza
- So Takao
- Mark van der Wilk
- Marc Deisenroth
tags: []
categories: [Gaussian processes, Variational inference]
date: '2023'
lastmod: 2023-05-02T12:49:14+01:00
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
abstract: Gaussian processes (GPs) are typically criticised for their unfavourable scaling in both computational and memory requirements. For large datasets, sparse GPs reduce these demands by conditioning on a small set of inducing variables designed to summarise the data. In practice however, for large datasets requiring many inducing variables, such as low-lengthscale spatial data, even sparse GPs can become computationally expensive, limited by the number of inducing variables one can use. In this work, we propose a new class of inter-domain variational GP, constructed by projecting a GP onto a set of compactly supported B-spline basis functions. The key benefit of our approach is that the compact support of the B-spline basis functions admits the use of sparse linear algebra to significantly speed up matrix operations and drastically reduce the memory footprint. This allows us to very efficiently model fast-varying spatial phenomena with tens of thousands of inducing variables, where previous approaches failed.
publication: '*International Conference on Artificial Intelligence and Statistics (AISTATS)*'
url_pdf: 'https://proceedings.mlr.press/v206/cunningham23a/cunningham23a.pdf'
---