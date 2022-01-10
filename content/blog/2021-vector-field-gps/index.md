---
title: Vector-valued Gaussian Processes on Riemannian Manifolds via Gauge Independent Projected Kernels
authors: [So Takao, Alex Terenin]
url_pdf: https://arxiv.org/pdf/2110.14423
url_code: https://github.com/MJHutchinson/ExtrinsicGaugeIndependentVectorGPs
date: 2021-12-03
lastmod: 2021-12-03
katex: true
math: true
# View.
#   1 = List
#   2 = Compact
#   3 = Card
view: 2

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Placement options: 1 = Full column width, 2 = Out-set, 3 = Screen-width
# Focal point options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
image:
  placement: 2
  focal_point: ""
  preview_only: true


featured: true
draft: false
---

Gaussian processes are machine learning models capable of learning unknown functions with uncertainty. Motivated by a desire to deploy Gaussian processes in novel areas of science, we present a new class of GPs that model random vector fields on Riemannian manifolds that is (1) mathematically sound, (2) constructive enough for use by machine learning practitioners and (3) trainable using standard methods such as inducing points. In this blogpost, we give a digest version of our paper, illustrating the main results and ideas.

# Nomenclature

- $\Omega$ : sample space
- $X$ : a smooth $d$-dimensional manifold
- $TX$ : the tangent bundle of $X$
- $T^\*X$ : the cotangent bundle of $X$
- $\Gamma(TX)$ : sections of $TX$ (i.e. the space of vector fields on $X$)

# Gaussian random vector fields

## The definition

We introduce the appropriate notion of a Gaussian random vector field as thus.

__Definition (\*):__ A random vector field $f : \Omega \rightarrow \Gamma(TX)$ is _Gaussian_ if for any points $x\_1, \ldots, x\_n \in X$ on the manifold, the vectors $f(x\_1),\ldots,f(x\_n)$ attached to it are jointly Gaussian distributed (in a sense made more precise in the paper).

