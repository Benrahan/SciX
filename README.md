# SciX

This is a Github repository for the UNSW SciX program 'Exploring the human genome' for learning Bioinformatics.

This tutorial will follow these steps:

1. Install R and Rstudio
2. Install R packages
3. Download Rscript files and RNA sequencing data
4. Differential expression analysis
5. Gene Set Enrichment Analysis
6. Match differentially expressed genes to Genome Wide Association Studies

# Overview
The central dogma of biology states that DNA is transcribed into RNA which is tranlated into protein. RNA sequencing allows scientists to infer the proteins being produced within the tissues of an individual. By comparing the expression levels of RNA between individuals with disease and healthy controls we can identify potential causes of disease or targets for drug therapies. 

In this study, we have processed raw RNA sequencing data from the brains of people with neurodegenerative disease and healthy controls. These studies include:

# Parkinson's disease
Link to data:
Number of patients:
Number fo controls:

# Alzheimer's disease
Link to data:
Number of patients:
Number of controls:

# Huntingtons disease.
Link to data:
Number of patients:
Number of controls:

The processing pipeline was as follows:
1. Files were downloaded from NCBI GEO
2. Sequencing reads were trimmed with Trimmomatic [REF] to remove adaptors and low quality reads
3. Reads were mapped to the GRCh38 Human genome with STAR [REF] 
4. Transcripts counted and annotated with Stringtie [REF]


# Install R and Rstudio
We will be using the R programming language and the Rstudio IDE for this analysis.

To install R please follow this link to download and install the correct version for your Mac, Windows or Linux computer.
https://cran.csiro.au/

Rstudio can be downloaded and installed at this link:
https://www.rstudio.com/products/rstudio/download/#download

# Install R packages
Once both and R and Rstudio have been installed open up Rstudio.

We will now install the packages required for this study. 
In the window on the left hand side copy and paste these commands.

if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("edgeR")
BiocManager::install("fgsea")
BiocManager::install("msigdb")
install.packages('ggplot2')
install.packages('reshape2')

Then enter the commands with 'shift + enter' or 'run' at the top.

When asked to update all/some/none select all by typing 'a'

To check these packages have been installed correctly enter:

library(ggplot2)
library(reshape2)
library(edgeR)
library(fgsea)
library(msigdbr)








