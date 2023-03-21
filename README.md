## MED263 - Final Project

This project aims to provide a tutorial on analyzing single-cell RNA sequencing data using the scanpy package. The tutorial is designed for users with basic Python-3 and Jupyter Notebook knowledge.

## Background:
RNA sequencing enables the high throughput quantification of mRNA transcript levels, which can be used downstream for transcriptome assembly, differential expression analysis, biomarker identification, and characterization of cell phenotype. RNA sequencing can mostly be done in two ways: by sequencing the mixed RNA from the source of interest across cells (bulk sequencing) or by sequencing the transcriptomes of each cell individually (single-cell sequencing). Most of the time, mixing the RNA of all the cells is cheaper and easier than single-cell sequencing, which is more expensive and challenging. Bulk RNA-Seq gives cell-averaged expression profiles, which are generally easier to analyze but hide some important complexity. For example, some drugs may only affect certain types of cells or the way those cells communicate with each other; however, even on cultured cells, it is hard to find these cells with simple bulk RNA-seq. So, looking at gene expression in a single cell is essential to find these kinds of connections. Single-cell RNA-seq enables transcriptomic profiling at a single cell resolution, permitting the identification and characterization of different cell types in a bulk tissue sample, as well as the calculation of their relative abundance.

## Goals:
This tutorial aims to provide a step-by-step guide to analyzing single-cell human PBMCs using the scanpy package, from the processed/post-alignment count matrix to transcript expression analysis, clustering, covariate regression, and final publication-ready visualization generation. This practice focuses on quality control and manipulating the downstream count matrix to analyze cell clusters and gain biological insights. We will introduce single cell data, barcoding, subsetting, and clustering using Scanpy. Particularly, we will delve into T cell subsets in a healthy individual using the pbmc8k dataset provided by 10x genomics. We hope to teach basic analysis techniques using Scanpy, the python-community equivalent of the commonly used Seurat package.

## Prerequisites and Installation:
 Users should have a basic knowledge of Python-3 and Jupyter Notebook. Instructions for creating python environment are available on:    
 https://github.com/MED263-WI23/MED263_Intro/blob/main/Step4_Conda_JupyterNotebooks_Tutorial.md

However, you can follow the following steps to create a conda environment to perform the analysis too:       
- conda create --name env_name python==3.9   
- conda activate env_name   
- conda install pip    
- conda install -c anaconda jupyter    
- pip install --user ipykernel    
- python -m ipykernel install --user --name=env_name    

Then, the following python packages need to be installed using pip3 or conda: scanpy and leidenalg.    
To install packages using pip3, use the following command in the python cells provided:      
 - !pip3 install scanpy    
 - !pip3 install leidenalg    

## Usage:
The tutorial starts with loading the publicly available dataset representing 32,738 genes in 2,700 PBMCs using the datasets.pbmc3k() function and storing it in an Anndata structure. Then we first walk through quality control steps and later  perform clustering and visualization of the data.

### Contributors:
This tutorial and its accompanying discussion questions were created by Avery Pong.  Alex Jambor and Behrooz Mamandipoor editted the tutorial and wrote this report.
