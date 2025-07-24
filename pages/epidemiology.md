---
layout: single
title: "Epidemiological modelling"
permalink: pages/epidemiology/
---

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
