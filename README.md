# Image-Analysis--1P-Voltage-datasets-of-Spiking-HEK-cells-expressing-GEVIs
This repository contains the python codes for the image analysis of one-photon (1P) voltage imaging datasets of spiking HEK cells (sHEK) expressing Genetically Encoded Voltage Indicators (GEVIs). 

The pipeline_version1.ipynb file contains the image analysis python code. To run the pipeline, install the caiman environment from https://github.com/flatironinstitute/CaImAn. 
The pipeline first motion corrects the uploaded 1P movies of sHEK cells expressing GEVIs. These movies are recorded on the octoscope. 

From the motion corrected movie, a 2-D mean + correlation image of the 3-D dataset is created. This is the input to the segmentation model.
The segmentation model used in this image analysis pipeline is U-Net. The re_trained_UNet.ipynb file contains the code of the U-Net model. The U-Net model is re-trained for segmentation of sHEK datasets. The re-training of the U-Net model is performed using the python codes available in model_re_training.ipynb and dataset.ipynb. The original pre-trained U-Net model is downloaded from https://github.com/milesial/Pytorch-UNet.

The re-trained U-Net model predicts binary masks of the sHEK cells. From these binary masks, features of the GEVIs expressed by the sHEK cells are extracted. The image analysis pipeline extracts the sensitivity, speed and, membrane localization values of the GEVIs expressed by the segmented sHEK cells. 
