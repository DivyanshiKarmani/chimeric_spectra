# Identification of chimeric spectra in LC-MS proteomics datasets

## Overview
The dynamic range of peptide amounts in complex proteomic samples scanned by Data-Dependent Acquisition (DDA) LC-MS gives rise to chimeric spectra, where MS peaks of two different peptide species are collected in the same scan window. This confounds peptide identifications when using database search algorithms to identify peptides and infer protein ID in bottom-up proteomics. Deconvolution of chimeric spectra is essential to accurately determine protein amounts, which differentiate biochemical pathways involved in diseases including cancer. 

This project is an attempt to identify chimeric spectra in a LC-MS proteomic dataset containing BSA peptides spiked in with E. coli proteins. 

## Usage
Run the R script called .rmd to see the extraction of peaks into metadatasets from .mzML LC-MS files. 
