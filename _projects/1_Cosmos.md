---
layout: page
title: Coastal Storm Modelling System (Cosmos) 
description: CoSMoS makes detailed predictions of storm-induced coastal flooding, erosion, and cliff failures over large geographic scales.
img: assets/img/Proj1_Cosmos/USGSCoSMoS.jpg
importance: 1
category: work
related_publications: true
---

Website in Progress


Flooding is increasingly becoming a reality for communities along the coastline. This is only going to continue to get worst as climate change and SLR change how the coastline, the ecosystem, and people/infastructure interact.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/Flooding1.png" title="Jetski" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/Flooding2.png" title="Topo Lowers" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/Flooding3.png" title="Survey Ski in the Surfzone" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Flooding in the Puget Sound
</div>

CoSMoS is a modelling tool to predict future coastal hazards over large geographical scales.  The idea is to provide emergency responders and coastal planners with increasingly critical storm-hazards information that can be used to increase public safety, mitigate physical damages, and more effectively manage and allocate resources within complex coastal setting. 

This is done using a dynamic downscaling approach in which global data are scaled down to local flood projections for use in community-level coastal planning and decision-making. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/Tiered_Downscaling.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The idea behind CoSMoS is to dynamically downscale from climate all the way to the local scale.
</div>

Global data (from global reanalysis and climate model simultaions) provide data to regional models. For the Puget Sound, the regional models are a Salish Sea implementation of a hydrodynamic and wave model.  

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj1_Cosmos/RegionalModel.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj1_Cosmos/RegionalModel_Wave.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   Left, Regional Water level model (Delft3d-FM). Right, Regional Wave model (SWAN lookup-table with linear Swell propogation).
</div>

These models provide data to local scale flooding models that provide data at high resolution for extreme events. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/SE_MultiHazards.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example Multi-Hazard outputs from a CoSMoS implementation on the SouthEast Atlantic coast
</div>

Website in progress
