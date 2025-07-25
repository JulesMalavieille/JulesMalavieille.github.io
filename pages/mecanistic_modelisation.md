---
layout: single
title: "Mecanistic modelisation projects"
permalink: pages/mecanistic_modelisation/
---

<!-- Load MathJax -->
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

## Epidemiological modelling 

This work was the first full modelling project I carried out, as the final project of my Bachelor's degree, under the supervision of Guillaume Legland, researcher at the Mediterranéean Institute of Oceanology.
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

Download the full report : <a href="/assets/epidemiologic_model.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/Epidemiological-modelling" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 

## Conservation strategie for Loggerhead turtle (Caretta caretta)

This project was conducted as part of an advanced modelling course and involved teamwork. The objective was to reproduce and extend the work of Crouse et al. (1987) on the conservation of *Caretta caretta*, the loggerhead sea turtle. At the time, the species was threatened with extinction. The initial conservation plan focused on protecting turtle eggs, but it proved ineffective. The goal of this work was to identify alternative strategies to ensure the survival of the species.

We developed a discrete-time model structured into seven life stages, using a Leslie matrix and Perron-Frobenius theory to analyse long-term population growth. My main contributions included building the model, performing the analytical resolution for abundance in each stage, and conducting sensitivity analysis of the model to key parameter values.

$$
\begin{cases}
N_1(t+1) = \sum(f_kN_k(t)) + N_1(t)(1-v_1-m_1) \\
N_{2->6}(t+1) = N_i(t)(1-v_i-m_i)+v_iN_{i-1}(t) \\
N_7(t+1) = N_7(t)(1-m_7)+v_6N_6(t)
\end{cases}
$$

Model simulations and sensitivity analysis showed that protecting eggs had minimal impact on overall population dynamics. In contrast, improving the survival rate of large juveniles (pre-adults) had a much greater effect on long-term viability. This life stage suffered high mortality rates due to accidental capture in fishing gear. As a result, the most effective conservation strategy was to reduce bycatch, for instance by using turtle-excluder devices in fishing nets.

Download the full report : <a href="/assets/turtle_project.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/Caretta_caretta_conservation" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 







