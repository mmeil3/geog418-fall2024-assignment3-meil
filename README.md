# Geog 418 Fall 2024 - Spatial Autocorrelation Tutorial


Introduction

Concepts such as point pattern analysis that are achieved through nearest neighbour analysis, k-function, and quadrat analysis are useful for quantifying and visualising patterns.  Such as, if they are clustered, dispersed, or random. However, it is also valuable to determine if attributes of these locations are random or not. This is called spatial autocorrelation, a spatial analysis tool that measures the correlation of a variable with itself across space.

Spatial pattern attributes arethe basis of spatial analysis, and are examined by determining if locations that are closer together have similar attributes. It has been argued that the integration of analytical and visual methods can improve the effectiveness of spatial analysis as a decision support tool for policy and management (Guo, 2007). These concepts build off of Tobler’s Law, determining that everything is related to everything else, but closer things are more similar than things further away  (Tobler, 1970, p. 236.)  When Tobler’s law is true, we see spatial patterns where closer things are more similar, created a positive spatial autocorrelation, or clustered pattern. When Tobler’s Law is false, it is referred to as negative spatial autocorrelated, or a dispoersed pattern. 

Spatial autocorrelation measures based on the Moran’s I (Getis 2008) are commonly used to test clustering tendency of medical data, including analysis in multivariate specifications (Lin and Zhang 2007). A significant and effective application of spatial autocorrelation is examining census. The census is an important dataset that provides a plethora of knowledge to inform policy decision, research, healthcare, and many more essential services. In Canada, the census is collected every five years, where it was last collected in 2021 (Statistics Canada, 2021).

We can use spatial autocorrelation to determine if a variable is more positively,  or negatively spatially autocorrelated. This is done through Moran’s I statistic, which determines whether you want to see how similar or different you are from your neighbours. To do this, you must also define your neighbourhoods, which can be done using several standards (k-Nearest, Inverse Distance). In this exercise, we use Rook Weights (Neighbours in 4 adjacent locations) and Queen Weights (Neighbours are surrounding point).

While we employ a number of statistical tests to perform our spatial autcorrelation analysis, we use the variables of median total income and french knowledge to determine whether degree these objects or activities at some place on the earth's surface are similar to other objects or activities located nearby.  We extract data from Saskatoon, Saskatchewan to perform this analysis. 

In order to map census Data in R, we need to understand how to open, format, and map census data. As mentioned above, we are going to me using median total income and french knowledge variables from the census to visualize are data. 

First, we need to install and load required libraries. Installing libraries only needs to be done once, while you need to ensure you load your libraries at the beginning of each session. Libraries in R help us with data processing and visualisation, such as map making or plotting. Each library has a set of functions and you must install and load them to use them. 

# Install packages if not already installed:

install.packages("knitr")
install.packages("rgdal")
install.packages("tmap")
install.packages("spdep")
install.packages("raster")
install.packages("e1071")
install.packages("moments")

# Load in libraries:

library("sp")
library("raster")
library("tmap")
library("knitr")
library("sf")
library("ggplot2")
library("plyr")
library("dplyr")
library("st")
library("spatstat")
library("e1071")
library("moments")

To start, you will want to read the shapefile for the census boundaries into ‘R’ as a st dataframe and the census data into a dataframe. 
After we load and install our libraries, we can open and format our census data to the correct data type and projections. We will have to set a working directory, which tells R where to look for, and save files. This helps prevent errors with file paths and makes it easier to view outputs.


Spatial Autocorrelation?
Working Library?
Working Directory?
