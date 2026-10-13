---
layout: page
title: VAE-QWGAN
permalink: /projects/vae-qwgan/
description: Learning informative latent priors to address mode collapse in quantum generative models.
importance: 1
---

**Quantum Machine Intelligence · 2025**

Quantum generative adversarial networks can repeatedly produce similar samples while missing parts of the data distribution. In this work, we investigate how an autoencoder-informed latent space can help address that mode collapse.

VAE-QWGAN combines a classical variational encoder with a quantum Wasserstein GAN, using data-dependent latent samples during training and a fitted Gaussian mixture prior for generation. Experiments on image datasets assess both sample quality and diversity.

I co-developed this work with **Harry Youel** and **Sharu Theresa Jose** as part of my research on quantum generative modelling.

### Paper

_VAE-QWGAN: addressing mode collapse in quantum GANs via autoencoding priors_. Aaron Mark Thomas, Harry Youel and Sharu Theresa Jose. **Quantum Machine Intelligence 7, 91 (2025)**.

[Read the published paper](https://doi.org/10.1007/s42484-025-00314-z)
