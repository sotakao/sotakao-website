---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Co-located OLCI optical imagery and SAR altimetry from Sentinel-3 for enhanced Arctic spring sea ice surface classification
subtitle:
authors:
- Weibin Chen
- Michel Tsamados
- Rosemary Willatt
- So Takao
- others
tags: []
categories: [Vision transformer, Remote sensing]
date: '2024'
lastmod: 2024-06-07T21:35:33+01:00
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
abstract: The Sentinel-3A and Sentinel-3B satellites, launched in February 2016 and April 2018 respectively, build on the legacy of CryoSat-2 by providing high-resolution Ku-band radar altimetry data over the polar regions up to 81° North. The combination of synthetic aperture radar (SAR) mode altimetry (SRAL instrument) from Sentinel-3A and Sentinel-3B, and the Ocean and Land Colour Instrument (OLCI) imaging spectrometer, results in the creation of the first satellite platform that offers coincident optical imagery and SAR radar altimetry. We utilise this synergy between altimetry and imagery to demonstrate a novel application of deep learning to distinguish sea ice from leads in spring. We use SRAL classified leads as training input for pan-Arctic lead detection from OLCI imagery. This surface classification is an important step for estimating sea ice thickness and to predict future sea ice changes in the Arctic and Antarctic regions. We propose the use of Vision Transformers (ViT), an approach adapting the popular deep learning algorithm Transformer, for this task. Their effectiveness, in terms of both quantitative metric including accuracy and qualitative metric including model roll-out, on several entire OLCI images is demonstrated and we show improved skill compared to previous machine learning and empirical approaches. We show the potential for this method to provide lead fraction retrievals at improved accuracy and spatial resolution for sunlit periods before melt onset.
publication: 'Frontiers in Remote Sensing'
url_pdf: 'https://www.frontiersin.org/journals/remote-sensing/articles/10.3389/frsen.2024.1401653/full'
---