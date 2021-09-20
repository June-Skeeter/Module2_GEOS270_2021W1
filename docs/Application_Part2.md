---
layout: default
title: Implications of CRS
parent: Application
has_children: true
nav_order: 2
---

# Implications of CRS on Population Density

Your choice of map projection can have drastic impacts on the accuracy of your analysis.  We're going to look at a simple example to highlight just how drastic the impact can make on the results you obtain!  For example, lets look at population density (D):

<img src="https://latex.codecogs.com/svg.image?D&space;=&space;\frac{P}{A}" title="D = \frac{P}{A}" />

P is the population, which we can get that from census data.  A is the area, we have to calculate that from our data layer.  Our calculation of area will be dependent upon the map projection we choose.  Generally, the map unit is meters, so our resulting population density will be "people per square meeter".  This isn't too meaningful as you can't fit very many humans in one square meter.  Generally, we want to convert to squaree kilometers, which can be done by multiplying by 1,000,000 (one million square meters in a square kilometer).