# Cyber-Threat-Detection
The Aegean WiFi Intrusion/threat Dataset (AWID2) project was prepared and managed by
George Mason University (U.S.) and University of the Aegean (Greece). The objective was
to survey and evaluate research in cyber threat detection. A standard set of data to be
audited, which includes real traces of both normal and intrusive 802.11 traffic with a wide
variety of cyber threats/intrusions simulated in a physical lab which realistically emulates a
typical SOHO infrastructure, was provided.

Details of the dataset can be found in the page below.
http://icsdweb.aegean.gr/awid/draft-Intrusion-Detection-in-802-11-Networks-Empirical-Evaluation-of-Threats-and-a-Public-Dataset.pdf

The AWID dataset categorises the cyber attacks into 4 different categories viz. Injection attacks, Flooding attacks, Impersonation attacks and Passive attacks
I have used the reduced CLS portion of the AWID2 dataset only which concentrates on Impersonation attacks. 

The major tasks in this project are

a. Feature Generation and Extraction - This is particularly important as we have around 154 features in the dataset. To make a classifcation algorithm learn all these features and then predict
if the data is a threat or not creates a case of 'Curse of Dimensionality'. It is therefore important that we select and provide only the important features to the classification algorithms.

b. Machine Learning Algorithms - Once the important features have been determined, they can then be supplied to the Classification Algorithms to predict if the datapoint is a cyber threat. 

c. Evaluations - Evaluate using various metrics and see how the ML algorithms performed.

After normalising the data, I created 2 Autoencoder Models(AE2,AE3). The extracted faetures of both these models performed better than standard dimensionality techniques like PCA.

The Autoencoder extracted features from bothe AE2 and AE3 were added to the original features in seperate cases. 'Mutual Information' feature selection technique was applied on the 'Original Features + Extracted features' and the TOP 20 features were selected.

5 Machine Learning classifiers were trained iteratively on these 20 features, for instance XG Boost algorithm was trained on the TOP 1 feature. In the next iteration it was trained on the TOP 2 features and so on till the TOP 20 features

XGBoost and ADABoost proved to be the best classifiers with 97.66% and 98.14% accuracy respectively...each being trained on only 5 features. Out of these 5 features 3 were autoencoder extracted features 

Apart from Accuracy, other evaluation metrics like F-1 Score, Precision , Recall and Matthew's Corelation Coefficient were used
