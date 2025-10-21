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

<a href="https://www.usgs.gov/centers/pcmsc/science/coastal-storm-modeling-system-cosmos"> CoSMoS </a> is a modelling tool to predict future coastal hazards over large geographical scales.  The idea is to provide emergency responders and coastal planners with increasingly critical storm-hazards information that can be used to increase public safety, mitigate physical damages, and more effectively manage and allocate resources within complex coastal setting. 

How this is done varies a bit geographically, but in general involves a dynamic downscaling approach in which global data are scaled down to local flood projections for use in community-level coastal planning and decision-making. 

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
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj1_Cosmos/RegionalModel.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj1_Cosmos/RegionalModel_Wave.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   Left, Regional Water level model (Delft3d-FM). Right, Regional Wave model (SWAN lookup-table with linear Swell propogation).
</div>

These models provide data to local scale flooding models that provide data at high resolution for extreme events. As an example of outputs for Cosmos as implemented in the South East Atlantic.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/SE_MultiHazards.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example Multi-Hazard outputs from a CoSMoS implementation on the SouthEast Atlantic coast
</div>

I work on a whole bunch of Cosmos related work, but lead (along with <a href="https://www.linkedin.com/in/kees-nederhoff/"> Kees Nederhoff</a>) the Cosmos implementation in the Pacific Northwest. There we have made some really cool changes to workflow, like full dynamic modelling of streamflow across the Salish Sea basin to better resolve compound flooding. We've also moved to a "response based" coastal hazard approach where we are modelling 100's of years of coastal flooding and then letting events naturally emerge from the system resonse (rather than event based approach where extreme events are pre-selected). This allows the specific event which causes a 100-year return interval event to vary spatially. This makes sense physically as the 100-year event in a coastal region will be driven by oceanographic forcing while the 100-year event up a stream will be fluvial driven (and likely not the same event).




As part of the Pacific Northwest implementation of Cosmos, I do everything in the project worflow from talking to stakeholders and project managment to building and running models on our High Performance Computing cluster. 

