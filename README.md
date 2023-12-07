# Upscale your Images using DEEP SUPER RESOLUTION with ESRGAN and SRGAN
# ESRGAN 
# 1. Clone Repo
Git clone -  https://github.com/xinntao/ESRGAN	

# 2. Download Pre-Trained Model 
Get Model - https://drive.google.com/drive/u/0/folders/17VYV_SoZZesU6mbxz2dMAIccSSlqLecY

# 3. Install Dependencies
pip install Pytorch CUDA
pip install opencv-python glob2

# 4. Grab Low Resolution Image and Run Script
Place low resolution image in LR folder 
Run ppython test.py


# SRGAN on Custom Dataset
Learn how to train SRGAN on Custom dataset

## Environment Setup
Open anaconda prompt and cd to the folder where you have your environment.yml file

conda env create -f environment.yml

conda activate srganenv_gpu 


Now Install Pytorch as per your resources

#### GPU
conda install pytorch==1.1.0 torchvision==0.3.0 cudatoolkit=10.0 -c pytorch

##### CPU Only
conda install pytorch-cpu==1.1.0 torchvision-cpu==0.3.0 cpuonly -c pytorch


#### Train your Model:
!python main.py --LR_path custom_dataset_cars/hr_train_LR --GT_path custom_dataset_cars/hr_train_HR

#### Test your Model:
!python main.py --mode test_only --LR_path test_data/cars --generator_path ./model/srgan_custom.pt
