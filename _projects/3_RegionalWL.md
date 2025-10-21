---
layout: page
title: Regional Water Level Components
description: Regional scale modelling to characterize water level components contributing to extremes
img: assets/img/Proj3_RegWL/GTSM.png
importance: 3
category: work
---

Often in my work I come across a need for large scale data related to oceanographic processes.  As a few examples, this could be because boundary conditions for a local scale study are needed or because a regionally consistent dataset is requried to compare vulnerability across large spatial extents. This was traditionally done by downscaling through multiple spatial scales, but improvements in computational power and modelling have made global scale products a potential solution. For this work, I've looked at a variety of global products and seen how they can be combined, corrected, and leveraged to answer usefull science questions.  

As an example, I've done a chunk of work looking at the Global Tide and Surge model <a href="https://www.sciencedirect.com/science/article/abs/pii/S0306261920304347](https://www.deltares.nl/en/expertise/projects/global-modelling-of-tides-and-storm-surges"> (GTSM) </a> combined with our own wave model runs <a href="https://cmgds.marine.usgs.gov/data-releases/datarelease/10.5066-P9KR0RFM/"> (WW3) </a> to look at large scale oceanographic processes controlling extremes and how they might change into the future.  

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj3_RegWL/GTSM_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj3_RegWL/WW3_Atlantic.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Global Tide and Surge Model (GTSM), a global implementation of Delft3d-FM. Right: Atlantic Grid for NOAA's MMAB global wave watch 3 model (Model used by USGS to produce consistent data to GTSM).  
</div>

Overall comparing modelled water levels (with some simple corrections) to tide gauges, the global product is able to produce fairly reasonable water levels.

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj3_RegWL/SE_GaugeError.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Proj3_RegWL/WL_Scatter.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Global Tide and Surge Model (GTSM), a global implementation of Delft3d-FM. Right: Atlantic Grid for NOAA's MMAB global wave watch 3 model.  
</div>

With some confidence in these global products, we can start to answer some interesting science questions.  For example, how do the contributors to extreme water levels vary across the United States.  

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj3_RegWL/GTSM_AllCoasts_ComponentsBars1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Regional Water level Contributions
</div>

This can help us to characterize what processes are important to capture in different regions.  For example, waves are very important on the West Coast and Non-Tidal Residual in the Gulf.  

We can also leverage these datasets to start to consider how these contributors to extremes may change into the future.  As an example for the West Coast, Total Water Level (TWL) may actually decrease into the future as a function of decreasing wave forcing during extremes.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Proj3_RegWL/AveExtremeContributions_wc.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    How water levels are expected to change into the future. 
</div>

This is one usage of these types of datasets, but they can also be leveraged to run large scale coastal hazard type analysis (E.g. Cosmos).  For example, we utilized these data as nearshore forcing for overland flow models in the South East Atlantic.  