While this is a neat definition, we also want to characterise vector fields in terms of a mean function and a kernel in order for them to be useful in practice. The former notion is clear: the mean of a Gaussian vector field should just be an ordinary vector field that will determine the mean vector at all finite-dimensional marginals. On the other hand, generalising matrix-valued kernels is less obvious as it is not clear what the appropriate notion of a `matrix' should be in the geometric setting.

<div class="row justify-content-center">
<div class="col-12">
<img class="img-fluid" alt="Discretization drift" src="/img/blog/vector-field-gps/examples.png">
</div>
<div class="col-12">
<p class="text-center">
Examples of Gaussian random vector fields on the torus (left) and the Klein bottle (right).
</p>
</div>
</div>


## The correct notion of a kernel

We claim that the correct notion of a kernel for Gaussian random vector fields is actually given by a _scalar-valued_ function
$$
k : T^\*X \times T^\*X \rightarrow \mathbb{R}
$$
that satisfies the following key properties:

1. Symmetry: for all $\alpha, \beta \in T^\*X$, $k(\alpha, \beta) = k(\beta, \alpha)$ holds.
2. Fibrewise bilinearity: for any pairs of points $x, x' \in X$,
$$
k(\lambda \alpha\_x + \mu \beta\_x, \gamma\_{x'}) = \lambda k(\alpha\_x, \gamma\_{x'}) + \mu k(\beta\_x, \gamma\_{x'})
$$
holds for any $\alpha\_x, \beta\_x \in T^\*\_x X$, $\gamma\_{x'} \in T^\*\_{x'} X$ and $\lambda, \mu \in \mathbb{R}$.
3. Positive definiteness: for any $\alpha\_{1}, \ldots, \alpha\_{n} \in T^\*X$, we have
$$
\sum\_{i=1}^n\sum\_{j=1}^n k(\alpha\_{i}, \alpha\_{j}) \geq 0.
$$

We know that this is precisely the notion we need, due to the following result.

__Theorem:__ A Gaussian random vector field $f$, in the sense of Definition $(\*)$, is fully characterised by a mean vector field and a kernel function in the above sense.


# Projected kernels

To proceed towards numerical implementation of Gaussian vector fields, we rely on an extrinsic geometric approach, detailed as follows:

1. Embed the manifold isometrically into a higher-dimensional Euclidean space $\mathbb{R}^{d'}$, which is always possible by the *Nash embedding theorem*.

2. Construct a vector-valued Gaussian process $\boldsymbol{f} : X \rightarrow \mathbb{R}^{d'}$ in the usual sense with a matrix-valued kernel $\boldsymbol{\kappa} : X \times X \rightarrow \mathbb{R}^{d'} \times \mathbb{R}^{d'}$.

3. Comb out the resulting field so that they become tangential to the manifold, giving us a vector field.

This general procedure is illustrated in the Figure below. We call the kernel that results from the third step a *projected kernel*, which is (1) indeed a kernel, and (2) no expressivity is lost, meaning that every kernels $k : T^\*X \times T^\*X \rightarrow \mathbb{R}$ arise this way. Thus, once we set a matrix-valued kernel $\boldsymbol{\kappa} : X \times X \rightarrow \mathbb{R}^{d'} \times \mathbb{R}^{d'}$ taking values in the higher dimensional space (this can be done for example by using scalar-valued Riemannian manifold GPs[^gprm] as building blocks), we obtain workable kernels for Gaussian random vector fields that is also very general.


<div class="row justify-content-center">
<div class="col-12">
<img class="img-fluid" alt="Discretization drift" src="/img/blog/vector-field-gps/projection-process.png">
</div>
<div class="col-12">
</div>
</div>


# Variational approximations

To enable efficient training of the GP, we also consider variational inference methods in the Gaussian random vector field setting. In variational inference, a parameterised approximation to the exact posterior distribution is obtained through various methods, making inference more tractable. While in general these procedures may not necessarily yield truly geometric approximate posteriors (i.e. satisfy appropriate transformation rules under change of frames[^fm]), fortunately, in a vast majority of approximation methods, such as the Titsias inducing point framework[^vfe], the obtained posteriors can be checked to be geometrically consistent. This allows us therefore to use said methods directly out of the box, with almost no modification to the code.


# Example

Here, we demonstrate a use case of the developed model on the problem of interpolating the global wind field from satellite observations. Interpolating weather fields accurately with well-calibrated uncertainty is crucial for initialising weather models, and we illustrate the benefit of using a geometrically consistent model over a naive implementation using Euclidean GPs.

<div class="row justify-content-center">
<div class="col-12">
<img class="img-fluid" alt="Discretization drift" src="/img/blog/vector-field-gps/wind-experiment.png">
</div>
<div class="col-12">
<p class="text-center">
Wind interpolation using a Euclidean vector-valued GP (top) and Riemannian vector-valued GP (bottom)
</p>
</div>
</div>

From the figure, we see that the uncertainties in the Euclidean vector-valued GP become unnaturally distorted as the satellite approaches the poles, while the Riemannian case has a uniform band along the observations. In addition, the Euclidean case gives rise to a spurious discontinuity in the uncertainty along the solid pink line, which indicates the latitudinal boundary when projected onto the plane.

# Summary

We have developed techniques that generalise Gaussian processes to model vector fields on Riemannian manifolds by first providing a well-defined notion of such processes and then introducing an explicit method to construct them. In addition to this, we have seen that standard Gaussian process training methods, such as variational inference, are compatible with the geometry, hence can be used safely within our framework. In an initial demonstration of our technique on the wind observation data, we have shown that it can be used successfully to interpolate global wind field with geometrically consistent uncertainty bars. We hope that our work inspires the use of GPs as easy and flexible means of modelling vector fields on manifolds in a variety of applications.


## References

[^gprm]: V. Borovitskiy, P. Mostowsky, A. Terenin, and M. P. Deisenroth. Matérn Gaussian processes on Riemannian Manifolds. NeurIPS, 2020.

[^vfe]: M. Titsias. Variational Learning of Inducing Variables in Sparse Gaussian Processes. AISTATS, 2009.

[^fm]: A _frame_ in differential geometry is an object that provides a "coordinate system" which we can use to study vector fields using the language of linear algebra. A truly "geometric'' object such as a vector field should not depend on the choice of a frame.
