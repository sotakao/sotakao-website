---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Vector-valued Gaussian Processes on Riemannian Manifolds via Gauge Independent Projected Kernels
subtitle: ''
summary: 'Vector-valued Gaussian Processes on Riemannian Manifolds via Gauge Independent Projected Kernels'
authors:
- Michael J. Hutchinson
- Alexander Terenin
- Viacheslav Borovitskiy
- So Takao
- Yee Whye Teh
- Marc P. Deisenroth
tags: []
categories: [Bayesian Machine Learning]
date: '2021-12-06'
lastmod: 2021-09-28T21:26:40+01:00
featured: true
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
publishDate: '2021-11-06T00:26:39.918381Z'
publication_types:
- '1'
abstract: Gaussian processes are machine learning models capable of learning unknown functions in a way that represents uncertainty, thereby facilitating construction of optimal decision-making systems. Motivated by a desire to deploy Gaussian processes in novel areas of science, a rapidly-growing line of research has focused on constructively extending these models to handle non-Euclidean domains, including Riemannian manifolds, such as spheres and tori. We propose techniques that generalize this class to model vector fields on Riemannian manifolds, which are important in a number of application areas in the physical sciences. To do so, we present a general recipe for constructing gauge independent kernels, which induce Gaussian vector fields, i.e. vector-valued Gaussian processes coherent with geometry, from scalar-valued Riemannian kernels. We extend standard Gaussian process training methods, such as variational inference, to this setting. This enables vector-valued Gaussian processes on Riemannian manifolds to be trained using standard methods and makes them accessible to machine learning practitioners.
publication: '*Advances in Neural Information Processing Systems (NeurIPS)*'
url_code: 'https://github.com/MJHutchinson/ExtrinsicGaugeIndependantVectorGPs'
url_pdf: 'https://openreview.net/pdf?id=FwVmM8Zol_8'
---
