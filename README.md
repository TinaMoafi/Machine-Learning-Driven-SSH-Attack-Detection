# Machine-Learning-Driven SSH Attack Detection

## Introduction

In the realm of network security, machine learning (ML) offers promising solutions for detecting and analyzing threats, particularly in the context of Secure Shell (SSH) attacks. Our project utilizes a dataset comprising approximately 230,000 unique Unix shell attacks, captured via honeypot deployments, to explore and categorize attack tactics based on the MITRE ATT&CK framework. By applying various ML techniques, we aim to automate the identification and classification of malicious activities within these SSH sessions. This project demonstrates how ML can transform complex, text-based data into actionable security insights.

## Methodology

### Data Exploration and Preprocessing
The dataset used in this project consists of SSH attack logs from honeypots, containing a wide variety of attack tactics. The data was preprocessed by:
- **Data cleaning:** Removing any irrelevant or redundant information.
- **Feature extraction:** Converting raw logs into structured features that can be used for training models.

### Machine Learning Approach
We applied both supervised and unsupervised learning techniques to classify SSH attack tactics. The supervised learning approach involved training models to predict attack types based on labeled data, while unsupervised methods were used to identify potential unknown attack strategies.

#### BERT Model for Classification
We leveraged a BERT (Bidirectional Encoder Representations from Transformers) model, which was particularly effective in processing the text-based SSH logs. The model was fine-tuned on the dataset, and its performance was evaluated based on metrics such as accuracy, F1 score, and loss.

### Training and Evaluation
The training process showed consistent improvements across epochs, with optimal performance typically achieved within 2-3 epochs. This minimized unnecessary computation and overfitting, while maintaining high model accuracy.

For instance, using the full dataset, after three epochs:
- **Training loss:** Decreased from 0.03 to 0.0125
- **Validation loss:** Reduced from 0.015 to below 0.0125
- **Validation accuracy:** Increased from 0.980 to 0.994
- **F1 score:** Stayed stable at 0.994

These metrics indicate that the model effectively learned from the data, generalized well, and minimized overfitting.

## Results

### Performance Metrics
The BERT model demonstrated significant improvement in the first two epochs, with diminishing returns in the third. The key performance indicators are summarized as follows:

- **Training loss:** Steady decrease
- **Validation loss:** Steady decrease
- **Validation accuracy:** High and stable (0.994)
- **F1 score:** Consistently high (0.994)

These results validate the effectiveness of the BERT model for classifying SSH attack sessions and highlight its potential for use in real-world security systems.

## Conclusion

This project demonstrates the potential of machine learning to automate the detection and classification of SSH attack tactics. By applying ML to analyze text-based SSH logs, we are able to identify malicious behavior, potentially improving response times and threat detection in network security systems. The use of advanced models like BERT showcases the value of deep learning in cybersecurity, especially in enhancing generalization and reducing overfitting.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Machine-Learning-Driven-SSH-Attack-Detection.git
