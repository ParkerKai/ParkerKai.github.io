---
layout: page
title: Emulation   
description: Hybrid modelling using machine learning to speed up dynamic models
img: assets/img/Proj4_Emulation/GPR.png
importance: 4
category: work
---

Website in progress

The idea behind an emulator is that often we have a process that takes too long to calculate. In my world, this is often a model that takes too long to run, but it could be any other situation where you need a computation faster than you can compute. The idea is actually fairly similar to how our brains solve for something like catching a baseball. We "could" theoretically try to solve for the motion of a baseball in order to catch it, but it's actually a pretty spicy set of differential equations. 


Instead, our brain solves this a different way.  We play catch and build up a database of where a baseball ends up from a set of initial conditions.  Your brain then guestimates based on this database. We can do something similar with computationally expensive model runs by building up a database of how the computationally expensive process behaves based on the inputs, and then use machine learning to guestimate what it would say from any set of initial conditions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj4_Emulation/EmulatorOrSimulator.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Emulator or simulator
</div>

The "Emulator" then can serve as a much faster replacement for you expensive computational process. This allows all kinds of exciting things that would normally be computationally prohibitice (like probabalistic modelling). An example emulator build to replace a computationally expensive coupled ADCIRC/SWAN (hydrodynamic + wave) model in order to allow probabalistic hazard analysis looks like this:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj4_Emulation/EmulatorBuild_Adcirc.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Emulator or simulator
</div>


This allows thousands of years of simulation to determine things like robust 100-year RI water levels or probabalistic wave hindcasts.  


This allows us to do cool things:

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj4_Emulation//SWAN_Emulator_Uncertinaty.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj4_Emulation//SWAN_Emulator_Uncertinaty.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left, probabalistic 100-year return level water levels for Gray's Harbor Washington. Right: Probabalistic wave hindcast for Pichilemu, Chile.  
</div>

