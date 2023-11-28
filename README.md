# How to run the code

First, create an account on the CBICA Image Processing Portal (https://ipp.cbica.upenn.edu/), then apply for the BraTs 2018 dataset under the MICCAI BraTS 2018 heading.
Extract the data into a specific directory, this directory will act as a backup.

Run the code in File 1, the Nifiti files will be converted to PNG images, these will be stored in a new directory. This directory will contain all the data we will use the train the models.
Use File 2 to spit the images into train-test splits with stratified sampling. Following this upload the train and test folders into your Google Drive. Note the Google Drive desktop app allows you to easily sync large amounts of files.
Upload File 3 along with the KAIR-Gaussian_blur_bicubic_interpolation folder onto Google Drive. Note you need to change the train and test directory in the main_train_psnr.py file for it to work. 

Open the superresolution sub-folder in the KAIR-Gaussian_blur_bicubic_interpolation folder and download the images. File 4 will now be used to extract the superresolution images based on the epoch that you want and will put them back into HGG and LGG foldlers.


