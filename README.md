# mia_testing

# ROC_AUC_AV.ipynb

Overview
The code defines a customizable CNN (small_cnn) for image classification, trains it on CIFAR-10, and evaluates its performance using ROC curves and Attacker Advantage. This serves as a proof-of-concept for building lightweight, privacy-aware ML models—potentially integrable into a server or privacy auditing tool.

Dataset: CIFAR-10 (10 classes, 50,000 training images, 10,000 test images).
Model: Configurable CNN with variable convolutional layers.
Evaluation: ROC curves and Attacker Advantage per class.
Features
Modular CNN: Adjust number of conv layers, activation functions, and learning rate.
CIFAR-10 Preprocessing: Normalizes images and one-hot encodes labels.
Training: Supports batch processing and validation with TensorFlow.
Privacy Metrics: Computes ROC curves and Attacker Advantage to hint at membership inference risks.
Visualization: Plots multi-class ROC curves with AUC and AA annotations.

# tensorflow_privacy_membership_inference_attacks.ipynb
Overview
This codebase builds a CNN for CIFAR-10 image classification and assesses its privacy risks via membership inference attacks. The model intentionally lacks regularization to highlight overfitting, making it a candidate for privacy analysis. It’s a proof-of-concept for understanding ML model vulnerabilities—potentially part of a broader privacy auditing tool.

Dataset: CIFAR-10 (10 classes, 50,000 training images, 10,000 test images).
Model: Simple 3-layer CNN with no dropout or regularization.
Privacy Analysis: Uses TensorFlow Privacy to run Threshold and Logistic Regression attacks.
Features
CIFAR-10 Loader: Preprocesses data with normalization and label flattening.
Simple CNN: 3 convolutional layers with ReLU, max pooling, and dense layers.
Training: 30 epochs with Adam optimizer and sparse categorical cross-entropy.
MIA: Computes logits, probabilities, losses, and runs attacks with slicing by class and correctness.
Visualization: Plots training/validation accuracy and ROC curves for attack performance.
