# **Target Label Prediction**

In this [subtrack](https://codalab.lisn.upsaclay.fr/competitions/5952), goal is to build a multiclass classifier that, given a Trojaned network, identifies the target label of the Trojan attack. The target label of a Trojan attack is the label that the Trojaned network switches to predicting when given an image with the trigger inserted. A dataset has been provided of Trojaned networks with target labels for building your classifier.

**Data**:The training and validation sets have 500 networks each. The test set will have 1,000 networks. Networks are split evenly across all four data sources. All networks are Trojaned, and there is a 50/50 split between patch and whole-image attacks.

**Metric**: Submissions will primarily be evaluated with accuracy on the held-out labels. We also compute accuracy separated by data source (CIFAR-10, CIFAR-100, GTSRB, MNIST). Ties will be broken using accuracy on CIFAR-10. Higher is better.

### **Contents**

Using the MNTD baseline as an example, starter code provided for submission in ```example_submission.ipynb```.
