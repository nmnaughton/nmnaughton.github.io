---
layout: page

# The title of the page.
title: Inverse Problem

---
### Estimating muscle microstructure from dMRI measurements

The inverse problem, as its name implies, is ultimately about working in the inverse direction as the [forward problem](/pages/forward-problem/). We are trying to use the dMRI signal that is measured when you get an MRI and from it infer the microstructural properties of your muscle. Going from the dMRI signal to the underlying microstrucutre is not straight forward. Often, models of the forward problem are used the possible microstrucutral parameters are varied untill the predicted dMRI signal matches the measured dMRI signal. These microstrucutre predictions can then be compared with the numerical LBM model to determine if they accurate capture changes in microstruture \[2, 5\]. This often requires many model evaluations so having a computational efficient model is important. 

### Meta-model of Bloch-Torrey equation

<figure style="float: right; padding-top:40px;  padding-left:20px; ">
<img src="/assets/img/diameter-fingerprint.png"  width="400">     
<figcaption>fractional anisotropy for changes in diameter and diffusion time</figcaption>
</figure>

The numerical LBM model of dMRI is computationally expensive. To allow for faster estimation, we can use a meta-model of the LBM mdoel. A meta-model is a model of a model, it models the relationsip between the input and the output of the underlying model with no regard for the actual physics \[1, 3\]. Since we are often just trying to adjust the microstrucutral paraemters to match the measured dMRI signal, this is perfect for our needs. The meta-model fits a polynomial to previous results from the numerical LBM model. This yields a polynomial which is much faster to evaluate than solving the numerical LBM model while retaining much of the accuracy. One use of this meta-model is being able to easily see how changes in different parameters lead to changes in the measured dMRI signal. For example, we can look at how a change in cell diameter affects fractional anisotorpy (FA). Even more interesting, we can also see how measuring the dMRI at different diffusion times also leads to chagnes in FA. By measuring at multiple diffusion times we can get a 'fingerprint' for a specific cell diameter. 

### PGSE pulse optimization for microstruture encoding

<figure style="float: left; padding-top:20px;  padding-right:30px; ">
<img src="/assets/img/final_parameter_selection.PNG"  width="400">     
<figcaption>dMRI pulse optimization for microstructure encoding</figcaption>
</figure>

Identifying these fingerprints for different combinations of microstrucutral parameters will help us estimate microstructure from the dMRI signal, but we also want to know what types of dMRI pulses will best allow us to do this. Being able to aquire the same microstruutral information using fewer pulse sequences leads to shorter aquisition times, something anyone who has ever had an MRI can appreciate. Using the meta-mdoel we can look at which pulse profiles give the largest range for dMRI measurements, and in particular, what combinations of pulse profiles allows us to encode the most possible information about the microstruture into the dMRI signals \[1\]. 

### Inverting the numerical LBM model

While the numerical LBM model is slow, it is still the most accurate model available. Because of this, it is a useful test canadite to show that it is possible to recover the microstruutral information about the muscle from the dMRI signal. Once this is establish we can work on improving the efficeny of the model. However, even though the LBM model is slow, we can take advantage of the parallelization of the LBM method by using GPU-acceleration. Additionally, by developing fitting methods that allow for parallel model evaluations we can use multiple GPUs to reduce the time it takes to fit the LBM model to the dMRI signal. 

### Machine Learning Models

Does the problem even exist if you don't use machine learning to try and solve it? Machine learning techniques have shown great promise in being able to solve inverse problems, and this inverse problem is no exception. By generating large training datasets using the numerical model, it is possible to train models to predict the microstruture from the dMRI signal \[4\]. The disadvantage of these models is they are often not based on the underlying physcis of the problem so the can not give insight into what is going on. Because of this, it is important to first understand the relatinoship between microstruture and dMRI. By first understanding this relationhsip, we can know the limits and caveats of the predictions of the machine learning models. 

Solving the inverse problem and being able to predict the microstruture of skeletal muscle from dMRI signal will likely require a combination of different models, each with its own strengths and weakness. By combining these models we will be able to take a dMRI measurement and estimate what the underlying tissue microstruture is. These microstrutural estiamtes will then be used in micro-mechancial models of muscle to solve the [mechanical problem](/pages/mechanical-problem/) of understanding how microstrutural variations affect the effective mechacnial properties of msucle, and by extension, the ability of the muscle to transmit force and function. 

### References

\[1\] Naughton NM and Georgiadis JG. Connecting Diffusion MRI to Skeletal Muscle Microstructure: Leveraging Meta-Models and GPU-acceleration. PEARC 2019 (July 2019), Chicago, Illinois (platform presentation)

\[2\] Naughton NM, Gallo NR, Anderson AT, and Georgiadis JG. Comparison of dMRI Models for Skeletal Muscle Microstructure Estimations with Numerical Simulations and Myocardial Porcine Phantom. ISMRM Annual Meeting (May 2019), Montreal, Canada (poster)

\[3\] Naughton NM, Jain A, and Georgiadis JG. Polynomial Meta-Model of Bloch-Torrey Equation for Track-based Regularization of Microstructural Inversion. ISMRM Annual Meeting (May 2019), Montreal, Canada (poster)

\[4\] Naughton NM, Gallo NR, Anderson AT, and Georgiadis JG. Microstructural Parameter Estimation of Skeletal Muscle using Random Forest Model of dMRI. ISMRM Annual Meeting (May 2019), Montreal, Canada (poster)

\[5\] Naughton NM, Gallo NR, Vaicik M, Anderson AT, Sutton BP, and Georgiadis JG. “Estimation of Extracellular Matrix Diffusion Properties in Decellularized Porcine Myocardium from DTI” ISMRM Annual Meeting (June 2018), Paris, France (poster)
