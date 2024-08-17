# Property_tax_fraud_detection
![pasted image 0](https://github.com/user-attachments/assets/bfc1d2d1-301d-4e5d-9395-9aac3ab667ce) 

In this project, we addressed the issue of identifying property tax fraud in New York City using anomaly detection techniques. The dataset comprised over one million property records, including various numeric and categorical fields. Our approach involved data cleaning, variable creation, dimensionality reduction, and the implementation of two anomaly detection algorithms. By ranking the records based on these algorithms, we identified the most suspicious property records.

ML Pipeline:
training data: data_small.xlsx
1. Data Exploration: NY DQR.ipynb
2. Unsupervised anomaly dtection: NY unsupervised fraud.ipynb

Summary Steps:
1. Data Cleaning: We removed irrelevant government property records and imputed null values using targeted methodologies.
2. Variable Creation: We generated new variables to capture property value, area metrics, and ratios that could indicate anomalies.
3. Dimensionality Reduction: Using Principal Component Analysis (PCA), we reduced the dimensionality of the data to five principal components, ensuring they were orthogonal and similarly scaled.
4. Anomaly Detection Algorithms: We implemented two algorithms:
Algorithm 1: Calculated a score based on the sum of Z-scores for each feature.
Algorithm 2: Used an AutoEncoder to measure the error between actual Z-scores and predicted Z-scores.
We ranked the records based on these scores and selected the maximum rank from the two algorithms to identify anomalies.
The results were summarized in the NY_top_with_zs.xlsx file, containing the top 10,000 suspicious property records. Additionally, due to a significant number of anomalies arising from null values in lot and building sizes, we produced two supplementary files: NY_top_sizes_ne_0.xlsx and NY_top_lotsize_ne_0.xlsx.
   
