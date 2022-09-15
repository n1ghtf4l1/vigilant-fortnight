### **Trigger Synthesis**

In this [subtrack](https://codalab.lisn.upsaclay.fr/competitions/5953), goal is to reverse-engineer the trigger that a Trojan attack uses given only the Trojaned network as input. This is known as trigger synthesis in the literature. Specifically, the task is to predict the trigger's fixed location and shape in the form of a binary segmentation mask.

**Data**: The training and validation sets have 500 networks each. The test set will have 1,000 networks. Networks are split evenly across all four data sources. All networks are Trojaned, and all Trojans use the patch attack.

**Metrics**: Submissions will be evaluated using intersection over union (IoU) between the predicted and true mask for the Trojan trigger. We do not anticipate any need for tie-breaking. Higher is better.

### **Contents**

Using the MNTD baseline as an example, we provide starter code for submission in ```example_submission.ipynb```.
