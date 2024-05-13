#  Danish National Forest Inventory

Quantification of forest biomass stocks and their dynamics is important for implementing effective climate change mitigation measures by aiding local forest management, studying processes driving af-, re-, and deforestation, and improving the accuracy of carbon accounting.
Remote sensing using airborne LiDAR can be used to perform  measurements of vegetation structure at large scale.
The state-of-the-art for predicting forest biomass from LiDAR point clouds is to voxelize the 3D data and compute summarizing statistics of the point distribution along the vertical axis, such as mean heights, relative height quantiles, or metrics of heterogeneity.
These simple statistical features, potentially combined with other features, then serve as inputs to prediction models.

The Danish National Forest Inventory (NFI) gathers information about Danish forests and 
computes statistics  for the formation and assessment of  national or regional forest programs, sustainability assessments, investment calculations for forest industry, strategic-level planning in general, and reporting to international conventions.
The Danish NFI is based on a grid  covering the entire land surface of the country (Nord-Larsen and Kvist, 2016).
The measurements are done at the level of subplots, where 
each subplots has a radius of 15m. 

We linked the data from the Danish NFI with LiDAR data similar to Oehmcke et al. (2024), who propose a deep learning approach directly operating on the 3D point clouds.
The main task is to predict aboveground tree biomass within a subplot from statistics of the 3D LiDAR data of the subplot. 
The data in this folder were taken from 2013 to 2017 and were heavily preprocessed and cleaned for this assignment.
First, features were derived from the point clouds of the single plots. Second, only plots with non-zero biomass and
trees that are  either all broadleaf trees or all conifer trees were selected. Finally, outliers were removed.


## Example of a classification and a regression task based on the data 
	regression_target = "BMag_ha"
	classification_target = "C_frac"
	features = ['h_mean_1_', 'h_mean_2_', 'h_std_1_', 'h_std_2_', 'h_coov_1_', 'h_coov_2_', 'h_skew_1_', 'h_skew_2_', 'IR_', 'h_q5_1_', 'h_q10_1_', 'h_q25_1_', 'h_q50_1_', 'h_q75_1_', 'h_q90_1_', 'h_q95_1_', 'h_q99_1_', 'h_q5_2_', 'h_q10_2_', 'h_q25_2_', 'h_q50_2_', 'h_q75_2_', 'h_q90_2_', 'h_q95_2_', 'h_q99_2_', 'red_q75', 'red_q50', 'red_q25', 'blue_q75', 'blue_q50','blue_q25', 'green_q75', 'green_q50', 'green_q25']



## References
Thomas Nord-Larsen and Vivian Kvist Johannsen. Danish national forest inven-
tory: Design and calculations. IGN Report, Department of Geosciences and
Natural Resource Management, University of Copenhagen, 2016.

Stefan Oehmcke, Lei Li, Jaime Revenga, Thomas Nord-Larsen, Katerina Trepekli,
Fabian Gieseke, and Christian Igel. 
[Deep point cloud regression for above-ground forest biomass estimation from airborne LiDAR](https://doi.org/10.1016/j.rse.2023.113968). *Remote Sensing of Environment* 302:113968, 2024

