---
layout: page

# The title of the page.
title: Forward Problem

---

Diffusion-weighted MRI (dMRI) is goverend by the Bloch-Torrey equation whcih is a 2nd order, parabolic PDE: 

\begin{equation}\label{B-T eq} 
\frac{\partial \bm{M}(\bm{x},t)}{\partial t} = 
-i(\gamma \bm{G}(t)\cdot \bm{x})\bm{M}(\bm{x},t) - \frac{\bm{M}(\bm{x},t)}{T_2} - \nabla\cdot(D(\bm{x})\nabla \bm{M})
\end{equation}
