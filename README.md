Sampling Assignment
Objective

This assignment aims to explore the role of sampling techniques in managing imbalanced datasets and to evaluate how different sampling methods influence the performance of machine learning models.

Methodology
Data Loading: The dataset was imported into Google Colab using the pandas library.
Imbalance Analysis: Class distribution was examined using value counts, revealing a significant imbalance between classes.
Data Balancing: Random oversampling was applied to address the imbalance by duplicating minority class samples, resulting in an equal number of instances for each class.
Sampling Process: After balancing the dataset, five different sampling techniques were implemented.
Model Training: For each sampled dataset, five machine learning models were trained and their accuracies were recorded.
Sampling Techniques Applied
Simple Random Sampling: Selects data points randomly without considering any structure.
Stratified Sampling: Ensures that class proportions remain consistent within the sample.
Cluster Sampling: Groups data based on the Time attribute and samples from these clusters.
Bootstrap Sampling: Generates new datasets by sampling with replacement.
Systematic Sampling: Picks samples at regular intervals (every k-th record).
Machine Learning Models Used
Logistic Regression
Decision Tree
Random Forest
Support Vector Machine (SVM)
K-Nearest Neighbors (KNN)
Results

The performance of machine learning models varied significantly depending on the sampling technique used. Tree-based models such as Decision Tree and Random Forest achieved extremely high accuracy with Simple Random, Cluster, and Bootstrap sampling, likely due to overfitting caused by duplicated data.

Stratified Sampling provided more stable and balanced results across all models. In contrast, Systematic Sampling yielded comparatively lower but more realistic accuracy values. Overall, the choice of sampling method had a substantial impact on model performance.

Sampling Techniques	LogReg	DecisionTree	RandomForest	SVM	KNN
Simple Random	90.16	98.36	100.00	70.49	95.08
Stratified	88.31	97.40	97.40	72.73	89.61
Cluster	95.65	100.00	100.00	91.30	95.65
Bootstrap	91.50	100.00	99.67	67.32	97.71
Systematic	80.95	90.48	85.71	66.67	80.95
Visualization
A bar chart was used to compare model accuracy across different sampling techniques.
A heatmap was created to visualize performance variations and identify patterns across models and sampling methods.
Conclusion

The dataset initially exhibited class imbalance, which was effectively addressed using random oversampling. The experimental findings indicate that no single sampling method performs best across all models. Although Cluster and Bootstrap sampling produced higher accuracy scores, these results may reflect overfitting.

Stratified Sampling, on the other hand, delivered more consistent and reliable performance. Therefore, selecting an appropriate sampling technique is crucial for building robust and generalizable machine learning models.
