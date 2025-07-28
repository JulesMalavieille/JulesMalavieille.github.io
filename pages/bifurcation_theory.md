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

## Modelling fold bifurcation and Early Warning Signal

This project was carried out during my first research internship in summer 2024. The goal was to model a regime shift using a classical model of *Ips typographus* (spruce bark beetle), and to assess the ability of Early Warning Signals (EWS) to detect an upcoming transition.

The model describes the outbreak dynamics of the spruce worm, which attacks and kills spruce trees. At low densities, tree resilience and reproduction maintain ecosystem stability. However, beyond a critical threshold, the population explodes, rapidly destroying the forest — a classical regime shift through a fold bifurcation.

To capture this dynamic, we used a stochastic differential equation of the form:

$$
\begin{cases}
\frac{dN}{dt} = RN(1-\frac{N}{K}) - \frac{AN^2P}{B^2+N^2} + bW
\end{cases}
$$

where W​ is a Wiener process and the system is integrated using the Milstein scheme for improved accuracy on the noise term.

To anticipate critical transitions, we tested classic Early Warning Signals such as rising variance and autocorrelation. While these indicators provided some predictive power, they showed a high rate of false positives and were sensitive to time resolution and observation lag.

Download the full report : <a href="/assets/fold_bifurcation.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/fold_bifurcation_EWS" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 

## Hopf bifurcation predicting method

I made this work during a research internship in summer 2025. We adapt the model-based method of Boettiger and Hastings (2012) to predict fold bifurcation for Hopf bifurcation. 

In order to anticipate this bifurcation, we compare two stochastical differential equations : one Olstein-Ulenbeck classic model, which can't shift and a second model based on the first one but modified to be able to shift. 

$$
\begin{cases}
dX_{noshift} = (-X\mu_0)dt + \sigma dB\\
dX_{shift} = \sqrt{\mu}(\phi-X)dt + \sigma\sqrt{\phi}dB\\
\mu = \mu_0 + mt
\end{cases}
$$

Then we try to fit the model on data to get the best parameters to simulate the system with the two models. Then we make a big number of simulations and we compare the two models. If in a high number of simulations, the models are significantly different, it means the system is shifting. In the contrary if the two models show a high number of similar dynamics then there is no shift happening. 


