---
layout: page
title: Coastal Storm Modelling System (Cosmos) 
description: CoSMoS makes detailed predictions of storm-induced coastal flooding, erosion, and cliff failures over large geographic scales.
img: assets/img/Proj1_Cosmos/USGSCoSMoS.jpg
importance: 1
category: work
related_publications: false
---

Coastal hazards are increasingly becoming a common reality for communities along the coastline, a pressure that will only become more prevalent as climate change and SLR continue to change how the coastline, the ecosystem, and people/infastructure interact. Information on how the coastal environment and extreme events are expected to change is critical for charting a course into the future. 

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

<a href="https://www.usgs.gov/centers/pcmsc/science/coastal-storm-modeling-system-cosmos"> CoSMoS </a> is a modelling tool to predict future coastal hazards over large geographical scales. The idea is to provide critical storm-hazards information that can be used to increase public safety, mitigate physical damages, and more effectively manage and allocate resources within complex coastal setting. 

Cosmos is a general framework and therefore the technical specifics vary a bit geographically, but in general involves a dynamic downscaling approach in which global data are scaled down to local flood projections for use in community-level coastal planning and decision-making.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/Tiered_Downscaling.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The idea behind CoSMoS is to dynamically downscale from climate all the way to the local scale.
</div>

Global data (from global reanalysis and climate model simultaions) provide data to regional models. As an example for the Puget Sound, the regional models are a Salish Sea implementation of a hydrodynamic and wave model.  

<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj1_Cosmos/RegionalModel.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj1_Cosmos/RegionalModel_Wave.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   Left, Regional Water level model (Delft3d-FM, <a href="https://doi.org/10.3390/w15234167"> Grossman et al., 2023</a> ). Right, Regional Wave model (SWAN lookup-table with linear Swell propogation, <a href="https://doi.org/10.1016/j.ocemod.2023.102231"> Crosby et al., 2023</a>).
</div>

These models provide data to local scale flooding models (SFINCS) that provide data at high resolution for extreme events. As an example of outputs for Cosmos as implemented in the South East Atlantic.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/SE_MultiHazards.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example Multi-Hazard outputs from a CoSMoS implementation on the SouthEast Atlantic coast. The plotted scenario is coastal flooding (no storm), shallow groundwater exposure and erosion (unimpeded model case) for 1.00 m of SLR (that is, the Intermediate scenario projected for 210014), and observed VLM. Plot from <a href="https://doi.org/10.1038/s41558-024-02180-2"> Barnard et al., 2025</a>
</div>

I work on a whole bunch of Cosmos related work, but lead (along with <a href="https://www.linkedin.com/in/kees-nederhoff/"> Kees Nederhoff</a>) the Cosmos implementation in the Pacific Northwest. There we have made some really cool changes to workflow, like full dynamic modelling of streamflow across the Salish Sea basin to better resolve compound flooding. We've also moved to a "response based" coastal hazard approach where we are modelling 100's of years of coastal flooding and then letting events naturally emerge from the system resonse (rather than event based approach where extreme events are pre-selected). This allows the specific event which causes a 100-year return interval event to vary spatially. This makes sense physically as the 100-year event in a coastal region will be driven by oceanographic forcing while the 100-year event up a stream will be fluvial driven (and likely not the same event).


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj1_Cosmos/Flooding_SLR_Duwmish.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example of flooding from the 20-year event at various SLR levels (Lower Duwamish River, King County WA)
</div>

As part of the Pacific Northwest implementation of Cosmos, I do pretty much a little of everything in the project from beginning to end.  This includes talking to stakeholders, project managment across teams, building and running models on our High Performance Computing cluster, wrangling giant meteology files, producing and releasing products, and everything in between you can imagine.  

