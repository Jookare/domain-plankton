# domain-plankton
Contains instructions for domain adaptations with plankton data

## Dataset
You can download the dataset from this [onedrive-link](https://lut-my.sharepoint.com/:u:/g/personal/joona_kareinen_lut_fi/ET1V8HRoxHBMvfxdhU5gVzUB8hlbDPfsQ34DynQPVsGSHw?e=XLnrNT)-

## Task Description

In this hackathon task, your goal is to develop a deep learning model that can classify plankton species while generalizing to new imaging conditions. You are provided with a dataset containing images of three plankton classes, captured using three different imaging instruments (IFCB, CS, FC). Although all datasets are labeled, during training, you may only use:

- One or two labeled datasets (source domain).  
- Unlabeled images from the test dataset (target domain).

This setup reflects a real-world scenario, where older labeled data is available, but newly collected data lacks annotations. You can download the dataset from here: [link](#).

### Your Challenge:
#### Step 1: Plankton Recognition (Supervised Learning)
- Train a model to classify plankton species using the labeled dataset.  
- Establish a baseline accuracy by testing the model on a different dataset (without adaptation).  

#### Step 2: Domain Adaptation
- Improve model performance on the unlabeled target dataset by incorporating domain adaptation techniques.  

**Example approach:** Train a model on the IFCB dataset and test it on the CS dataset → This serves as your baseline. Then, train using both IFCB and unlabeled CS data to see if you can improve accuracy.  

---

### Hints to Get Started:
- Utilize pretrained models (e.g., ViT-Base, ResNet-18) using the PyTorch Image Models (`timm`) package.  
- You do not have to use the full dataset for training, but can instead utilize a small subset (e.g., 100 images per class) to make training possible on your laptop.  
- You can find more information from the results with the full dataset in the [DAPlankton paper](https://arxiv.org/abs/2402.05615).  

---


### Example Pipeline:
![Example Pipeline](figures/Methods.pdf)  
**Figure:** (a) Supervised training for baseline performance, (b) Training a domain adaptation method using unlabeled target dataset images.  
