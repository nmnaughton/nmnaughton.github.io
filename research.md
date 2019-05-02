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

<figure style="float: right; padding-right:50px;">
<img src="/assets/img/final_frame_hist.png"  width="400">     
<figcaption>dMRI signal in skeletal muscle</figcaption>
</figure>

# Forward Problem

How do changes in skeletal muscle microstructure affect the dMRI signal? In order to predict microstructure from dMRI, we first need to answer this question. To answer this we perform numerical simulations of dMRI in skeletal muscle using both realistic and simplified geometric models. These simulations allow us to understand how the dMRI signal will change when there is a change in the underlying microstrucutre. We call this the forward problem becasue it involves solving a problem that mimics what actually happens in a dMRI experiment where the underlying structure effects the measured signal. [learn more](/pages/forward-problem/)

# Inverse Problem

How do we go from the dMRI signal to the underlying structure? This includes various modeling attempts such as response surfaces and machine learning. 
Image ideas: Difficult to create a graphical representation since this is mostly about predicting a single value, however, the idea of sensitivity to the signal might yield good visualization. 

[learn more](/pages/inverse-problem/)

# Mechanical Problem

If we can predict microstructural information, then how does this help us understand the mechanics of muscle? We use a simple mechancial model to see which parameters most effect muscle properties. We also need to measure properties of the muscle. 

[learn more](/pages/mechanical-problem/)


