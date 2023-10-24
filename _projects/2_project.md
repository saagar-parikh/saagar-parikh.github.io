---
layout: page
title: BIJAX - Bayesian Inference in JAX
description:
img: assets/img/3.jpg
importance: 2
category: work
giscus_comments: false
github: https://github.com/saagar-parikh/bijax
---

- Contributed to an open-source Python library with a unified and transparent approach for various distribution approximation techniques such as Laplace Approximation and Markov Chain Monte Carlo (MCMC) sampling.
- Reinforced the approximation methods by adding extensive functionalities such as Full rank, Low rank, Mean Field, Subnetwork, Last Layer, and Kronecker-Factored Approximate Curvature (KFAC).

### Laplace Approximation

The results of Laplace Approximation for fully bayesian network, last-layer bayesian network, and subnet bayesian network are shown in the figures below.

<p align="center"><img src="/assets/img/bijax-hmc-results.png" width="100%">Laplace Approximation using all layers for regression on a 2D dataset. MAP, fullrank, lowrank, diag, kron (left to right)
<p align="center"><img src="/assets/img/bijax-hmc-results.png" width="80%">Laplace Approximation using last layer for regression on a 2D dataset. MAP, fullrank, diag, kron (left to right)
<p align="center"><img src="/assets/img/bijax-hmc-results.png" width="40%">Laplace Approximation using subnetwork for regression on a 2D dataset. MAP, fullrank (left to right)

### Hamiltonian Monte Carlo (HMC) on the Digits dataset

For the case of out of distribution data (the letter 'A' is out of distribution for a dataset of digits), a deterministic model, would predict a class with a certain confidence.
We define an uncertainty metric 'entropy' which provides information on how uncertain the model is (higher is more uncertain). The results below show that the HMC model predicts a class with low confidence and high entropy.

<p align="center"><img src="/assets/img/bijax-hmc-results.png" width="40%">
Ground Truth, Predicted Class, Predicted Class Probability and Entropy
</p>

### Accuracy and Timing Analysis

<table>
  <tr>
    <td><p align="center"><figure><img src="/assets/img/bijax-acc.png", width="100%"><figcaption>Comparable accuracies for different models</figcaption></figure></p></td>
    <td><p align="center"><figure><img src="/assets/img/bijax-timing", width="100%"><figcaption>Time taken for training different models</figcaption></figure></p></td>
  </tr>
</table>

