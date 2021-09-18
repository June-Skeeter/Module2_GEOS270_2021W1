---
layout: default
title: Visualizing the Difference
parent: Implications of CRS
grand_parent: Application
has_children: true
nav_order: 2
---

1. TOC
{:toc}

# Create Geodatabase

Create new .gdb

## Import Data

Find the Canada WGS 1984 shapefile.  Import once to base .gdb
* Add field:
    * Population, Integer
* Edit field, (xxxxx) current pop estimate

**Definition** Integer, whole round number.

## Feature Classes

Create 2 feature classes.
Specify the CRS: Web Mercator WGS 1984, Albers Equal Area WGS 1984
* Feature classes will require all .shp contained to take that projection
* Importing a shapefile will automatically reproject it.

Add the Canada_WGS_1984 to both feature classes.

# Calculate Population Density

Look at the area value for WGS 1984 - Does this value make any sense??  No!  Area in degrees isn't helpful

* Add field:
    * Population Density, Float

**Definition** Float, floating point number (allows decimals).

### **QC**

What projection is the layer currently in?

# Calculate Population Density

### **QC**

Which province/territory has the greatest area?

# Change the projection to Lambert Conformal Conic

### **QC**

Look at the province/territory you identified above.  Did the area change?  If so, by how much?

# Change the projection again

This time choose xxx Equal Area.

### **QC**

Look at the province/territory you identify above.  Did the area change?  If so, by how much?

# Save your project.

Click Save in the top left of the Arc Pro window.
