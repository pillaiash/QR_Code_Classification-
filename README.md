#QR Code Classification System:
Overview
This project implements a machine learning-based system to classify QR code images as either "first print" (original) or "second print" (counterfeit). The system leverages both traditional machine learning models and deep learning approaches to identify subtle differences in print quality and microscopic patterns that distinguish originals from counterfeits.

Dataset Description
The dataset contains 200 QR code images, divided equally into two classes:

First Print (Original): 100 images of original QR codes with embedded copy detection patterns.

Second Print (Counterfeit): 100 images of counterfeit versions created by scanning and reprinting original codes.

Each image exhibits subtle differences due to print quality degradation and reprinting artifacts, which were analyzed and extracted as features for classification.

Project Workflow
1. Data Exploration and Analysis
Visual inspection was performed to identify key differences between first and second prints.

Statistical summaries and feature distributions were analyzed.

Relevant features such as texture, pattern quality, and resolution differences were extracted.

2. Feature Engineering
GLCM (Gray-Level Co-occurrence Matrix): Used to extract texture-based features.

Additional features focused on capturing print artifacts, degradation patterns, and local variations in QR code quality.

3. Model Development
Random Forest (RF): A traditional machine learning approach leveraging GLCM-based features.

Convolutional Neural Network (CNN): A deep learning model trained on augmented image data to capture intricate patterns.

4. Model Training and Validation
RF was optimized using hyperparameter tuning for best performance.

CNN architecture was fine-tuned with dropout and batch normalization to prevent overfitting.

Models were validated using a 5-fold cross-validation strategy.

5. Model Evaluation
Models were evaluated using key metrics:

Accuracy

Precision

Recall

F1-Score

Confusion matrices were generated to analyze misclassifications and identify challenging cases.

6. Deployment Considerations
Models were optimized using quantization and pruning techniques.

The system was containerized using Docker and deployed using Flask APIs.

Edge-based deployment was implemented for offline scanning scenarios.
