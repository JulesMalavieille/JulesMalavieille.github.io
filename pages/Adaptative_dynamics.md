---
layout: single
title: "Adaptative dynamics projects"
permalink: pages/bifurcation_theory/
---

<!-- Load MathJax -->
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

The adaptative dynamics theory provides a set of mathematical tools and framework to modelise evolution over time for a specific evolutionary trait. 

## Evolutionary cycle under predation and asymetric competition
In this project I studied the mean size of individual in a population. I assume that competition is a decreasing logistic function with the differnce between the size of the resident and the mutant and the reproduction is a decreasing exponential function of the size. In other words, the bigger you are, the more competitive you are, but you reproduce less and the smaller you are, the less competitive you are but you reproduce more. Those hypothesis ar widely verified in a lot of studies, it is all based on energy consumption by organisms. The mutant-resident model following these assumptions is the following :

$$
\begin{cases}
\frac{dN}{dt} = N(r(x) - \alpha(0)N - \alpha(x-x')N' - \frac{\beta P(N+N')}{c^2*(N+N')^2})\\        
\frac{dN'}{dt} = N'(r(x') - \alpha(0)N' - \alpha(x'-x)N - \frac{\beta P(N+N')}{c^2*(N+N')^2})
\end{cases}
$$

Using this model I show that for a specific range of parameters, specifically when competition is "strong" then the mean size of the population is not stable, it fluctuates in regular patern as shown in the following graph :

<figure class="half">
  <img src="assets/cycle.png" alt="Cycle" style="width:30%">
  <figcaption style="font-size: 1.3em; font-weight: bold;">Evolutionary cycle</figcaption>
</figure>
