
# Sampling Assignment

---

## Objective

The objective of this assignment is to understand the importance of sampling techniques in handling an imbalanced dataset and to analyze how different sampling strategies affect the performance of various machine learning models.

---

## Methodology

- Data Loading: The dataset is loaded into Google Colab using pandas.
- Imbalance Analysis: Class distribution is analyzed using value counts, which confirms that the dataset is highly imbalanced.
- Data Balancing: To handle class imbalance, **random oversampling** is used i.e. Minority class samples are duplicated and the final dataset contains equal samples of both classes.
- Sampling: After balancing the dataset, 5 different types of sampling is aaplied on it.
- Train Models: For each type of sampled data, 5 different models were trained and accuracy was calculated.

---

## Sampling Techniques Used

- **Simple Random Sampling** : Randomly selects a subset of data without bias.
- **Stratified Sampling** : Maintains class proportion in the sample.
- **Cluster Sampling** : Uses the `Time` attribute as a cluster identifier.
- **Bootstrap Sampling** : Sampling with replacement to create a resampled dataset.
- **Systematic Sampling** : Selects every k-th record from the dataset.
  
---

## ML Models Used

- Logistic Regression  
- Decision Tree  
- Random Forest  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)

---

## Results
Different sampling techniques produced different accuracy results for machine learning models. Tree-based models such as Decision Tree and Random Forest showed very high accuracy for Simple Random, Cluster, and Bootstrap sampling due to data duplication, indicating possible overfitting. Stratified Sampling provided more balanced and stable performance across all models. Systematic Sampling resulted in lower but more realistic accuracy values. Overall, sampling technique plays a crucial role in model performance.

| Sampling Techniques | LogReg | DecisionTree | RandomForest | SVM   | KNN   |
|---------------------|--------|--------------|--------------|-------|-------|
| Simple Random       | 90.16  | 98.36        | 100.00       | 70.49 | 95.08 |
| Stratified          | 88.31  | 97.40        | 97.40        | 72.73 | 89.61 |
| Cluster             | 95.65  | 100.00       | 100.00       | 91.30 | 95.65 |
| Bootstrap           | 91.50  | 100.00       | 99.67        | 67.32 | 97.71 |
| Systematic          | 80.95  | 90.48        | 85.71        | 66.67 | 80.95 |


---

## Result Graphs

 **Bar Graph** to compare model accuracy across sampling techniques

<img width="726" height="531" alt="image" src="https://github.com/user-attachments/assets/964f3e4a-d6de-4ed9-b5af-2c0780b58759" />





 **Heatmap** to highlight performance variation

<img width="718" height="597" alt="image" src="https://github.com/user-attachments/assets/af34cbfd-f81b-4ccc-962f-3ee6bd166b31" />


---

## Conclusion
The dataset was initially imbalanced and was successfully balanced using oversampling. Experimental results show that no single sampling technique is best for all models. While Cluster and Bootstrap sampling gave higher accuracy, Stratified Sampling produced more reliable and consistent results. Hence, proper sampling selection is essential for building accurate models.    chnage its wording as i want to paste it somewhere else
