---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Irreversible Langevin MCMC on Lie groups
subtitle:
authors:
- Alexis Arnaudon
- Alessandro Barp
- So Takao
tags: []
categories: [Geometric Mechanics, Statistics]
date: '2019'
lastmod: 2019-08-27T21:26:40+01:00
katex: true
math: true
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
publishDate: '2019'
publication_types:
- '1'
abstract: It is well-known that irreversible MCMC algorithms converge faster to their stationary distributions than reversible ones. Using the special geometric structure of Lie groups $G$ and dissipation fields compatible with the symplectic structure, we construct an irreversible HMC-like MCMC algorithm on $G$, where we first update the momentum by solving an OU process on the corresponding Lie algebra $\mathfrak{g}$, and then approximate the Hamiltonian system on $G \times \mathfrak{g}$ with a reversible symplectic integrator followed by a Metropolis-Hastings correction step. In particular, when the OU process is simulated over sufficiently long times, we recover HMC as a special case. We illustrate this algorithm numerically using the example $G = SO(3)$.
publication: '*International Conference on Geometric Science of Information*'
url_pdf: 'https://arxiv.org/pdf/1903.08939.pdf'
---