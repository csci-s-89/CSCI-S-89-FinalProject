# <img style="float: left; padding-right: 10px; width: 45px" src="https://raw.githubusercontent.com/Harvard-HES-ALM/master/main/ds-masters/content/images/hes-logo.png"> CSCI S-89: Introduction to Deep Learning
</br>

**Harvard Summer School**<br/>
**Summer 2024**<br/>
**Instructor**: Dmitry Kurochkin<br/>
**Student**: Artemio Mendoza-García</br>
**Date**: 05/AUG/2024</br>

## Final Project

### From CelebA to Real-World: improving Face Restoration Models for Diverse Image Degradations
<hr style="height:2pt">

#### Intro

This project investigates the application of advanced deep learning techniques to reconstruct high-quality human face images from severely distorted inputs, by developing and comparing three distinct approaches: a custom-built autoencoder, the state-of-the-art CodeFormer model, and a fine-tuned version of CodeFormer using transfer learning.

We stablished a baseline by building a custom autoencoder from scratch. It  was trained on 180,000 images from the CelebA dataset with artificially added random noise to simulate blur. For transfer learning, we fine-tuned the pre-trained CodeFormer model on a subset of 10,000 blurred CelebA images. We also evaluated the performance of the original pre-trained, state-of-the-art (SOTA) CodeFormer without modifications.
Our results demonstrate significant improvements over baseline methods, with each model showing distinct strengths. The custom autoencoder performed well on CelebA test images but struggled with real-world samples. The original CodeFormer excelled in restoring real-world images but underperformed on our specific CelebA blur. The transfer learning model achieved a balance, improving performance on CelebA while maintaining reasonable real-world image restoration. 

#### Dependencies and Installation 

```
# git clone this repository
git clone https://github.com/csci-s-89/CSCI-S-89-FinalProject.git


# create new anaconda env
conda create -f s89-finalProject.yml -y
conda activate s89-finalProject

# Custom Autoencoder Notebook
cd CustomAutoEncoder
code AutoEncoder.ipynb

# Transfer Learning Notebook
cd TransferLearning
code TransferLearning.ipynb
```