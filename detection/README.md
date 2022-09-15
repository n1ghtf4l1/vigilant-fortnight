# **Trojan Detection**

In this [track](https://codalab.lisn.upsaclay.fr/competitions/5951), goal is to build a detector that can tell whether a given neural network contains a Trojan. We provide a dataset of networks with labels (Trojan, clean) for building your detector. Training additional networks to augment this dataset is not allowed. You will submit predictions on a set of validation/test networks to the evaluation server. The validation and test sets have held-out labels. 

**Data**: The training, validation, and test sets have 1,000 networks each. Networks are split evenly across all four data sources. Half of the networks are Trojaned, and there is a 50/50 split between patch and whole-image attacks.

**Metrics**: Submissions will primarily be evaluated using area under the receiver operating characteristic curve (AUROC). An AUROC of 50% is random performance, and higher is better. Secondary metrics include area under the precision-recall curve (AUPR) and false-positive rate at 95% recall (FPR95). AUPR will be used to break ties.

## Contents

Using the MNTD baseline as an example, starter code provided for submission in ```example_submission.ipynb```.
