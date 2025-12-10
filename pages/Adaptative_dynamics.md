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
In this project I studied the mean size of individual in a population. I assume that competition is a decreasing logistic function with the differnce between the size of the resident and the mutant and the reproduction is a decreasing exponential function of the size. In other words, the bigger you are, the more competitive you are, but you reproduce less and the smaller you are, the less competitive you are but you reproduce more. 

Those hypothesis ar widely verified in a lot of studies, it is all based on energy consumption by organisms. The mutant-resident model following these assumptions is the following :

$$
\begin{cases}
\frac{dN}{dt} = N(r(x) - \alpha(0)N - \alpha(x-x')N' - \frac{\beta P(N+N')}{c^2(N+N')^2})\\        
\frac{dN'}{dt} = N'(r(x') - \alpha(0)N' - \alpha(x'-x)N - \frac{\beta P(N+N')}{c^2(N+N')^2})
\end{cases}
$$

Using this model I show that for a specific range of parameters, specifically when competition is "strong", the mean size of the population is not stable. It fluctuates in regular periodic patern as shown in the following graph. This dynamic can explain a variablility in mean size over time of a population even when environemental conditons don't change. But only if the hypothesis assume ton build this model are verified. 

<p align="center">
  <img src="/assets/cycle.png" width="600px">
</p>

Download the full report : <a href="/assets/EVACO-1.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/Cycling-evolution" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 
