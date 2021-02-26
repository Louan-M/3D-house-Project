# 3D-house-Project


- Developer: `Louan Mastrogiovanni`
- Type of Challenge: `Learning & Consolidation`
- Duration: `2 weeks`
- Deadline: `25/02/21 5:00 PM`
- Deployment strategy :
	 Github page
	| Powerpoint
	| Jupyter Notebook
	| Webpage
	| App
- Team challenge : `solo`

## Mission Objectives

Consolidate the knowledge in Python, specifically in :

- NumPy
- Pandas
- Matplotlib


## Learning Objectives


* to be able to search and implement new librairies
* to be able to read and use shapefiles
* to be able to read and use geoTIFFs
* to be able to render a 3D plot
* to be able to present a final product

&nbsp;

## About the Repository

This project consists of building a 3D model of a house based on an address located in the Flemish region of Belgium. The data used is Lidar data. The Flemish Region has been divided into 43 parts, each encoded into a raster geotiff file (.tif), in two types: DSM and DTM.

### Canopy Height Model

The DSM and the DTM are combined together to create a Canopy Height Model (CHM) which is required for the 3D model.

		CHM = DSM - DTM

The files are available online on the *Geopunt.be* website via those links:


[DTM](http://www.geopunt.be/download?container=dhm-vlaanderen-ii-dtm-raster-1m&title=Digitaal%20Hoogtemodel%20Vlaanderen%20II,%20DTM,%20raster,%201m)
[DSM](http://www.geopunt.be/download?container=dhm-vlaanderen-ii-dsm-raster-1m&title=Digitaal%20Hoogtemodel%20Vlaanderen%20II,%20DSM,%20raster,%201m)

&nbsp;

### Repository

The main file is "**3D-project.ipynb**" (Jupyter notebook). 

The *Utils/* folder contains the csv file (coordinates dataset) used by the program to find the raster.

<img src="https://github.com/Louan-M/3D-house-Project/blob/main/Images/dataset.png" width="750">

&nbsp;

## Process

1. Postal address converted to geospatial coordinates (Lambert projection (CRS= 31370)) 
2. From the coordinates, a look into the coordinates dataset (csv file) is done to select the correct raster
3. Creation of the polygon from the coordinates
4. Mask (Crop) of the DSM and DTM rasters based on the polygon geometry
6. Creation of the Canopy Height Model from the masked DSM and DTM
7. 3D Plot

&nbsp;

### Example of output

<img src="https://github.com/Louan-M/3D-house-Project/blob/main/3D-Plot-images/Maaltekouter-1-9000-Gent.png" width="700">

<img src="https://github.com/Louan-M/3D-house-Project/blob/main/3D-Plot-images/Maaltekouter%201%209000%20Gent%20Google%20map%20view.png" width="600">

&nbsp;

## Challenges

Find the easiest way to get the coordinates from a given address.

Several issues with environnements (conda) and Linux packages compatibility

Issues with RAM overlad

Rendering problems with Plotly (Firefox)

...
&nbsp;


## Further Improvements

Merge to a web application

Add an interactive input box

Access the rasters directly without downloading them
