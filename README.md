# Tennessee Eastman Process Dataset Analysis and Anomaly Detection

This repository contains the implementation of machine learning models including Random Forest and Bi-directional LSTM (Long Short-Term Memory) followed by an ANN neural classifier. The objective of the repository is to achieve anomaly detection as early as possible and then classify them into the fault type for post analysis of faults in industries.

## Introduction

Usual alarm systems in industries are mechanized to work on pre-set threshold values for different kinds of control variables like pressure, flow rate, etc. These alarm systems miss out anamolies that are captured by combination of disturbances in more than one control variables. 

The Tennessee Eastman Process dataset is a widely used benchmark dataset in the field of process monitoring and fault detection. It simulates a chemical process with various operating conditions and potential faults. The goal of this project is to develop machine learning models to detect anomalies as early as possible and classify the fault type in the process.

## Dataset

The Tennessee Eastman Process dataset is available [here](link-to-dataset). It contains measurements from various sensors in the chemical process under different operating conditions and fault scenarios.

## Usage

1. Clone the repository:
git clone https://github.com/your-username/tennessee-eastman-process.git

2. Install the required dependencies:
pip install -r requirements.txt

3. EDA has been performed separately in the notebook named "[EDA.ipynb](https://github.com/bns1808/MECE788Group1/blob/main/main/EDA.ipynb)", located in the main folder of the repo

4. Execute the Jupyter notebook named "RF and LSTM Combined - TK.ipynb" to train and evaluate the models:
For each session, the data is imported from google drive, stored into corresponding variables and then the files are temporarily deleted from the directory.

Our intital dataset has some instances for each fault type, where the classes are mislabelled. So next part of the code deals with labels and adds a column named "faultOccurence", that sets normal mode as '0', whereas all other fault types as '1'. This 

With analysis from the EDA, it is followed by data pre-processing. This deals with capturing the temporal nature of the dataset by introducing the rolling window and taking lagged intervals as new features.

A pipeline is defined, that has a standardsclaer transformer, succeeded by the Random Forest binary classifier.



## Results

Random Forest achieved an accuracy of X% on the test set.
LSTM achieved an accuracy of Y% on the test set.
Autoencoder achieved an accuracy of Z% on the test set.

## Conclusion

In this project, we explored the application of Random Forest, LSTM, and Autoencoder for anomaly detection on the Tennessee Eastman Process dataset. Each model demonstrated varying degrees of success in detecting anomalies. Further experimentation and fine-tuning may be required to improve the performance of these models.

## References

Tennessee Eastman Process dataset: link
Example reference 1
Example reference 2

## Contributors

Your Name - @your-username
Contributor 2 - @contributor-2-username