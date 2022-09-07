# StrainNet
### StrainNet: Improved Myocardial Strain Analysis of Cine MRI by Deep Learning from DENSE
<br/>

## Getting Started
Current version is implemented with Python 3.9 and PyTorch 1.10.0. 

Other packages and versions are listed in `requirements.txt`.
<br/><br/>

## Data
Testing and training data are located at `./data/test_cine/` and `./data/train/` folders. Each subject will be in separate subfolders. For testing, the `input.mat` is a series of binarized images of LV myocardium, with size of [1, N<sub>x</sub>, N<sub>y</sub>, N<sub>t</sub>]. Fot training, additional ground truth displacement `label.mat` is needed, with size of [2, N<sub>x</sub>, N<sub>y</sub>, N<sub>t</sub>].

One example testing and one example traning dataset are provided for reference.
<br/><br/>

## Pre-trained Model
A pre-trained model is shared [here](https://www.dropbox.com/s/yaoqz6gig8kovnn/model_best.pth?dl=0). This model should be at `./saved/models/StrainNet/0422_000912/model_best.pth`.
<br/><br/>

## Testing
A jupyter notebook demo `StrainNet_demo.ipynb` showed the inference of StrainNet, and the testing example results were embedded.

Another way to test is to run the `test_cine.py` file and the corresponding testing configuration is implemented at `config_test_unet_cine.json`.
<br/><br/>

## Training
Run the `train.py` file and the corresponding training configuration is implemented at `config_train_unet.json`.
<br/><br/>
