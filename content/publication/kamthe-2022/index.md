---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Iterative State Estimation in Non-linear Dynamical Systems Using Approximate Expectation Propagation
subtitle:
authors:
- Sanket Kamthe
- So Takao
- Shakir Mohamed
- Marc P. Deisenroth
tags: []
categories: [Bayesian Machine Learning, Data Assimilation]
date: '2022'
lastmod: 2022-07-06T21:26:40+01:00
featured: true
draft: false
katex: true
math: true

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
publishDate: '2022'
publication_types:
- '2'
abstract: Bayesian inference in non-linear dynamical systems seeks to find good posterior approximations of a latent state given a sequence of observations. Gaussian filters and smoothers, including the (extended/unscented) Kalman filter/smoother, which are commonly used in engineering applications, yield Gaussian posteriors on the latent state. While they are computationally efficient, they are often criticised for their crude approximation of the posterior state distribution. In this paper, we address this criticism by proposing a message passing scheme for iterative state estimation in non-linear dynamical systems, which yields more informative (Gaussian) posteriors on the latent states. Our message passing scheme is based on expectation propagation (EP). We prove that classical Rauch--Tung--Striebel (RTS) smoothers, such as the extended Kalman smoother (EKS) or the unscented Kalman smoother (UKS), are special cases of our message passing scheme. Running the message passing scheme more than once can lead to significant improvements of the classical RTS smoothers, so that more informative state estimates can be obtained. We address potential convergence issues of EP by generalising our state estimation framework to damped updates and the consideration of general $\alpha$-divergences.
publication: '*Transactions on Machine Learning Research*'
url_pdf: 'https://openreview.net/pdf?id=xyt4wfdo4J'
url_code: 'https://github.com/sanket-kamthe/EPyStateEstimator'
url_video: 'https://www.youtube.com/watch?v=FrTY04gXErY'
---