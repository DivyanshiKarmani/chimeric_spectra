# Identification of chimeric spectra in LC-MS proteomics datasets

## Overview
The dynamic range of peptide amounts in complex proteomic samples scanned by Data-Dependent Acquisition (DDA) LC-MS gives rise to chimeric spectra, where MS peaks of two different peptide species are collected in the same scan window. This confounds peptide identifications when using database search algorithms to identify peptides and infer protein ID in bottom-up proteomics. Deconvolution of chimeric spectra is essential to accurately determine protein amounts, which differentiate biochemical pathways involved in diseases including cancer. 

This project is an attempt to identify chimeric spectra in a LC-MS proteomic dataset containing BSA peptides spiked in with E. coli proteins, with different ratios isobarically labelled using Tandem Mass Tags (TMT). 

To generate the simulated BSA dataset, I used the web-tool Fragment Ion Calculator (http://db.systemsbiology.net:8080/proteomicsToolkit/FragIonServlet.html) to simulate trypic digested BSA peptides with TMT modifications. 

## Usage
Run the R script called `Chimeric_spectra_removal_Handover.Rmd` to see the extraction of peaks into metadatasets from .mzML LC-MS files, followed by matching simulated b- and y-ions of trypic diegsted BSA peptides with precursor-reporter ion pairs in the dataset. I attempted to do this by looping the large dataset. 

## Files
- :.mzML files containing MS peaks
- `final_simulated_ions_BSA_v2.csv`: Excel dataset of simulated precursor m/z masses and associated b- and y-ions
- `Chimeric_spectra_removal_Handover.Rmd`: R script to use the mzR package to work with LC-MS proteomics files.
  

