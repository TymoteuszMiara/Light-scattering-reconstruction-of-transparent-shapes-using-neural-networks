# Light-scattering reconstruction of transparent shapes using neural networks
 
This repository publishes the code for the reconstruction of a translucent sheet which may translate, rotate and change its shape. 
We provide two demos: 
1. A set of raw images in the folder DemoExperiment obtained by dynamically scanning a PDMS sheet of radius 19.0 mm and thickness of 50 microns with a projector-camera system. The folder is accompanied by a config file DemoExperiment.txt which contains all necessary information about the system which is used by the HypercloudExtractor.nb Mathematica notebook to generate the hypercloud from the raw images i.e. a set of {x_ij, y_ij, z_ij t_ij} data where i labels scans and j lapels points in each scan. Running this notebook will generate a dump file DemoExperiment.mx which can then be imported by the SurfaceFitter.nb notebook for reconstruction. See the comments in the code of HypercloudExtractor.nb for further details of how the config file is specified.
2. A synthetic 'flattened' hypercloud i.e. a set of (x_i, y_i, z_i, t_i) points of a sheet dynamically wrapping around a log spiral of dynamically varying pitch while translating and rotating. This set is generated synthetically but simulates a similar camera-projector scanning method.

Once the hypercloud is created by the HypercloudExtractor.nb or otherwise, the SurfaceFitter.nb notebook imports it and finds a time-dependent parametrisation of the surface of the sheet using an autoencoder. 


