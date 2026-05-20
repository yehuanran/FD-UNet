# FD-UNet: A Frequency Decoupled U-Net for Building Segmentation in High-Resolution Remote Sensing Imagery

This is an official PyTorch implementation of "[**FD-UNet: A Frequency Decoupled U-Net for Building Segmentation in High-Resolution Remote Sensing Imagery**]".

# Introduction

<center> 
<img src="DRAU-Net.png" width="auto" height="auto">
</center>

# Image segmentation

## 1. Requirements
```
# Environments:
cuda==11.8
python==3.9
# Dependencies:
pip install torch==2.0.0 torchvision==0.22.1
pip install einops==0.6.1 imageio==2.28.1   albumentations   Torchmetrics==0.11.4
```

## 2. Data Preparation

```
│inria/
├──austin1/
│  ├── images
│  │   ├── austin1.jpg
│  │   ├── ......
│  ├── binary_masks
├──austin2/
│  ├── images
│  │   ├── austin2.jpg
│  │   ├── ......
│  ├── ......
```

## 3. Train

python train.py --dataset inria 

## 4. Validation

python test.py --load_checkpoint output/checkpoints/20250401-0413_unet/20250401-0413_unet_e1.pt

