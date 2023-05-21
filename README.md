# Classification_of_High_Energy_Physics_particles

Introduction
Aim of the project
This project aims to study different classification algorithms used in Machine Learning domain. For this purpose, a signal-background classification problem is considered.

Particle Accelerators are primarily used to collide sub-atomic particles to study their nature. Generally, such collisions produce some particles which decay quickly into decay products making it difficult for the sensors to detect their presence in the collider.

The other thing that makes the problem more difficult is that the decay products formed from both the signal process (exotic particle is generated and decays) and background-process (exotic particle is not generated) are same. [5]

Information about the dataset
Thus, to analyze their presence HEPMASS dataset was generated using Monte-Carlo simulations of the collisions producing such exotic particles. The data set is produced such that 50% of the data is from signal process and the remaining 50%of the data set is from the background process. As the mass of the particles is unknown the mass is distributed uniformly from the set {500, 750, 1000, 1250, 1500} and is fed as one of the input feature. Apart from this the original dataset has 10500000 number of instances with 28 attributes.

The class label is present in the first column. The features are present from column 2 to column 27 (22 low-level features and 5 high level features) and are already normalized. [4]

In order to understand the relative behaviour of these algorithms, the data set was trimmed and first 500000 samples were considered for the purpose of this project. As the dataset is simulaed with uniform distribution of signal and background processes, this would not affect the results in terms of bias in training over either target.

Further, this dataset is split as 70 percent for training and 30 percent for testing purposes.

HARDWARE:
Implemented on Tesla K80 GPU and 12 GB of RAM on Google Colab

Brief overview of methods:
In this report, classification is done using tree structures. Following tree based algorithms are harnessed.

1] Decision tree Classifier: Decision Tree is constructed by splitting the input space, to optimize certain parameter (e.g maximize the information gain or minimize the gini impurity), across a feature sequentially until the input space partitions can be mapped into the target space partitions.

2] Random Forest Classifier: Random Forest is constructed by constructing many decision trees froma randomly sampled data set with replacement and splitting the nodes at optimal features. The final classification is decided by drawing out a vote from all the trees.

3] Extra-Tree Classifier: Extra-Tree Classifier works just like random-forest classifier except that the data is sampled without replacement in this method and the nodes are split at random instead of calculating the optimal features which reduces the computational burden.

4] XgBoost Classifier XgBoost Classifier implements boosting trees algorithm, wherein the trees are constructed sequentially, by considering the prediction of the previous tree, to minimize the loss of prediction.

Finally, a comparative analysis of their performance is done.

