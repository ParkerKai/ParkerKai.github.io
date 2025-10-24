---
layout: page
title: Emulation   
description: Hybrid modelling using machine learning to speed up dynamic models
img: assets/img/Proj4_Emulation/GPR.png
importance: 4
category: work
---

The idea behind an emulator is that often we have a process that takes too long to calculate. In my world, this is often a model that takes too long to run, but it could be any other situation where you need a solution faster than you can compute. The idea behind an emulator is actually fairly similar to how our brains solve for something like catching a baseball. Our brain "could" theoretically try to solve for the motion of a baseball in order to catch it, but it's actually a pretty spicy set of differential equations. 


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj4_Emulation/Catch.png" title="Jetski" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj4_Emulation/EquationsMotion.png" title="Topo Lowers" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj4_Emulation/Brain.png" title="Survey Ski in the Surfzone" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    To catch a ball (left), would you prefer to solve the system of PDE's (middle), or solve it like our brain does?  
</div>

Instead, our brain solves this a different way.  We play catch and build up a database of where a baseball ends up from a set of initial conditions.  Your brain then does a fancy guestimates based on this database and our observation of the ball. We can do something similar with computationally expensive model runs by building up a database of how the computationally expensive process behaves based on the inputs, and then use machine learning to predict what the model would say from any set of initial conditions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj4_Emulation/EmulatorOrSimulator.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    From a set of inputs, we build an Emulator to rapidly predict what our simulator (or model) was solve.
</div>

The "Emulator" then can serve as a much faster replacement for you expensive computational process. This allows all kinds of exciting things that would normally be computationally prohibitive. An example emulator build to replace a computationally expensive coupled ADCIRC/SWAN (hydrodynamic + wave) model in order to allow probabalistic hazard analysis looks like this:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj4_Emulation/EmulatorBuild_Adcirc.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Emulator or simulator
</div>

For the experiment design, you run the expensive simulator at a set of design points (ideally chosen in a smart way to best sample variability across the input space). This produces a training dataset that you then use for building a machine learning model. For my work, I've used Gaussian Progress Regression, but you can insert you favorite machine learning algorithm here.  Overall I've shown that, with a proper build, the emulation step introduces only a small amount of error (in general the physical model you are using has an order of magnitude larger error).  

This workflow has a whole range of applications (I think most of us have come up against computational limits as a barrier to a science question). For me I've used this technique to model thousands of years of simulation to determine things like statistically robust 100-year RI water levels or probabalistic wave hindcasts under high input uncertainty.


<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj4_Emulation/Greys_100yrRI.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj4_Emulation/SWAN_Emulator_Uncertinaty.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left, probabalistic 100-year return level water levels for Gray's Harbor Washington. Right: Probabalistic wave hindcast for Pichilemu, Chile.  
</div>

