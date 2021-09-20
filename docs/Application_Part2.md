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

## Countries by Population Density

The most densely populated countries are small "City-States" like Monaco (19,000 ppl km<sup>-2</sup>) and Singapore (8,000 ppl km<sup>-2</sup>), they have relatively large populations (38,000 ppl) and (5,757,000 ppl) but very small areas (2 km<sup>2</sup>) and (716 km<sup>2</sup>).

Mongolia is one of the least densely populated countries (2 ppl km<sup>-2</sup>) because it has a small population (3,170,000 ppl) but a very large area (1,564,000 km<sup>2</sup>).


<img src="content/images/countries_by_population_density.png" width="800">

[data source](https://en.wikipedia.org/wiki/List_of_countries_and_dependencies_by_population_density)