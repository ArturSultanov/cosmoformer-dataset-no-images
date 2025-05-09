# Cosmoformer Dataset

Dataset repo with pre-downloaded images: https://github.com/ArturSultanov/cosmoformer-dataset.

## Introduction

This repository "Cosmoformer Dataset" contains dataset and pipeline, that was used to prepare dataset for model tratining. Both components are the parts of my Bachelor thesis at Brno Technical University (BUT).

**Thesis title**: AI-Powered Web Application for Galaxy Morphology Classification on Red Hat OpenShift  
**Acad. year**: 2024/2025  
**Department**: Department of Intelligent Systems  
**Type of thesis**: Bachelor's Thesis  
**Language of thesis**: en  
**Thesis focus**: Artificial Intelligence  
**Supervisor**: Mgr. Kamil Malinka, Ph.D.  
**Reviewer**: Ing. Milan Šalko  
**Consultant**: Forde Kieran, Ph.D.  

**Electronic source citation (english):**

    SULTANOV, Artur. AI-Powered Web Application for Galaxy Morphology Classification on Red Hat OpenShift. Online, bachelor's Thesis. Kamil MALINKA (supervisor). Brno: Brno University of Technology, Faculty of Information Technology, 2025. Available at: https://www.vut.cz/en/students/final-thesis/detail/164309. [accessed 2025-04-15].

---

## Installation and Prerequisites

1. Install `Python 3.12` version.
2. Install `Python` packages from <a href="requirements.txt">requirements.txt</a> file.
3. Open <a href="dataset.ipynb"> `dataset.ipynb` </a> file and follow steps inside the Jupyter notebook.

## Dataset overview

Galaxy Zoo 2 project has been used for dataset creation. Dataset represents a three subsets for training, validation and test phases.

Each subset contains following labels:
 - **img_path** - the path to the image file
 - **label** - the correspoding galaxy type

Labes will be saved into `.parquet` files:
 - `train.parquet` - labes for training subset
 - `validation.parquet` - labes for validaion subset 
 - `test.parquet` - labes for test subset
 
Images will be saved into corresponding folders (after running pipeline):
 - `train/` folder contains images for training subset
 - `validaion/` folder contains images for validaion subset
 - `test/` folder contains images for test subset

The sizes of each subset:  
 - Train subset size: 125575  
 - Val subset size:   41859  
 - Test set size:   41859  

## Dataset pipeline

Python `galaxy-datasets`package has been used for data acquisition. The link to the original GitHub page: https://github.com/mwalmsley/galaxy-datasets

Python `scikit-learn` and `pandas` packages have been used for data processing and separation.

### Galaxy Zoo 2

    @article{10.1093/mnras/stt1458,
    author = {Willett, Kyle W. and Lintott, Chris J. and Bamford, Steven P. and Masters, Karen L. and Simmons, Brooke D. and Casteels, Kevin R. V. and Edmondson, Edward M. and Fortson, Lucy F. and Kaviraj, Sugata and Keel, William C. and Melvin, Thomas and Nichol, Robert C. and Raddick, M. Jordan and Schawinski, Kevin and Simpson, Robert J. and Skibba, Ramin A. and Smith, Arfon M. and Thomas, Daniel},
    title = "{Galaxy Zoo 2: detailed morphological classifications for 304 122 galaxies from the Sloan Digital Sky Survey}",
    journal = {Monthly Notices of the Royal Astronomical Society},
    volume = {435},
    number = {4},
    pages = {2835-2860},
    year = {2013},
    month = {09},
    issn = {0035-8711},
    doi = {10.1093/mnras/stt1458},
    }

## Links:
1. Galaxy classification application: https://github.com/ArturSultanov/cosmoformer-application
2. CosmoFormer model: https://github.com/ArturSultanov/cosmoformer-model
3. CosmoFormer dataset: https://github.com/ArturSultanov/cosmoformer-dataset
4. CosmoFormer dataset (no pre-downloaded images): https://github.com/ArturSultanov/cosmoformer-dataset-no-images