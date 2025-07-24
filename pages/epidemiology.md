---
layout: single
title: "Epidemiological modelling"
permalink: pages/epidemiology/
---

This work was the first full modelling project I carried out, as the final project of my Bachelor's degree, under the supervision of *Guillaume Legland*, researcher at the Mediterranéean Institute of Oceanology.
The objective was to understand how **zooplancton grazing** affects the **viral infection dynamics** of phytoplancton population 

To explore this we build a **system of differential equation** describing the interactions between healthy phytoplancton, infected phytoplankton and zooplancton : 

\[
\text{(dP/dt = aP - c/L*PF - bPZ)}
\]
\[
\text{(dF/dt = c/L*PF - 1/L*F - bFZ)}
\]
\[
\text{(dZ/dt =b(P+F)Z - mZ^2)}
\]


We deduce from the equilibrium and stability of the system that the grazing of pjytoplancton by zooplancton was reducing the amount of infected cells and so the number of viruses reinjected in the system. This reduces the infection of phytoplancton. So by eating the phytoplancton, zooplancton reduce the infection of phytoplancton
