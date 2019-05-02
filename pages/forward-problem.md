---
layout: page

# The title of the page.
title: Forward Problem

---
### dMRI and the Bloch-Torrey equation

Diffusion-weighted MRI (dMRI) is governed by the Bloch-Torrey equation which is a 2nd order, parabolic PDE: 

$$\frac{\partial \bm{M}}{\partial t} = -i(\gamma \bm{G} \cdot \bm{x})\bm{M} - \frac{\bm{M}}{T_2} - D \nabla^2 \bm{M}$$ .

Solving the Bloch-Torrey equation for different microstrucutral geoemtries allows us to determine what the dMRI signal should be for that particular microstrucutre. Unfortunatly, dMRI in muscle has a resolution size of 1-2 mm while the microstrucutre being meaasured is one the order of 10 microns (0.001 mm). This means that when we measure the dMRI signal, we only measure the voxel average of the dMRI signal,
<br/> <br/>
$$ S(t) = \int_{V}|\bm{M}(\bm{x},t)|d\bm{x}$$ .

<figure style="float: right; padding-right:20px; padding-top:20px;">
<img src="/assets/img/REV.png"  width="300">     
<figcaption>Chicken skeletal muscle and simplified REV model</figcaption>
</figure>

This averaging smears the signal, making it difficult to directly connect the dMRI measurement with the underlying microstructure. However, because of muscle's semi-periodic structure, it is still possible to infer microstrucutral parameters from the dMRI signal. Muscle consists of many long fibers that are tightly bundled together. By assuming that these fibers all have the same cross-sectional shape and are packed together in the same way we can approximate the muscle strucutre using a simplified model that we call a Representative Elementary Volume (REV). This REV model allows us parameterize the model and unerstand how changes in these microstrucutral parameters (for example, the cell diameter) lead to changes in the dMRI signal. 


<figure style="float: right; padding-top:150px;  padding-left:20px;">
<img src="/assets/video/REV-animation.gif"  width="400">     
<figcaption>evolution of dMRI signal in REV model</figcaption>
</figure>

### Solving the Bloch-Torrey equation

Solving the Bloch-Torrey equation can be done analytically over simple shapes, however, over more complex domains such as the REV, it is necessary to use numerical methods. We use the lattice Boltzmann method which is an efficient solution technique that can be easily parallelized to take advantage of high performance computing (HPC) resources \[1\]. Thanks to a startup allocation from [XSEDE](https://xsede.org/), we have shown that the model can efficiently scale to over 160 cores on [SDSU's](https://www.sdsc.edu/) Comet cluster. 

### Validating existing models

Using this LBM model we have an accurate solution of the Bloch-Torrey equation that make few assumtions about the dMRI physics. This allows us to treat is as an in silico phantom that can be used to validate new and existing models of dMRI \[2\]. The advantage of using an in silico phantom is exact knowledge of the underlying microstrucutre, something that is very difficult to measure in real biological tissue. This allows rigours validation that model are able to capture the underlying strucutral behaviro and physcis of dMRI before applying them to the more complex case of real biological tissue where noise and difficulty in verifying the underlying tissue complicate the validation process. 

### Sensitivity analysis

Another advantage of having this in silico phantom is being able to easily change the microstrucutral parameters to see how these changes effect the dMRI signal. By doing this in a systematic fashion we can perform a sensitivity analysis to understand how changes in tissue mcirostruture and dMRI pulse parameters lead to changes in the dMRI signal \[3\]. Understanding this sensitivity helps us interpret dMRI measurements and also design pulse sequences that able to efficently encode microstrucutral information. Both of these insights are important in giving us the correct cools to accuratly solve the [inverse problem](/pages/inverse-problem/).

### References
\[1\] Naughton NM, Tennyson C, and Georgiadis JG. Lattice Boltzmann method for simulation of diffusion magnetic resonance imaging physics in heterogeneous tissue models. Journal of Computational Physics, (under review).

\[2\] Naughton NM and Georgiadis JG. Comparison of two-compartment exchange and continuum models of dMRI in skeletal muscle. Physics in Medicine and Biology, (in revision).

\[3\] Naughton, N. and Georgiadis J., “Global Sensitivity Analysis of Skeletal Muscle dMRI: Effects of Microstructural and PGSE Pulse Parameters,” Magnetic Resonance in Medicine, (in preparation).
