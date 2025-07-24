---
layout: single
title: "Epidemiological modelling"
permalink: pages/epidemiology/
---

<!-- Load MathJax -->
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

This work was the first full modelling project I carried out, as the final project of my Bachelor's degree, under the supervision of *Guillaume Legland*, researcher at the Mediterranéean Institute of Oceanology.
The objective was to understand how **zooplancton grazing** affects the **viral infection dynamics** of phytoplancton population 

To explore this we build a **system of differential equation** describing the interactions between healthy phytoplancton, infected phytoplankton and zooplancton : 

$$
\begin{cases}
\frac{dP}{dt} = aP - \frac{c}{L}PF - bPZ \\
\frac{dF}{dt} = \frac{c}{L}PF - \frac{1}{L}F - bFZ \\
\frac{dZ}{dt} = b(P+F)Z - mZ^2
\end{cases}
$$

By analyzing the **equilibria and stability** of the model, we found that zoopkancton grazing significantly reduces the number of infected phytoplankton. This led to fewer infectious cells in the environement. Thus **lowering the infection pressure** on the phytoplankton population.

In other words, by consuming phytoplankton, zooplankton indirectly helped to limit the spread of phytoplanktonic viral infection. This result highlights the importance of trophic intercations in the control of ecological diseases.

Download the full report : <a href="assets/epidemiological_model.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/Epidemiological-modelling" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 
