---
layout: page

# The title of the page.
title: Forward Problem

---

Diffusion-weighted MRI (dMRI) is goverend by the Bloch-Torrey equation which is a 2nd order, parabolic PDE: 

$$\frac{\partial \bm{M}}{\partial t} = -i(\gamma \bm{G} \cdot \bm{x})\bm{M} - \frac{\bm{M}}{T_2} - D \nabla^2 \bm{M}$$ .

Solving the Bloch-Torrey equation for different microstrucutral geoemtries allows us to determine what the dMRI signal should be for that particular microstrucutre. Unfortunatly, dMRI in muscle has a resolution size of 1-2 mm while the microstrucutre being meaasured is one the order of 10 microns (0.001 mm). This means that when we measure the dMRI signal, we only measure the voxel average of the dMRI signal,
<br/> <br/>
$$ S(t) = \int_{V}|\bm{M}(\bm{x},t)|d\bm{x}$$ .

<figure style="float: right; padding-top:20px;">
<img src="/assets/video/REV-animation.gif"  width="400">     
<figcaption>evolution of dMRI signal in REV model</figcaption>
</figure>

This averaging smears the signal, making it difficult to directly connect the dMRI measurement with the underlying microstructure. However, because of muscle's semi-periodic structure, it is still possible to infer microstrucutral parameters from the dMRI signal. Muscle consists of many long fibers that are tightly bundled together. By assuming that these fibers all have the same cross-sectional shape and are packed together in the same way we can approximate the muscle strucutre using a simplified model that we call a Representative Elementary Volume (REV). This REV model allows us parameterize the model and unerstand how changes in these microstrucutral parameters (for example, the cell diameter) lead to changes in the dMRI signal. 

Solving the Bloch-Torrey equation can be done analytically over simple shapes, however, over more complex domains such as the REV, it is necessary to use numerical methods. We use the lattice Boltzmann method 


