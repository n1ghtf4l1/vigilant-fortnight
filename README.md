#### **vigilant-fortnight**

# **Trojan Detection**

##### Detect and Analyze Trojan attacks on deep neural networks that are designed to be difficult to detect. 

### **Overview**

Neural Trojans are a growing concern for the security of ML systems, but little is known about the fundamental offense-defense balance of Trojan detection. Early work suggests that standard Trojan attacks may be easy to detect, but recently it has been shown that in simple cases one can design practically undetectable Trojans.

This repository contains code for the **Trojan Detection Challenge (TDC) NeurIPS 2022** [competition](https://trojandetection.ai/).

There are 3 main tracks for this competition:
- **Trojan Detection Track**: Given a dataset of Trojaned and clean networks spanning multiple data sources, build a Trojan detector that classifies a test set of networks with held-out labels (Trojan, clean). For more information, see here.

- **Trojan Analysis Track**: Given a dataset of Trojaned networks spanning multiple data sources, predict various properties of Trojaned networks on a test set with held-out labels. This track has two subtracks: (1) target label prediction, (2) trigger synthesis. For more information, see here.

- **Evasive Trojans Track**: Given a dataset of clean networks and a list of attack specifications, train a small set of Trojaned networks meeting the specifications and upload them to the evaluation server. The server will verify that the attack specifications are met, then train and evaluate a baseline Trojan detector using held-out clean networks and the submitted Trojaned networks. The task is to create Trojaned networks that are hard to detect. For more information, see here.

The competition has two rounds: In the primary round, participants will compete on the three main tracks. In the final round, the solution of the first-place team in the Evasive Trojans track will be used to train a new set of hard-to-detect Trojans, and participants will compete to detect these networks. For more information on the final round, see here.

## **Contents**

There are four folders corresponding to different tracks and subtracks: 1) Trojan Detection, 2) Trojan Analysis (Target Label Prediction), 3) Trojan Analysis (Trigger Synthesis), and 4) Evasive Trojans. We provide starter code for submitting baselines in ```example_submission.ipynb``` under each folder. The ```tdc_datasets``` folder is expected to be under the same parent directory as ```tdc-starter-kit```. The datasets are available [here](https://zenodo.org/record/6894041). You can download them from the Zenodo website or by running ```download_datasets.py```.

The ```utils.py``` file contains helper functions for loading new models, generating new attack specifications, and training clean/Trojaned networks. This is primarily used for the Evasive Trojans Track starter kit. It also contains the load_data function for loading data sources (CIFAR-10/100, GTSRB, MNIST), which may be of general use. To load GTSRB images, unzip ```gtsrb_preprocessed.zip``` in the data folder (NOTE: This folder is only for storing data sources. The network datasets are stored in tdc_datasets, which must be downloaded from Zenodo). You may need to adjust the paths in the load_data function depending on your working directory. The ```wrn.py``` file contains the definition of the Wide Residual Network class used for CIFAR-10 and CIFAR-100 models. When loading networks from the competition datasets, ```wrn.py``` must be in your path. See the example submission notebooks for details.

## How to Use

**Clone this repository, download the competition [datasets](https://huggingface.co/datasets/anubhavde/trojan-detection/blob/main/tdc_datasets.zip) from my HuggingFace repository and unzip adjacent to the repository**. Ensure that Jupyter version is up-to-date (fairly recent). To avoid errors with model incompatibility, please use PyTorch version 1.11.0. Run one of the example notebooks or start building your own submission.
