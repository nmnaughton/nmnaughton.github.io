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


## Mechanics of Musculo(skeletal) Structures
<figure style="float: right; padding-left:20px; padding-top:5px;">
<img src="/assets/video/Octo_dMRI.gif"  width="350">     
<figcaption>dMRI tractography of an octopus arm </figcaption>
</figure>
My current research is on using Cosserat rods, which are slender, 1-dimensional rods that can stretch, bend, twist and shear. I am working on the [CyberOctopus](https://cyberoctopus.csl.illinois.edu/){: target="_blank"} project where we are using Cosserat rods to model the musculo (but not skeletal!) biomechanics of octopus arms. I am working on the development of the numerical solver [Elastica](https://cosseratrods.org){: target="_blank"}, which is used to perform this simulations. Long term, I believe this modeling approach holds great promise to improve our ability to understand how fibrous tissues are organized and how this organization gives rise to their functional capabilities.

## Skeletal Muscle dMRI
<figure style="float: right; padding-left:20px; padding-top:5px;">
<img src="/assets/video/REV-animation.gif"  width="350">     
<figcaption>dMRI signal evolution in simplified muscle model </figcaption>
</figure>
I am also working on computational modeling of diffusion-weighted magnetic resonance imaging (dMRI) in fibrous tissue, with a particular focus on skeletal muscle. I have developed numerical models how dMRI is influenced by a tissues microstructural environment, characterized the sensitivity of this signal to microstructural changes, and developed data-driven inverse models that predict microstructural parameters from dMRI images. [Learn More](/muscle_research/).


## Bio-inspired and Neuromorphic Control of Soft Robots
<figure style="float: right; padding-left:20px; padding-top:5px;">
<img src="/assets/video/soft_arm.gif"  width="350">     
<figcaption>RL control of a soft arm in the presence of obstacles </figcaption>
</figure>
I am exploring how learning-based, bio-inspired, and neuromorphic control techniques can be combined with the compliant physics of a soft robot to improve control. A soft robot's infinite degrees of freedom often frustrate traditional control techniques. Use of learning-based techniques such as reinforcement learning allow us to avoid having to explicitly model these compliant dynamics with the RL algorithm instead implicitly learning a control policy. Bio-inspired and neuromorphic control extends this by adopting strategies evolved by biological creates to solve this challenge. 

