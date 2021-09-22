---
layout: default
title: Steps of Abstraction
parent: Coordinate Reference Systems
# has_children: true
grand_parent: Content
nav_order: 1
---
<!-- 
# Steps of Abstraction
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

--- -->

# Flattening the Blue Marble

This is what earth looks like when you take a picture of it from 29,000 kilometers away.  This is the original [Blue Marble](https://en.wikipedia.org/wiki/The_Blue_Marble) photo, taken from Apollo 17.

<img src="content/images/blue_marble_og.jpg" width="400">

# Steps of Abstraction

The Earth is a lumpy ball of rock in space.  It is far too complicated to represent fully.  We need to create abstractions to simplify the shape of the earth so we can map it in 2D.  


<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/Abstraction.html" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/Abstraction.html" target="_blank">View slides in new tab</a>

<!-- 

## Approximating the Geoid

Approximating the **Geoid** is the first step in the abstraction process.  A
- Smoothed topography, less lumpy ball of rock

### 3)**Datum**:
- Completely smoothed oblate spheroid

### 4)**Geographic Coordinate System (GCS)**:
- Spherical coordinate system corresponding to points on the datum

### 5)**Projected Coordinate System (PCS)**:
- Projection of a 3D GCS onto a 2D plane (computer screen, paper map, etc.) -->

---

# Assessment Questions

### QC3

The first step in creating an abstraction of the earth is to simplify it to a geoid.  The is an abstract representation of the earth that smooths out ______ but preserves ______ differences due to ______ differentials.


### QC4

If you are mapping a city like Vancouver, ______ a datum is best.  When mapping the whole world, you'll want to use a ______ datum.  WGS 1984 is an example of a ______ datum, NAD 1983 is an example of a ______ datum.


### QC5

[Latitude/Longitude] is a measure of angular distance North/South of the equator and [Latitude/Longitude] is a measure of angular distance from the prime meridian.  


### QC6

 Together they form a ______, describing locations on the surface of a simplified model of the earth known as a ______ which represents the earth as an oblate spheroid.