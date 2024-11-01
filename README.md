# Parkinsons-Disease-Detection-using-Inception-and-Xception-with-Attention-Mechanism.ipynb
The project uses InceptionV3 and Xception models with attention mechanisms to detect Parkinson’s disease from spiral drawings. Images are labeled as "healthy" or "parkinson," preprocessed, and split for training with early stopping. High validation accuracy and strong classification metrics validate model effectiveness.



**Parkinson's Disease Detection Using Inception and Xception with Attention Mechanism**

**Overview:**  
This project explores a cutting-edge approach to detecting Parkinson’s disease using deep learning models, specifically InceptionV3 and Xception, with the integration of attention mechanisms. It utilizes the unique patterns found in spiral drawings created by individuals, which are known to reflect motor control, a significant marker for Parkinson’s.

**Data Collection and Preparation:**  
- **Dataset:** Spiral drawing images are collected and labeled as "healthy" or "parkinson."
- **Preprocessing:** Images are resized to 224x224 pixels, normalized, and stratified into training, validation, and test sets to balance the class distribution.
- **Image Augmentation:** Techniques like rescaling and random flipping are applied to enhance model robustness.

**Model Architecture:**  
1. **Base Models (InceptionV3 & Xception):** Pre-trained on ImageNet, these models capture complex spatial features. For this task, the top layers are removed, and the remaining layers are frozen to retain previously learned features.
2. **Attention Mechanism:** Multi-Head Attention is applied to help the model focus on critical parts of the images, enabling it to distinguish subtle patterns indicative of Parkinson's.
3. **Additional Layers:** After attention, layers like Gaussian Noise, GlobalAveragePooling2D, Dense, BatchNormalization, and Dropout are added for regularization and to reduce overfitting.

**Training and Optimization:**  
- **Early Stopping:** Monitors validation loss, stopping training if performance ceases to improve, saving resources and preventing overfitting.
- **Optimizer:** Adam optimizer with a learning rate of 0.0001 is used for efficient and stable learning.
- **Loss Function:** Binary cross-entropy for binary classification.

**Performance Evaluation:**  
- **Metrics:** Precision, recall, F1-score, and confusion matrix are used to assess the model.
- **Validation Accuracy:** Both models reached high accuracy levels, confirming their capability in distinguishing between healthy and Parkinson's samples.
- **Comparative Analysis:** A comparative bar chart displays InceptionV3 and Xception’s performance across metrics, showing how each model responds to attention integration.

**Results and Findings:**  
- **Accuracy and Reliability:** The models demonstrate impressive classification performance with high precision, recall, and F1-scores, ensuring accurate disease detection.
- **Attention Enhancement:** The attention mechanism significantly improves model focus on crucial image regions, enhancing diagnostic accuracy.

**Conclusion:**  
This innovative approach leverages advanced deep learning models and attention mechanisms, providing a reliable, non-invasive diagnostic tool for Parkinson’s. The integration of visual attention highlights the potential of AI in medical diagnostics, setting the stage for further applications in neurology and beyond.
