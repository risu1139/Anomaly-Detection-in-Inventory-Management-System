KNN-Based Heuristic Algorithm for Real-Time Anomaly Detection

Overview

This project implements a KNN-based heuristic algorithm designed to tackle speed, scalability, and accuracy challenges commonly encountered in anomaly detection. It is particularly suited for processing large datasets in real-time, with applications such as inventory management and order anomaly detection in retail environments.

Problem Statement

Traditional anomaly detection algorithms often face limitations in processing speed, scalability, and accuracy, especially when dealing with large datasets. This project introduces a heuristic approach that focuses on localized computation and range-based validation to optimize performance across these dimensions.

Key Features

KNN-based Localized Computation: Utilizes a K-nearest neighbours approach to reduce computational complexity by focusing on the most relevant data points.
Mean-based Prediction: Predicts anomalies based on the mean of the nearest neighbours, reducing reliance on complex calculations while maintaining high accuracy.
Range-based Validation: Classifies anomalies by comparing predictions against a defined range (mean ± standard deviation) of local neighbours' transactions.
Real-time Performance: The algorithm's simplified approach facilitates real-time or near-real-time anomaly detection.
Heuristic Approach

Steps:
Find K Nearest Neighbours: Identify the nearest neighbours of a data point to create a subset of relevant data.
Calculate the Mean: Compute the mean transaction value of the nearest neighbours.
Calculate Variance: Determine the variance to assess variability.
Define Range: Create a range from the mean - standard deviation to mean + standard deviation.
Classify Anomaly: Classify the data point as anomalous if it falls outside the calculated range.
Heuristic Methodology:
Nearest Neighbours Simplification: By focusing only on K nearest neighbours instead of the entire dataset, the algorithm significantly reduces computational load.
Localized Computation: Reduces the burden of global analysis, instead focusing on a local neighborhood around each data point.
Mean-based Prediction: Uses the mean of the nearest neighbours to predict normalcy, simplifying calculations while preserving accuracy.
Range-based Validation: Compares the predicted value against a locally defined range to quickly determine anomalies.
Range Calculation

The algorithm defines an acceptable range as the mean ± one standard deviation of the nearest neighbours' transactions. This range captures typical variability in transaction values and has been empirically shown to strike the best balance between avoiding false positives and minimizing false negatives, thereby optimizing the detection performance.

Impact

Speed Enhancement: The localized approach reduces computational complexity, speeding up the algorithm significantly, even for large datasets.
Scalability: Simplified calculations make the algorithm scalable, allowing it to handle growing datasets without large increases in processing time or resources.
Real-time Capabilities: The reduced computational burden enables real-time anomaly detection, making it suitable for time-sensitive applications.
Performance Metrics

Surpassed benchmarks with over 9% improvement in accuracy and 21% improvement in F1 score compared to algorithms like Isolation Forest.
Achieved >99% accuracy and >0.98 F1 score on datasets with orders of 100+, showcasing top performance across varying dataset sizes.
Conclusion

This KNN-based heuristic algorithm offers a powerful solution to the common challenges of speed, scalability, and accuracy in anomaly detection. Its localized and range-based approach ensures efficient, real-time processing, making it ideal for data-intensive applications like inventory management and retail order anomaly detection.
