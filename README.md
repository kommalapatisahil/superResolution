# superResolution

Machine Learning for super-resolution in turbulent boundary layer data. 

![](https://github.com/kommalapatisahil/superResolution/blob/main/introSR.png)

Contents of the repository. 

## Notebooks

SuperResolution_ANNs_ModelV1.ipynb - Complete work flow: Loads data, converts to low resolution images, trains using Keras, analyze training accuracies and plot a few test cases.

SuperResolution_ANNs.ipynb - Complete work flow: beta version

SuperResolution-wHyperTuning.ipynb - Uses Keras-tuner to obtain optimal hyperparameters.

## Modules

PIVutils.py, PODutils.py, grafteaux.py - Modules containing utility functions to process PIV data, perform POD and vortex identification respectively. 
