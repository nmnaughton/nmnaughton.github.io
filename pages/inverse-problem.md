---
layout: page

# The title of the page.
title: Inverse Problem

---
### Estimating muscle microstructure from dMRI measurements

The inverse problem, as its name implies, is ultimately about working in the inverse direction as the forward problem. We are trying to use the dMRI signal that is measured when you get an MRI and from it infer the microstructural properties of your muscle. Going from the dMRI signal to the underlying microstrucutre is not straight forward. Often, models of the forward problem are used the possible microstrucutral parameters are varied untill the predicted dMRI signal matches the measured dMRI signal. These microstrucutre predictions can then be compared with the numerical LBM model to determine if they accurate capture changes in microstruture /[1/]. This often requires many model evaluations so having a computational efficient model is important. 

### Meta-model of Bloch-Torrey equation

<figure style="float: right; padding-top:20px;  padding-left:20px; ">
<img src="/assets/img/diameter-fingerprint.png"  width="400">     
<figcaption>example of a pulse 'fingerprint' for radial diffusivity</figcaption>
</figure>

The numerical LBM model of dMRI is computationally expensive. To allow for faster estimation, we can use a meta-model of the LBM mdoel. A meta-model is a model of a model, it models the relationsip between the input and the output of the underlying model with no regard for the actual physics \[1, 2\]. Since we are often just trying to adjust the microstrucutral paraemters to match the measured dMRI signal, this is perfect for our needs. The meta-model fits a polynomial to previous results from the numerical LBM model. This yields a polynomial which is much faster to evaluate than solving the numerical LBM model while retaining much of the accuracy. One use of this meta-model is being able to easily see how changes in different parameters

### PGSE pulse optimization for microstruture encoding

<figure style="float: left; padding-top:20px;  padding-right:20px; ">
<img src="/assets/img/final_parameter_selection.PNG"  width="400">     
<figcaption>dMRI pulse optimization for microstructure encoding</figcaption>
</figure>

### Inverting the numerical LBM model

While the numerical LBM model is slow, it is still the most accurate model available. Because of this, it is a useful test canaditie to show that it is possible to recover 

### Machine Learning Models

### References

\[2\] Naughton NM, Gallo NR, Anderson AT, and Georgiadis JG. Comparison of dMRI Models for Skeletal Muscle Microstructure Estimations with Numerical Simulations and Myocardial Porcine Phantom. ISMRM Annual Meeting (May 2019), Montreal, Canada (poster)

\[1\] Naughton NM and Georgiadis JG. Connecting Diffusion MRI to Skeletal Muscle Microstructure: Leveraging Meta-Models and GPU-acceleration. PEARC 2019 (July 2019), Chicago, Illinois (platform presentation)

\[3\] Naughton NM, Jain A, and Georgiadis JG. Polynomial Meta-Model of Bloch-Torrey Equation for Track-based Regularization of Microstructural Inversion. ISMRM Annual Meeting (May 2019), Montreal, Canada (poster)

\[4\] Naughton NM, Wang A, and Georgiadis JG. Fascicle Ellipticity as an Explanation of Transverse Anisotropy in Diffusion MRI Measurements of Skeletal Muscle. ISMRM Annual Meeting (May 2019), Montreal, Canada (poster)

\[5\] Naughton NM, Gallo NR, Anderson AT, and Georgiadis JG. Microstructural Parameter Estimation of Skeletal Muscle using Random Forest Model of dMRI. ISMRM Annual Meeting (May 2019), Montreal, Canada (poster)

\[6\] Naughton NM, Gallo NR, Vaicik M, Anderson AT, Sutton BP, and Georgiadis JG. “Estimation of Extracellular Matrix Diffusion Properties in Decellularized Porcine Myocardium from DTI” ISMRM Annual Meeting (June 2018), Paris, France (poster)
