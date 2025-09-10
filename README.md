# Identification of chimeric spectra in LC-MS proteomics datasets

## Overview
The dynamic range of peptide abundances in complex proteomic samples analyzed by data-dependent acquisition (DDA) LC-MS often gives rise to chimeric spectra, where peaks from multiple peptide species are collected in the same scan window. This confounds peptide identification in database search algorithms, leading to incorrect protein inference in bottom-up proteomics. Deconvolution of chimeric spectra is essential to accurately quantify proteins and distinguish biochemical pathways involved in diseases such as cancer.

This project explores identification of chimeric spectra in a model LC-MS dataset where bovine serum albumin (BSA) peptides were spiked into E. coli proteomes at varying ratios, isobarically labelled with Tandem Mass Tags (TMT).

## Data & Simulation 
- To generate the simulated BSA dataset, I used the web-tool Fragment Ion Calculator (http://db.systemsbiology.net:8080/proteomicsToolkit/FragIonServlet.html) to simulate trypic digested BSA peptides with TMT modifications.
- LC-MS runs of BSA/E. coli mixtures in .mzML format, not shared because due to lab property restrictions. 

## Usage
Run `Chimeric_spectra_removal_Handover.Rmd` to:
- Use the mzR package to parse .mzML LC-MS proteomics files.
- Extract peak lists and convert metadata into tidy dataframes for downstream analysis.
- Match simulated b- and y-ions of tryptic BSA peptides with precursor–reporter ion pairs.
- Loop through the dataset to identify potential chimeric spectra.

## Files
Input files:
- .mzML files containing MS peaks (not shared due to lab property restrictions).
- `final_simulated_ions_BSA_v2.csv`: Excel dataset of simulated precursor m/z masses and associated b- and y-ions

Project code
- `Chimeric_spectra_removal_Handover.Rmd`: R script to use the mzR package to work with LC-MS proteomics files.
  

