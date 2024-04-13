

# Early Process Fault Diagnosis

**Model ID**: Tennessee-Eastman-Fault-Detection

**Summary**: This model leverages a combination of RandomForestClassifier and LSTM networks to monitor and classify faults in real time using the Tennessee Eastman Process Simulation Dataset. Initially, it detects the occurrence of a fault, then identifies the specific class of the fault for targeted interventions.

# Table of Contents

- [Model Details](#model-details)
- [Intended Use](#intended-use)
- [Training and Evaluation](#training)
- [Ethical Considerations](#ethical-considerations)
- [Limitations and Recommendations](#limitations-and-recommendations)
- [Additional Information](#maintenance)


## Model Details

- **Model Name**: Tennessee Eastman Fault Detection Model
- **Model Version**: 1.0
- **Model Type**: Hybrid (RandomForest for fault detection, LSTM for fault classification)
- **Developers**: MECE788Group1
- **Release Date**: April 13, 2024

## Intended Use

- **Primary Use**: This model is primarily developed for real-time monitoring and fault detection in the Tennessee Eastman chemical process. It aims to identify when a fault occurs and classifies the type of fault to enable timely corrective actions.
- **Intended Users**: The model is intended for chemical process engineers, operational staff, and safety personnel who manage and maintain the Tennessee Eastman process. It aids in enhancing operational safety and efficiency by providing early fault detection.
- **Out-of-Scope Use Cases**: This model is not designed for use in non-industrial contexts, such as healthcare monitoring, financial forecasting, or consumer behavior prediction. Additionally, it should not be employed in chemical processes significantly different from the Tennessee Eastman setup, as the model's accuracy and reliability are specific to the data and scenarios it was trained on.


## Training and Evaluation

### Training Procedure
The model was trained using the Tennessee Eastman Process Simulation Dataset. The RandomForest classifier was first trained to detect the occurrence of faults in real-time. Training parameters included a maximum depth of 40, 200 estimators, and a random state for reproducibility. The LSTM network was subsequently trained to classify the type of fault based on sequences of process data, using a learning rate of 0.001 and 200 epochs.

### Evaluation Metrics
The model's performance was evaluated using precision and F1 score for the RandomForest classifier, and loss for the LSTM. The RandomForest achieved an accuracy of 80% and an F1 score of __, while the LSTM reached a categorical accuracy of __ with a loss of __ on the test dataset.

### Baseline Comparison
Compared to a baseline SVM classifier that achieved an 85% accuracy and an F1 score of 0.82, the RandomForest classifier shows significant improvement in both accuracy and precision. The LSTM's ability to classify fault types surpasses that of a traditional RNN, which achieved a categorical accuracy of 90%.



## Ethical Considerations

### Fairness and Bias
The model utilizes the Tennessee Eastman Process Simulation Dataset, which is synthetic and designed to simulate typical process faults. Given the synthetic nature of the data, traditional biases related to human factors are not present. However, we continuously evaluate the model’s decision-making process to ensure no algorithmic biases are introduced during development. Techniques such as feature importance analysis are used to monitor any potential biases.

### Privacy
Since the dataset is synthetic and does not contain any real personal or sensitive data, privacy concerns related to personal data are inherently mitigated. Our model does not require or process any real-world personal information, aligning with privacy best practices.

### Security



## Limitations and Recommendations

### Known Limitations
- **Data Specificity**: While the model is trained on the Tennessee Eastman Process Simulation Dataset, its ability to generalize to real-world industrial environments with different operational parameters may be limited. Users should validate the model’s performance with pilot tests before full-scale deployment.
- **Performance Variability**: The model's performance may degrade under conditions not represented in the training data, such as novel fault types or unexpected operational scenarios.
- **Scalability Issues**: The current implementation may require adjustments to scale up to larger, more complex industrial systems or to integrate with different types of process control equipment.

### Recommendations for Use
- **Validation Before Deployment**: It is recommended that users conduct thorough validation of the model using their own specific datasets to ensure it performs as expected in their operational context.
- **Continuous Monitoring and Updating**: Users should continuously monitor the model’s performance over time and consider retraining with new data to adapt to changes in the operational environment.
- **Ethical Use**: Ensure that the model’s use complies with local regulations and ethical standards, particularly in making decisions that could affect the safety and reliability of industrial processes.



## Additional Information

### References
- "Introduction to the Tennessee Eastman Process Simulation Dataset", [Link to the dataset description and download](URL_to_dataset).

### License
This model is released under the MIT License, which permits use, modification, distribution, and private use. This license is permissive and allows for commercial use, but it does not provide any warranty.

### Contact Information
- **Lead Developers**: Madhura, Mansimran, Thomas, Yarooj 
- **Email**: [johndoe@example.com](mailto:johndoe@example.com)
- **GitHub**: [johndoe](https://github.com/johndoe)
