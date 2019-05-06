---
layout: page

# The title of the page.
title: My Research

# Write a short (~150 characters) description of each blog post.
# This description is used to preview the page on search engines, social media, etc.
description: >
  Overview of My Research

# You can show the description on the page by deleting this line:
hide_description: true

---

<figure style="float: right; padding-top:20px;">
<img src="/assets/img/microstructure_white.PNG"  width="400">     
<figcaption>skeletal muscle microstructure</figcaption>
</figure>

My current research focus is on non-invasively measuring the microstructure (or cellular organization) of skeletal muscle. Muscle microstructure consists of long fibers that are tightly packed together and surrounded by an extracellular collagen matrix. Changes in this microstructure are related to changes in muscle health, so non-invasive measurement of this microstructure should provide new diagnostic tools for assessing muscle health. 

I work on measuring this microstructure using diffusion-weighted magnetic resonance imaging (dMRI) and connecting this microstrucutre to effective meachancial properties of muscle. This work can be broadly organized as three separate but interrelated problems:  

<figure style="float: left; padding-right:20px; padding-top:10px;">
<img src="/assets/img/dMRI.png"  width="250">
<figcaption>dMRI of human thigh</figcaption>
</figure>

[The Forward Problem](#forward-problem): Understanding how changes in skeletal muscle microstructure affect the dMRI signal.

[The Inverse Problem](#inverse-problem): Estimating the microstructure of skeletal muscle from dMRI measurements.

[The Mechanical Problem](#mechanical-problem): Using microstructural information to understand mechanical properties of muscle. 

<br/> <br/>
By solving these three problems, I am working to create an imaging pipeline that can image a skeletal muscle, estimate its microstructure, and use this microstructural information to estimate mechancial properties of the muscle. This pipeline will better inform our understanding of muscle's functional ability. Much of this work is based on measuring the muscle's microstructure using dMRI. dMRI measures the movement of water molecules. By measuring how microstructural restrictions affect the movement of these water molecules, we can measure the cumulative effect of the microstructure on the dMRI signal. For a brief introduction into how we can measure muscle microstructure using dMRI, check out the video below. 

&nbsp;

<figure>
<iframe width="560" height="315" src="https://www.youtube.com/embed/Kj3s-ayh6VE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<figcaption>video I submitted to ISMRM 2019 Magnetic Moments competition explaining dMRI to the public</figcaption>
</figure>

&nbsp;


<figure style="float: right; padding-top:150px;  padding-left:20px; padding-bottom:50px;">
<img src="/assets/img/final_frame_hist.png"  width="400">     
<figcaption>dMRI signal in skeletal muscle microstructure</figcaption>
</figure>

# Forward Problem

How do changes in skeletal muscle microstructure affect the dMRI signal? In order to predict microstructure with dMRI, we first need to answer this question. To answer it, we perform numerical simulations of dMRI in skeletal muscle using both realistic and simplified geometric models. These simulations allow us to understand how the dMRI signal will change when there is a change in the underlying microstructure. We call this the forward problem because it involves solving a problem that mimics what actually happens in a dMRI experiment, where the underlying structure affects the measured signal.

[learn more](/pages/forward-problem/)

<figure style="float: left; padding-top:150px;  padding-right:20px; padding-bottom:70px;">
<img src="/assets/img/final_parameter_selection.PNG"  width="400">     
<figcaption>dMRI pulse optimization for microstructure encoding</figcaption>
</figure>

# Inverse Problem

The inverse problem asks "how do you take the dMRI signal and determine the microstructure of the muscle from it?" We use the insights we gain from solving the forward problem to invert the forward problem by taking the measured dMRI signal and going backwards to the original microstructure that caused the signal. These models consist of analytical compartment models, numerical inversion methods, meta-models and machine learning techniques. They allow us to determine what dMRI pulse sequences encode the most information into the signal and how to decode this information to recover the underlying microstructure.

[learn more](/pages/inverse-problem/)


<figure style="float: right; padding-top:150px;  padding-left:20px; padding-bottom:50px;">
<img src="/assets/img/muscle_schematic.png"  width="400">     
<figcaption>simplified model of muscle</figcaption>
</figure>

# Mechanical Problem

The final piece of the puzzle is using the microstructural information from the inverse problem to gain new insight into how the muscle functions. In particular, we look at how changes in muscle microstructure lead to different effective mechanical properties of the muscle. These mechanical properties are integral to force transmission through the muscle. Using micro-mechanical models of the muscle, we connect how changes in the microstructure change these properties, which will help us non-invasively measure muscle health and quality. 

[learn more](/pages/mechanical-problem/)


