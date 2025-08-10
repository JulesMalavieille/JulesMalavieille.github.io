---
layout: single
title: "Projects based on bifurcation theory"
permalink: pages/bifurcation_theory/
---

<!-- Load MathJax -->
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

In complex or chaotic systems, describing precisely how a system evolves can be impossible. In such cases, it is often more practical to identify critical thresholds — the conditions under which the system shifts from one state to another. The study of these thresholds is known as bifurcation theory.

## Hopf bifurcation predicting method

This work was conducted during a research internship in the summer of 2025. The objective was to adapt the model-based method developed by Boettiger and Hastings (2012), originally designed for fold bifurcations, to **detect Hopf bifurcations**.

The method is based on a likelihood-based comparison between two stochastic differential equations models :
  - Null model (Ornstein-Uhlenbeck process), which captures **stationary dynamics** without bifurcation.
  - Test model, which includes a slowly changing control parameter **leading to a Hopf bifurcation**.

$$
\begin{cases}
\text{Null model :} & dX = (-X\mu_0)dt + \sigma dB\\
\text{Test model :} & dX = \sqrt{\mu}(\phi-X)dt + \sigma\sqrt{\phi}dB\\
\mu = \mu_0 + mt
\end{cases}
$$

The approach consists of three main steps:
  - Parameters estimation : Fit both models to time-series data using **maximum likelihood estimation (MLE)**.
  - Simulation-based comparison : Generate many stochastic trajectories from each fitted model.
  - Statistical divergence : Compute a likelihood ratio or a distance metric (e.g., D-statistic) between the two distributions of trajectories.

If the **test model significantly outperforms the null model** in reproducing the observed dynamics, this is interpreted as evidence of an **ongoing shift**, consistent with a Hopf bifurcation. On the contrary, if both models yield similar behavior, the system is considered stable.

Our results demonstrate that **this method is capable of anticipating Hopf bifurcations** in synthetic datasets. This opens the way to generalizing model-based frameworks beyond fold-type transitions to more complex bifurcation structures.

Download the full report : <a href="/assets/Hopf_bifurcation_report.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/Anticipate-Hopf-bifurcation" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 

## Modelling fold bifurcation and Early Warning Signal

This project was carried out during my first research internship in summer 2024. The goal was to **model a regime shift** using a classical model of *Ips typographus* (spruce bark beetle), and to assess **the ability of Early Warning Signals (EWS) to detect an upcoming transition**.

The model describes the outbreak dynamics of the spruce worm, which attacks and kills spruce trees. At low densities, tree resilience and reproduction maintain ecosystem stability. However, beyond a critical threshold, the population explodes, rapidly destroying the forest — a classical regime shift through a fold bifurcation.

To capture this dynamic, we used a **stochastic differential equation** of the form:

$$
\begin{cases}
\frac{dN}{dt} = RN(1-\frac{N}{K}) - \frac{AN^2P}{B^2+N^2} + bW
\end{cases}
$$

where W​ is a Wiener process and the system is integrated using the **Milstein scheme** for improved accuracy on the noise term.

To anticipate critical transitions, we tested classic Early Warning Signals such as **rising variance and autocorrelation**. While these indicators provided some predictive power, they showed a high rate of false positives and were sensitive to time resolution and observation lag.

Download the full report : <a href="/assets/fold_bifurcation.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/fold_bifurcation_EWS" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 

