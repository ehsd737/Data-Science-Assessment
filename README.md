# Data-Science-Assessment
This repository contains all materials for the Data Science and Machine Learning assessment.


The code is presented as an annotated .ipynb notebook.

This a script written to explore a bulk RNA-seq dataset (LINK). For the script to work as expected, please make sure that the dataset matches the following expected format:
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



1)	Please download the csv file provided
2)	Please run the first cell, importing all necessary libraries
3)	If using the script to explore a different dataset, ensure that the functions to extract time points and conditions from the column titles are updated to reflect the time points and conditions of the new dataset
   
    a.	You will also need to create your own lists of genes of interest if you wish to extract and plot them
  	 
    b.	Please also note that the script removes all zero-read data as part of its data cleaning.
  	
      •	If you would rather include this, please remove the cell that removes zero read data from the variable
  	    filtered_data, and change the formula of the for loop that applies the log2 function to “log2_data[col] =
  	    np.log2(filtered_data[col]) +” a small positive value

The script outputs a PCA plot helping to identify clusters of similar samples, a line plot for each of the selected genes of interest under each of the experimental conditions, and a heatmap for the genes of interest. 

