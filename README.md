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

