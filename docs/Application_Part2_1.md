---
layout: default
title: Calculating Population Density
parent: Implications of CRS
grand_parent: Application
has_children: true
nav_order: 1
---

1. TOC
{:toc}

# Setting Up a Project

Create a new project called "Pop Density", following the same steps as in [Module 1].  *Note*(If you are working on a Geography lab computer, remember to **work in C:/Temp** but save to your **H:/** drive.  If you are unsure what that means, ask your TA for assistance.

## Working with Geodatabases

We introduced the concept of geodatabases last week.  To review, a geodatabase (.gdb) is a file management structure that is designed specifically for ESRI products.  You don't have to store your data in a .gdb, Arc Pro can work with data stored in standard formats as well.  **But** .gdb have some enhanced functionality that can be useful, so a .gdb is created by default with every new project.  If you expand the 


<img src="content/images/catalog.png" height="1000">

### Importing a Feature Class

Right click on Pop_Density.gdb and select >> Import >> Feature Class.  The Feature Class to Feature Class tool will open.  Specify CAN_WGS1984.shp as the Input Feature.  This file came with the mapProjectons tutorial, and can be found in gisData/shapefiles/.  You can name the output CAN_WGS1984.  Click Run.
* The layer will now be in your .gdb and it will be added to your map.  Notice how the shape of the display changed when the layer was added to the Map.  This is a feature of the *Project on the Fly* function may introduced.

<img src="content/images/import.png" height="800">

## Feature Datasets

We briefly covered Feature Dataset in Module 1.  To review, a Feature Dataset: a collection of feature classes within a geodatabase that have common properties (eg. projections).  When we create a feature dataset, we can specify a projection.  Then any layer we add to the feature dataset, will be re-projected to match.

**1**{: .label } Right click on Pop_Density.gdb and select New>>Feature Dataset

<img src="content/images/feature_dataset.png" height="800">

**2**{: .label } Name the Feature Dataset WebMercator 

**3**{: .label } Set the coordinate system to *WGS 1984 Web Mercator Auxiliary Sphere* as shown in the screenshot below.
* This is the projection used by ArcPro's basemap.  Its also the projection used by google maps, and most other web based mapping services (as explained in the Vox video).

<img src="content/images/web_mercator.png" height="800">

**4**{: .label } Create another new Feature Dataset, name this one AlbersEqualArea.  Set the coordinate system to *Canada Albers Equal Area Conic* as shown in the screenshot below then click Run.

<img src="content/images/albers.png" height="800">

### Importing a Feature Class

**1**{: .label } Right click on the WebMercator Feature Dataset.  Select Import >> Feature Class.  Name the Output_Feature_Class CAN_Web_Mercator as shown in the screenshot below.  Click Run.

<img src="content/images/feature_class_import.png" height="800">

**2**{: .label } Repeat this for the AlbersEqualArea Feature Dataset.  Select Import >> Feature Class.  Name the Output_Feature_Class CAN_Albers_EA.  Click Run.


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

Look at the province/territory you identify above.  Did the area change?  If so, by how much?

# Save your project.

Click Save in the top left of the Arc Pro window.
