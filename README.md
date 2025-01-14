# Data Science Assessment
This repository contains all materials for the Data Science and Machine Learning assessment.


The code is presented as an annotated .ipynb notebook.

This a script written to explore a bulk RNA-seq dataset. For the script to work as expected, please make sure that the dataset matches the following expected format:
geneID | ensembleID | biotype | base condition | condition1timepoint | condition2timepoint | condition3timepoint etc. 


To run: 

The script requires the following libraries:

•	pandas

•	matplotlib.pyplot

•	numpy

•	re

•	seaborn

•	StandardScaler from sklearn.preprocessing

•	PCA from sklearn.decomposition



1)	The csv file is uploaded into GitHub and the data is read from the URL. If there is an issue, please download the csv data file and alter the initial read-in instructions.
2)	Please run the first cell, importing all necessary libraries
3)	If using the script to explore a different dataset, ensure that the functions to extract time points and conditions from the column titles are updated to reflect the time points and conditions of the new dataset
   
    a.	You will also need to create your own lists of genes of interest if you wish to extract and plot them
  	 
    b.	Please also note that the script removes all zero-read data as part of its data cleaning.
  	
      •	If you would rather include this, please remove the cell that removes zero read data from the variable
  	    filtered_data, and change the formula of the for loop that applies the log2 function to “log2_data[col] =
  	    np.log2(filtered_data[col]) +” a small positive value

The script outputs a PCA plot helping to identify clusters of similar samples, a line plot for each of the selected genes of interest under each of the experimental conditions, and a heatmap for the genes of interest. 


### Introduction to the specific analysis  
Early human development and cell plasticity is still a relative black box in biological science. 

The script was specifically made to explore a bulk RNA-seq data set produced by Guo et al which established that alternative cell culture conditions allow human naive epiblast cells to differentiate into trophectoderm. This transition does not occur in mouse models; instead, cells from the zygote divide and later differentiate into either trophectoderm or inner cell mass cells. These inner cell mass cells then have a second lineage bifurcation, becoming either epiblast or hypoblast. 

This study shows that human epiblast cells do not obey the sequential lineage bifurcation developmental pathway seen in mouse, but instead the epiblast cell fate remains plastic for far longer. This suggests a degree of cell fate flexibility which may aid our understanding of early human development. 
