---
layout: default
title: Spatial Analysis
parent: Application
grand_parent: Module 1
nav_order: 4
---

# Spatial Analysis

We already know the Broad St. pump was the source of the outbreak, but lets explore a couple analysis techniques we could use to identify the source of the outbreak.

## Measures of Central Tendency

There are numerous ways to analyze the spatial distribution of a dataset.  The [Mean Center](https://pro.arcgis.com/en/pro-app/latest/tool-reference/spatial-statistics/mean-center.htm) and [Directional Distribution](https://pro.arcgis.com/en/pro-app/latest/tool-reference/spatial-statistics/directional-distribution.htm) are two of the simplest measures.  Mean center gives you a single point around which the directional distribution creates an ellipse to show directional trends in the data.  You don't have to calculate these statistics, but skim the linked pages and look at the example below to understand what these methods do.
* They can be weighted (eg. by the number of deaths per address).
* These measures roughly identify the Broad St. Pump as the source of the outbreak, as shown in the figure below.
  * However, they are rudimentary metrics at best.  They could be used to identify multiple point sources for example.

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/images/Distribution.png" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/images/Distribution.png" target="_blank">View Image in New Tab</a>


### [**Written Answer 2**](/Assessment.md#written-answer-2)

What do the mean center and directional distribution tell us about a set of points?

## Point Density

A more advanced method is [Kernel Density](https://pro.arcgis.com/en/pro-app/latest/tool-reference/spatial-analyst/kernel-density.htm), which gives you a magnitude (eg. number of deaths) per unit area (eg. hectare).  Follow the steps as outlined and refer to the video below to calculate the Kernel Density of cholera deaths in Soho.

**1)** Click the Analysis tab and select Tools.  In the Geoprocessing pane, search for and open the Kernel Density tool.
* The Geoprocessing pane is where you can find all the different spatial analysis tools in ArcGIS Pro.

**2)** Set Deaths as the input and COUNT as the Population Field.
* The population field weights the calculations by the number of deaths at each address.

**3)** Rerun the analysis multiple times, playing around with different Output cell sizes and Area units.  When you are done exploring the effects of cell size and units, calculate the Kernel Density with a cell size of 5 and unit of Hectares.
* A Hectare is 10,000 m<sup>2</sup>, or about the area a small city block.

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/videos/KD.mp4" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/videos/KD.mp4" target="_blank">View Image in New Tab</a>

### [**Written Answer 3**](/Assessment.md#written-answer-3)

Why might Kernel Density might be more useful for identifying the source of a source(s) of a cholera outbreak outbreak than the mean center and directional distribution?

### [**Written Answer 4**](/Assessment.md#written-answer-4)
What are the effects of changing the "Output cell size" and "Area unit"?

## Save your project.

Click Save in the top left of the Arc Pro window.
