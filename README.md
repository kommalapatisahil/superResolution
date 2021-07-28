# superResolution

Machine Learning for super-resolution in turbulent boundary layer data. 

Super resolution is a challenging probelem in turbulent datasets, owing to the highly non-linear relationship between the smallest and the largest scales in the data. Traditional techniques involve superresolution by interpolation with higher ordered schemes such as bicubic (3rd ordered) and quintic (5th ordered) polynomial schemes.

It is shown that these schemes are not sufficient and model that could capture a higher level of non-linearity are required to accurately map the low resolution inputs to their high resolution counterparts. 

The framework begins by imputing missing data in the captured datasets. 

![](https://github.com/kommalapatisahil/superResolution/blob/main/files/impute.png)

Once the low resolution snapshots are generated, a shallow neural network is trained to decode them into high resolution snapshots. Here is an example snapshot with low and high resolution images. 
![](https://github.com/kommalapatisahil/superResolution/blob/main/files/lowres_highres.png)


Tensorboard was used for automated hyper parameter tuning in the neural network architecture. The parallel coordinates view was very helpful in identifying the optimal Hparams values and also enabled an estimation of the sensitivity. The learning rate was found to be crucial and a step based decay was used. 

![](https://github.com/kommalapatisahil/superResolution/blob/main/files/tensorboard_demo_SFOV.PNG)

Post training, the results of ML based super resolution are compared against higher order polynomial interpolation based super resolution. 


The neural network produces errors that are 25% lower compared to other methods. 
![](https://github.com/kommalapatisahil/superResolution/blob/main/files/LSR_errors.svg)


Contents of the repository. 

## Notebooks

SuperResolution_ANNs_ModelV1.ipynb - Complete work flow: Loads data, converts to low resolution images, trains using Keras, analyze training accuracies and plot a few test cases.

SuperResolution_ANNs.ipynb - Complete work flow: beta version

SuperResolution-wHyperTuning.ipynb - Uses Keras-tuner to obtain optimal hyperparameters.

## Modules

PIVutils.py, PODutils.py, grafteaux.py - Modules containing utility functions to process PIV data, perform POD and vortex identification respectively. 
