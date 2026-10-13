---
layout: page
title: Same Graph, Different Likelihoods
permalink: /projects/graph-calibration/
description: Testing whether graph generators learn graph structure or the ordering used to represent it.
importance: 2
---

**National Institute of Informatics · AISTATS 2026 calibration workshop**

One graph can be represented by several equivalent sequences. An autoregressive generator may assign these different likelihoods, making its confidence depend on the representation rather than the underlying graph.

We study this effect using permutation-equivalent encodings and **Linearization Uncertainty**, a measure of variation in negative log-likelihood across equivalent sequences. Experiments examine ordering bias and calibration, including the reliability of generated molecular graphs on QM9.

This collaboration grew out of my research internship at the **National Institute of Informatics in Tokyo**.

### Paper

*Same Graph, Different Likelihoods: Calibration of Autoregressive Graph Generators via Permutation-Equivalent Encodings*. Laurits Fredsgaard, Aaron Thomas, Michael Riis Andersen, Mikkel N. Schmidt and Mahito Sugiyama.

Workshop **Towards Trustworthy Predictions: Theory and Applications of Calibration for Modern AI**, AISTATS 2026.

[Read the paper](https://arxiv.org/abs/2604.05613) · [Research code](https://github.com/lauritsf/linearization-uncertainty)
