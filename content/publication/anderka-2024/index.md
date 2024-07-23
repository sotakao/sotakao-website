---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Iterated INLA for State and Parameter Estimation in Nonlinear Dynamical Systems
subtitle:
authors:
- Rafael Anderka
- Marc Deisenroth
- So Takao
tags: []
categories: [Data assimilation, INLA, stochastic PDEs]
date: '2024'
lastmod: 2024-02-26T21:35:33+01:00
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
abstract: Data assimilation (DA) methods use priors arising from differential equations to robustly interpolate and extrapolate data. Popular techniques such as ensemble methods that handle high-dimensional, nonlinear PDE priors focus mostly on state estimation, however can have difficulty learning the parameters accurately. On the other hand, machine learning based approaches can naturally learn the state and parameters, but their applicability can be limited, or produce uncertainties that are hard to interpret. Inspired by the Integrated Nested Laplace Approximation (INLA) method in spatial statistics, we propose an alternative approach to DA based on iteratively linearising the dynamical model. This produces a Gaussian Markov random field at each iteration, enabling one to use INLA to infer the state and parameters. Our approach can be used for arbitrary nonlinear systems, while retaining interpretability, and is furthermore demonstrated to outperform existing methods on the DA task. By providing a more nuanced approach to handling nonlinear PDE priors, our methodology offers improved accuracy and robustness in predictions, especially where data sparsity is prevalent.
publication: 'Uncertainty in Artificial Intelligence'
url_pdf: 'https://arxiv.org/abs/2402.17036'
---