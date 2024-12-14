# Bearing Failure Detection

This project is an extensive exploration of bearing failure detection using various statistical and machine learning models. It processes and analyzes vibration data from bearings to detect anomalies and predict failure events using advanced techniques such as Isolation Forest, One-Class SVM, Local Outlier Factor, and Autoencoders.


## Objectives

- **Data Processing:** Extract and preprocess vibration signal data from multiple test sets.
- **Feature Extraction:** Calculate statistical signal-based features for better anomaly detection.
- **Anomaly Detection Models:** Implement multiple anomaly detection models to identify bearing failures.
- **Evaluation:** Compare the performance of different methods in identifying anomalies.
- **Insights:** Gain insights into the timeline and characteristics of bearing failures.


## Dataset Description

The dataset consists of vibration signals collected from test-to-failure experiments conducted on bearings:

### Test Set 1:
- **Recording Duration:** October 22, 2003 - November 25, 2003
- **Files:** 2,156 (ASCII format)
- **Channels:** 8
- **Description:** Inner race defect in Bearing 3, roller element defect in Bearing 4.

### Test Set 2:
- **Recording Duration:** February 12, 2004 - February 19, 2004
- **Files:** 984 (ASCII format)
- **Channels:** 4
- **Description:** Outer race failure in Bearing 1.

### Test Set 3:
- **Recording Duration:** March 4, 2004 - April 4, 2004
- **Files:** 4,448 (ASCII format)
- **Channels:** 4
- **Description:** Outer race failure in Bearing 3.


## Models Used

1. **Isolation Forest**
   - Identifies anomalies based on the isolation of data points.
   - Parameters: `n_estimators`, `contamination`.

2. **One-Class SVM**
   - Detects anomalies using Support Vector Machines.
   - Kernel: `rbf`, Parameters: `nu`, `gamma`.

3. **Local Outlier Factor (LOF)**
   - Identifies outliers by comparing the local density of points.
   - Parameters: `n_neighbors`, `contamination`.

4. **Autoencoders**
   - Uses neural networks to reconstruct input and calculate reconstruction errors to identify anomalies.

5. **Mahalanobis Distance**
   - Statistical measure to detect outliers based on covariance and mean.


## Key Insights

- **Test Set 1:**
  - Detected anomalies toward the end of the test, highlighting defects in Bearing 3 (inner race) and Bearing 4 (roller element).

- **Test Set 2:**
  - Significant rise in vibration for Bearing 1 towards the end, indicating outer race failure.

- **Test Set 3:**
  - Sharp increase in vibration for Bearing 3 at the end, confirming the outer race defect.


## Business Recommendations

1. Implement predictive maintenance using Autoencoders and Isolation Forest models.
2. Continuously monitor vibration signals to detect anomalies before failure.
3. Use statistical feature extraction to enhance anomaly detection models.
4. Adjust machine operation parameters when anomalies are detected to prevent catastrophic failures.


## Results

| Model                  | Test Set 1 Anomalies | Test Set 2 Anomalies | Test Set 3 Anomalies |
|------------------------|----------------------|----------------------|----------------------|
| Isolation Forest       | Optimal Detection   | Optimal Detection   | Optimal Detection   |
| One-Class SVM          | High False Positives| Adjusted Parameters | Adjusted Parameters |
| Local Outlier Factor   | Tuned Parameters    | Tuned Parameters    | Tuned Parameters    |
| Autoencoders           | Best Reconstruction | Best Reconstruction | Best Reconstruction |
| Mahalanobis Distance   | Statistical Baseline| Statistical Baseline| Statistical Baseline|


## Technologies Used

- **Python** (Pandas, NumPy, Scikit-learn, TensorFlow, Matplotlib, Seaborn)
- **Google Colab** for cloud-based computation
- **7-Zip** for dataset extraction


## How to Run the Project

1. **Setup Environment:**
   - Mount Google Drive in Google Colab.
   - Install required Python libraries.

2. **Download Dataset:**
   - Use the provided `wget` command to download the dataset.

3. **Preprocess Data:**
   - Extract and preprocess vibration signal data.

4. **Feature Extraction:**
   - Calculate signal-based statistical features such as mean, standard deviation, skewness, kurtosis, entropy, RMS, etc.

5. **Run Models:**
   - Train and evaluate anomaly detection models.

6. **Visualize Results:**
   - Generate plots highlighting detected anomalies.

7. **Save Results:**
   - Save processed data and anomaly detection results as CSV files.


## Folder Structure

```plaintext
Root/
├── Data/
│   ├── 1st_test/
│   ├── 2nd_test/
│   ├── 3rd_test/
├── ProcessedData/
│   ├── MergedData/
│   ├── Test1_TimeFeatures.csv
│   ├── Test2_TimeFeatures.csv
│   ├── Test3_TimeFeatures.csv
├── AnomalyDetection/
│   ├── BearingTest_1_Anomalies.csv
│   ├── BearingTest_2_Anomalies.csv
│   ├── BearingTest_3_Anomalies.csv
└── Readme Document for IMS Bearing Data.pdf
```


## License

This project is provided for educational and research purposes. Please reference the original dataset source for any publication or presentation.

## **Author**
**Faizan Bhutto**  
[LinkedIn](https://www.linkedin.com/in/faizanbhutto) | [GitHub](https://github.com/bhutto17)

Feel free to reach out if you have any questions or feedback regarding this project.

