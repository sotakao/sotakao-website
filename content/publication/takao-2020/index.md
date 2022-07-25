---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Stochastic geometric mechanics for fluid modelling and MCMC
subtitle:
authors:
- So Takao
tags: []
categories: [Geometric Mechanics, Differential Geometry, Stochastic PDEs, Statistics]
date: '2021'
lastmod: 2020-05-30T21:26:40+01:00
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
publishDate: '2020'
publication_types:
- '7'
abstract: Geometric mechanics is a mathematical discipline that aims to tie various aspects of classical and quantum mechanics together using differential geometry. Beyond the profound beauty of the theory, it has revolutionsed the way we think about physics. Two important processes however, are not treated traditionally in the framework. These are, noise and dissipation. Indeed, real world dynamical systems such as the weather are inherently noisy and dissipative, therefore having a geometric framework for these processes may potentially bring benefit to our further understanding and modelling of these systems. The purpose of this dissertation is to develop a geometric framework for the inclusion of structure-preserving noise and dissipation into mechanical systems and study their implications in the areas of stochastic fluid dynamics and statistical mechanics. In particular, we study the effect of noise added using this framework on the solution behaviours of certain fluid systems, such as the inviscid Burgers’ equation and transport equation of tensor fields. While the noise does not prevent the formation of singularities in the Burgers’ system, it is shown to restore uniqueness of solutions in the tensor transport equation driven by non-smooth drift. We then proceed to add a type of dissipation that balances the energy influx from the noise, resulting in the preservation of Gibbs measure on phase space. This property is then exploited to construct a novel irreversible MCMC algorithm to sample from Lie groups, and also to study phase transition behaviours in a network model consisting of coupled LiePoisson systems with noise and dissipation.
publication: '*Imperial College London*'
url_pdf: 'https://spiral.imperial.ac.uk/bitstream/10044/1/89597/1/Takao-S-2020-PhD-Thesis.pdf'
---