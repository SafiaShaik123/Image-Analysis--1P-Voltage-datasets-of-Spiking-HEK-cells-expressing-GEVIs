# Image-Analysis--1P-Voltage-datasets-of-Spiking-HEK-cells-expressing-GEVIs
This repository contains the python codes for the image analysis of one-photon (1P) voltage imaging datasets of spiking HEK cells (sHEK) expressing Genetically Encoded Voltage Indicators (GEVIs). 

The pipeline_version1.ipynb file contains the image analysis python code. To run the pipeline, install the caiman environment from https://github.com/flatironinstitute/CaImAn. 
The pipeline first motion corrects the uploaded 1P movies of sHEK cells expressing GEVIs. From the motion corrected movie, a 2-D mean + correlation image of the 3-D dataset is created. This is the input to the segmentation model.
The segmentation model used in this pipeline is U-Net. The re_trained_UNet.ipynb file contains the code of the U-Net model. The U-Net model is re-trained for segmentation of sHEK datasets. 
