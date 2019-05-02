---
layout: page

# The title of the page.
title: My Research -- under construction

# Write a short (~150 characters) description of each blog post.
# This description is used to preview the page on search engines, social media, etc.
description: >
  Overview of My Research

# You can show the description on the page by deleting this line:
hide_description: true

---

<figure style="float: right;">
<img src="/assets/img/microstructure_white.PNG"  width="400">     
<figcaption>skeletal muscle microstructure</figcaption>
</figure>

My current research focus is on non-invasively measuring the microstructure of skeletal muscle. Muscle microstructure is a description of how muscle cells are organized. Muscle consists of long fibers that are tightly packed together and surrounded by an extracellular collagen matrix. Changes in this microstructure have been related to changes in muscle health so non-invasive measurement of this microstrucutre should provide new diagnostic tools for assessing muscle health. 

I am working on measuring this microstrucutre using diffusion-weighted magnetic resonance imaging (dMRI). Then, using these estimations of microstructure from the dMRI, I am working to develop mechancial models of muscle microstructure to the muscle’s mechancial properties are affected by changes in the microstructure. 

This work can be broadly organized as three separate but interrelated problems:  
<figure style="float: left; padding-right:20px; padding-bottom:20px;">
<img src="/assets/img/project_scheme.png"  width="300" vspace>
</figure>

[The Forward Problem](#forward-problem): Understanding how changes in skeletal muscle microstructure affect the dMRI signal.

[The Inverse Problem](#inverse-problem): Estimating the microstructure of skeletal muscle from dMRI measurements.

[The Mechanical Problem](#mechanical-problem): Using microstructural information to understand mechanical properties of muscle. 

By combining solutions to these problems I hope to create an imaging pipeline that can image a skeletal muscle, estimate its microstructure, and use this microstrucutral information to better inform understanding of the mechancial function of the muscle.   

The first two problems (forward and inverse Problems) relate to the major challenge of measuring the muscle's microstructure. dMRI measures the movement of water molecules. By measuring how the presence of microstrucutral restrictions affects the movement of these water molecules, we can measure the cumulative effect of the microstructure on the dMRI signal. The following is a brief video explaining how exactly we can measure muscle microstructure using dMRI signal. 

&nbsp;

<iframe width="560" height="315" src="https://www.youtube.com/embed/KDJG7JLhH2M" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

&nbsp;

# Forward Problem

<figure style="float: right; padding-top:50px;  padding-left:20px;">
<img src="/assets/img/final_frame_hist.png"  width="400">     
<figcaption>dMRI signal in skeletal muscle</figcaption>
</figure>

How do changes in skeletal muscle microstructure affect the dMRI signal? In order to predict microstructure from dMRI, we first need to answer this question. To answer this we perform numerical simulations of dMRI in skeletal muscle using both realistic and simplified geometric models. These simulations allow us to understand how the dMRI signal will change when there is a change in the underlying microstrucutre. We call this the forward problem becasue it involves solving a problem that mimics what actually happens in a dMRI experiment where the underlying structure effects the measured signal. 

[learn more](/pages/forward-problem/)

<figure style="float: left; padding-top:150px;  padding-right:20px; padding-bottom:50px;">
<img src="/assets/img/final_parameter_selection.PNG"  width="400">     
<figcaption>dMRI pulse optimization for microstructure encoding</figcaption>
</figure>

# Inverse Problem

THe inverse problem asks how take the dMRI signal from it determine the microstrucutre of the muscle? We use the insights we gain from solving the forward problem to develop models that allow us to invert the forward problem by taking the measured dMRI signal and going backwards to the orginal microstructure that caused the signal. These models consist of analytical compartment models, numerical inversion methods, meta-models and machine learning techniques to determine what dMRI pulse sequences encode the most information into the signal and how to decode this information to recover the underlying microstructure. 

[learn more](/pages/inverse-problem/)


<figure style="float: right; padding-top:150px;  padding-left:20px; padding-bottom:50px;">
<img src="/assets/img/muscle_schematic.png"  width="400">     
<figcaption>simplified model of muscle</figcaption>
</figure>

# Mechanical Problem

The final peice of the puzzle is using the microstructure information from the inverse problem to give new insight into how the muscle is able to function. In particular we look at how changes in muscle microstruture lead to different effective emchancial properties of the muscle. These mechanical properties are integral to force transmission through the muscle. Using micro-mechanical models of the muscle, we connect how changes in the microstructure change these proeprties, which will help us non-invesivly measure muscle health and quality. 

[learn more](/pages/mechanical-problem/)


