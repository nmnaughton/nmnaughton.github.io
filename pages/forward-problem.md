---
layout: page

# The title of the page.
title: Forward Problem

---

Diffusion-weighted MRI (dMRI) is goverend by the Bloch-Torrey equation which is a 2nd order, parabolic PDE: <br/> <br/> 
$$\frac{\partial \bm{M}}{\partial t} = -i(\gamma \bm{G} \cdot \bm{x})\bm{M} - \frac{\bm{M}}{T_2} - D \nabla^2 \bm{M}$$.

Solving the Bloch-Torrey equation for different microstrucutral geoemtries allows us to determine what the dMRI signal should be for that particular microstrucutre. Unfortunatly, dMRI in muscle has a resolution size of 1-2 mm while the microstrucutre being meaasured is one the order of 10 microns (0.001 mm). This means that when we measure the dMRI signal, we only measure the voxel average of the dMRI signal

$$ S(t) = \int_{V}|\bm{M}(\bm{x},t)|d\bm{x} $$




