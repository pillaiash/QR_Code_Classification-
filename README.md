# QR Code Classification System: First Print vs Second Print

## Overview

This project implements a machine learning-based system to classify QR code images as either **"first print" (original)** or **"second print" (counterfeit)**. The system utilizes both traditional machine learning models and deep learning approaches to detect subtle differences in print quality and microscopic patterns that distinguish originals from counterfeits.

## Dataset Description

The dataset contains 200 QR code images, equally divided into two classes:
- **First Print (Original)**: 100 images of original QR codes with embedded copy detection patterns.
- **Second Print (Counterfeit)**: 100 images of counterfeit versions created by scanning and reprinting original codes.

## Approach

1. **Data Exploration and Analysis**: Identified key differences between first and second prints.
2. **Feature Engineering**: Utilized texture-based features (GLCM) to capture print artifacts and degradation.
3. **Model Development**:
   - Random Forest (RF) using GLCM-based features.
   - Convolutional Neural Network (CNN) trained on augmented image data.
4. **Model Training**: Optimized the models using hyperparameter tuning and cross-validation.
5. **Model Evaluation**: Assessed models based on accuracy, precision, recall, and F1-score.

## Model Performance

- **Random Forest**: Accuracy = 95%
- **CNN**: Accuracy = 96%

## Deployment

- **Dockerized Application** for easy deployment.
- **Flask API** for real-time QR code classification.
- **Edge Deployment** using TensorFlow Lite for offline scanning.

## Future Improvements

- Hybrid model combining CNN and RF predictions.
- Transfer learning with pre-trained CNN models.
- Implement explainability techniques (e.g., SHAP, LIME).

## License

MIT License. You are free to modify and distribute the code with proper attribution.

## Contact

For questions, contact:  
Aishwarya  
Email: your-email@example.com
