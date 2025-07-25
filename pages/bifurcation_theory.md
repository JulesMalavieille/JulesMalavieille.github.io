---
layout: single
title: "Theory of dynamical system and bifurcations"
permalink: pages/bifurcation_theory/
---

<!-- Load MathJax -->
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

## Modelling fold bifurcation and Early Warning Signal

This project was carried out during my first research internship with Jean-Christophe Poggiale in summer 2024. The goal was to model a regime shift using a classical model of Ips typographus (spruce bark beetle), and to assess the ability of Early Warning Signals (EWS) to detect an upcoming transition.

The model describes the outbreak dynamics of the spruce worm, which attacks and kills spruce trees. At low densities, tree resilience and reproduction maintain ecosystem stability. However, beyond a critical threshold, the population explodes, rapidly destroying the forest — a classical regime shift through a fold bifurcation.

To capture this dynamic, we used a stochastic differential equation of the form:

$$
\begin{cases}
\frac{dN}{dt} = RN(1-\frac{N}{K}) - \frac{AN^2P}{B^2+N^2} + bW
\end{cases}
$$

where WtWt​ is a Wiener process and the system is integrated using the Milstein scheme for improved accuracy on the noise term.

To anticipate critical transitions, we tested classic Early Warning Signals such as rising variance and autocorrelation. While these indicators provided some predictive power, they showed a high rate of false positives and were sensitive to time resolution and observation lag.


