# Colon-cancer-dt-classifier
This project shows the use of Decision Tree classifiers in Apache Spark's MLlib library to classify samples in the Colon Cancer dataset. We focus on understanding the decision tree parameters, training the model, testing it and evaluating its performance. The dataset is **"Colon Cancer Dataset"** which contains physical attributes of samples and the corresponding class labels like cancerous or non-cancerous. The motive is to predict the class label based on the features.

## DT parameters
- **maxBins:** Used to define the number of bins utilized while tuning continuous features. Fine split decisions can be considered by increasing the number of manBins, also increasing computation and communication. The maxBins should be the maximum number of categories of any categorical feature.
- **maxMemoryInMB:** Throughout the training process, this determines how much memory or space, or RAM can be utilized to store accurate statistics. To guarantee compatibility with a variety of circumstances, the default values are selected conservatively. We can speed up the training process by increasing the amount of maxMemoryInMB.
- **subsamplingRate:** Proportion of training data is determined to train the decision tree in this parameter. It is necessary for training Random Forest and GradientBoostedTrees as subsampling the initial dataset can give a variety among trees.
- **Impurity:** This is used to compare the candidate splits and must be appropriate according to the decision tree algorithm applied. This parameter makes sure that an optimal split is chosen based on the impurity measure.


## Output
<img width="1096" height="685" alt="image" src="https://github.com/user-attachments/assets/b5721a94-797f-4413-9b39-c2fc311bd436" />

The test error is **0.176** according to the sample screnshot above, which means accuracy of approximately 82% on the unseen test data. The model learned a tree of depth 3 with 9 nodes, indicating it made three hierarchical splits to classify the samples. Each internal node represents a decision based on a feature threshold, and the leaf nodes represent the predicted class labels.

The relatively low depth suggests that the model is not overfitting and is able to generalize reasonably well to new data.
