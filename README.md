# Massaly-Ibrahim-2022
Codes used to analyze fiber photometry experiments in "Dorsal Hippocampus To Nucleus Accumbens Projections Drive Reinforcement Via Activation of Accumbal Dynorphin Neurons" manuscript.

## Overview
There are two different custom MATLAB codes used in this manuscript. 
1) To analyze calcium transients paired with dHPC stimulation in the self-stimulation paradigm (Fig 2G-J) and to cue onset (SFig 1A-D).
2) To analyze calcium transients paired with non-contingent (experimenter-controlled) dHPC stimulation (Fig 4A-D; SFig 1E-H)

## System Requirements
### Hardware requirements
It requires only a standard computer with enough RAM to support the in-memory operations.
### Software requirements
The Matlab version used was R2019b and it was tested on Windows 10 with 8GB of RAM and 64-bit operating system.

## Installation Guide
Documentation on how to install Matlab and license required to run the program can be found on MathWorks website (https://www.mathworks.com/help/install/). The typical installation time is about 30 minutes depanding on the computer model, configuration and internet connection.

Since these recording were taken using Tucker-Davis Technology (TDT) fiber photometry system, a MATLAB SDK file is required to read TDT file directly into MATLAB post-recording. This SDK file and documentation can be found on TDT website (https://www.tdt.com/docs/sdk/offline-data-analysis/offline-data-matlab/getting-started/). Add the TDTMatlabSDK folder into the computer Matlab folder.

## How To Use
### Analysis of calcium transients in self-stimulation paradigm (Fig 2G-J and SFig 1A-D).
1) Open the `Photometry and self-stim` folder and download the Matlab code (PhotometryZScoreAnalysis_forPtAB_selfstim_15Aug22).
2) Download the example data folder from [this link](https://wustl.box.com/s/u0dy3uubmhw614c00cquz4iot8l53eab)
3) Unzip the example data folder and ensure that folder is copied into `MATLAB\TDTMatlabSDK\Examples\` directory.
4) Open the code (PhotometryZScoreAnalysis_forPtAB_selfstim_15Aug22) in your Matlab program.
5) Ensure that the BLOCKPATH is reading from the correct data folder, which is in this case is `'FP_SelfStim_Example-201130-083802'`
![image](https://user-images.githubusercontent.com/60552089/184723906-000f999b-bf3f-462b-b38c-363d912677db.png)
6) Set up the variable that you want to extract. In this code, variable value 1 is cue onset and variable value 6 is photo-stimulation
![image](https://user-images.githubusercontent.com/60552089/184724343-c0da6555-ca0c-4fbc-a75f-2c672a46dd9d.png)
7) Run the code!
8) You should get the following output in a separate window:
  (Top Left): Epoch Response from both 470 and 405 channels with onset at 0s
  (Top Right): Z-Score heatmap for all the trials recorded in this example data
  (Bottom Left): Z-Score Epoch Response for all trials
  (Bottom Right): Area under the curve 2 seconds pre and post event onset
  ![image](https://user-images.githubusercontent.com/60552089/184725087-15238505-1cd9-4a29-a419-587a3303edb5.png)
  
  ### Analysis of calcium transients in non-contingent (experimenter-controlled) dHPC stimulation (Fig 4A-D; SFig 1E-H).
1) Open the `Photometry and experimenter` folder and download the Matlab code (PhotometryZScoreAnalysis_forScore_experimenter_15Aug22).
2) Download the example data folder from [this link](https://wustl.box.com/s/tacboojptlf621ndnv26f6iyd4t65k83)
3) Unzip the example data folder and ensure that folder is copied into `MATLAB\TDTMatlabSDK\Examples\` directory.
4) Open the code (PhotometryZScoreAnalysis_forScore_experimenter_15Aug22) in your Matlab program.
5) Ensure that the BLOCKPATH is reading from the correct data folder, which is in this case is `'FP_Experimeter_Example-220602-162235'`
![image](https://user-images.githubusercontent.com/60552089/184731992-51935248-16fe-47db-9e8c-917a4bf99cc7.png)
6) In this code, variable value is 1 which has been paired with experimenter delivered stimulation.
![image](https://user-images.githubusercontent.com/60552089/184732278-8c16c8e6-9554-499a-96b2-4b9e184827db.png)
7) Run the code!
8) You should get the following output in a separate window:
  (Top Left): Epoch Response from both 470 and 405 channels with onset at 0s
  (Top Right): Z-Score heatmap for all the trials recorded in this example data
  (Bottom Left): Z-Score Epoch Response for all trials
  (Bottom Right): Area under the curve 2 seconds pre and post event onset
  ![image](https://user-images.githubusercontent.com/60552089/184732491-3033da72-f0a7-4741-8165-27fef638ffb9.png)
