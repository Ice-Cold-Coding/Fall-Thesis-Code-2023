# How to run the code

First, create an account on the CBICA Image Processing Portal (https://ipp.cbica.upenn.edu/), then apply for the BraTs 2018 dataset under the MICCAI BraTS 2018 heading.
Extract the data into a specific directory, this directory will act as a backup.

Run the code in File 1, the Nifiti files will be converted to PNG images, these will be stored in a new directory. This directory will contain all the data we will use to train the models.
Use File 2 to split the images into train-test splits with stratified sampling. Following this upload the train and test folders into your Google Drive. Note the Google Drive desktop app allows you to easily sync large amounts of files.
Upload File 3 along with the KAIR-Gaussian_blur_bicubic_interpolation folder onto Google Drive. Note you need to change the train and test directory in the main_train_psnr.py file for it to work in the KAIR-Gaussian_blur_bicubic_interpolation folder. 

After running the code in File 3, Open the superresolution sub-folder in the KAIR-Gaussian_blur_bicubic_interpolation folder and download the images. Note this folder is created only after the model has been trained for at least 1 epoch.
File 4 will now be used to extract the super-resolution images based on the epoch. The images will also be put back into HGG and LGG folders along with creating the train-test-validation splits for the classification task. 
Next run File 5, this will tune the hyper-parameters for the ResNet50. Run File 6 to train and test the ResNet50s and obtain the results.
Additionally, Files 7 and 8 contain the code used to aggregate the performance metrics and create the plots visible in the thesis

Credit to https://github.com/cszn/KAIR/tree/master for providing the code for the SwinIR model

