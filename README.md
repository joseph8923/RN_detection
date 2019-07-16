# RN_detection
Classify waveform signals to Random Noise, Not Random Noise and the Mixture of these two

This project is dedicated to classify continuous waveform in to Random Noise (RN),
not Random Noise (NRN), and the mixture of these two. 

The method is based on a research paper:
Meng, H., Ben-Zion, Y. and Johnson, C., 2019. Detection of random noise and anatomy 
of continuous seismic waveforms in dense array data near Anza California: Geophysical 
Journal International, in revision.

Readme.txt: 
  A file introduces this project.

wvfm.sac: 
  Example waveform recorded by a geophone in SAC formate.

load_sac.m: 
  A Matlab function to read in SAC files.

RN_det_1_xcorr.m: 
  A Matlab script reads in waveform, cuts into small windows, computes 
  cross-correlations of each window pair. This step is time-consuming.
  Please be patient when running this script.

RN_Xcorr.mat: 
  A Matlab data file generated by script RN_det_1_xcorr.m. The big size of this file
  is not supported by GitHub. Please go to google drive link below to download.

  https://drive.google.com/drive/folders/113SK3ZrzhdiTzQgBFm1k35YHiHM2HCyy?usp=sharing

RN_det_2_clst.m: 
   Matlab script reads in RN_Xcorr.mat and classifies the waveform segments into
   RN, NRN, and the mixture.

Fig_1_spectra.png        
Fig_2_classification.png 
Fig_3_results.png: 
   Three figures plated by RN_det_2_clst.m
