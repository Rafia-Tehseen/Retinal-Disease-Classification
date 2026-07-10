# Retinal Disease Classification using Deep Learning

### 📌 Project Overview
This project focuses on the automated detection and classification of retinal diseases using medical fundus imaging. It addresses both binary classification (Disease Risk vs. No Risk) and multi-class classification across 47 distinct retinal conditions. By leveraging advanced Deep Learning architectures, the project aims to assist medical professionals in early diagnosis and treatment planning.

### 📂 Dataset Information
The project uses the **Retinal Disease Classification** dataset from Kaggle, which is partitioned into Training, Evaluation, and Test sets.
*   **Total Observations:** Organized into specific directories for train, validation, and test images.
*   **Target Labels:** Provided in CSV format, including identifiers (`ID`) and diagnostic categories (`Disease_Risk`).
*   **Classes:** The dataset covers **47 different retinal disease categories**.

### ⚙️ Methodology & Preprocessing
To prepare the medical images for neural network processing, a comprehensive preprocessing pipeline was established:
*   **Standardization:** All images are resized to a uniform dimension of **224x224 pixels**.
*   **Normalization:** Pixel values are scaled between 0 and 1 to ensure faster model convergence.
*   **Image Augmentation:** To improve model generalization and prevent overfitting, the `ImageDataGenerator` applies several real-time transformations:
    *   Rotation (20°)
    *   Width and Height Shifts (0.2)
    *   Shear and Zoom Transformations (0.2)
    *   Horizontal Flipping

### 🤖 Model Architectures
The project implements and compares several state-of-the-art Deep Learning strategies:

#### 1. Custom Sequential CNN
A custom-built Convolutional Neural Network designed for medical image feature extraction:
*   **Three Convolutional Blocks:** Using 32, 64, and 128 filters with ReLU activation.
*   **Pooling:** Max-pooling layers to reduce spatial dimensions.
*   **Dense Layers:** A fully connected layer with 512 units followed by **Dropout (0.5)** for regularization.
*   **Output Layer:** Sigmoid activation for binary classification or Softmax for multi-class tasks.

#### 2. Transfer Learning (Pre-trained Models)
Leveraging models pre-trained on the ImageNet dataset with a custom head for retinal classification:
*   **ResNet50**
*   **InceptionV3**
*   **MobileNetV2**

### 📊 Performance & Findings
*   **Optimizers:** All models were trained using the **Adam optimizer** with a binary/sparse categorical cross-entropy loss function.
*   **Training Results:** Pre-trained models showed strong performance. For instance, **InceptionV3** and **MobileNetV2** achieved a validation accuracy of approximately **79.06%** during training.
*   **Evaluation:** Models are evaluated using **Accuracy Scores**, **Classification Reports** (Precision, Recall, F1-Score), and **Confusion Matrices**.

### 📈 Visualizations
To provide a clear understanding of model performance, the following visualizations are included in the analysis:
*   **Disease Distribution Chart:** A bar graph showing the prevalence of different conditions in the dataset.
*   **Training History Plots:** Graphs depicting Accuracy and Loss trends for both training and validation sets over 20-50 epochs.
*   **Confusion Matrix:** A heatmap highlighting the classification performance across different disease categories.
*   **Sample Predictions:** A visual grid displaying retinal fundus images with their True and Predicted labels.

### 🛠️ Technologies Used
*   **Languages:** Python
*   **Deep Learning:** TensorFlow, Keras
*   **Data Analysis:** Pandas, NumPy
*   **Visualization:** Matplotlib, Seaborn, Plotly (Express & Graph Objects)
*   **Computer Vision:** OpenCV (`cv2`)
*   **Evaluation:** Scikit-learn

### 👨‍💻 Author
**[Rafia Tehseen]**
