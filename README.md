# Retinal Disease Classification using Deep Learning

### 📌 Project Overview
This project focuses on the automated detection and classification of retinal diseases using medical fundus imaging. It addresses both binary classification (Disease Risk vs. No Risk) and multi-class classification across 47 distinct retinal conditions. By leveraging advanced Deep Learning architectures and image augmentation, the project aims to provide a robust tool for early diagnostic support.

### 📂 Dataset Information
The project utilizes the **Retinal Disease Classification** dataset from Kaggle, partitioned into Training, Evaluation, and Test sets.
*   **Target Labels:** Provided in CSV format, including identifiers (`ID`) and diagnostic categories (`Disease_Risk`).
*   **Classes:** The dataset covers **47 different retinal disease categories**.

### ⚙️ Methodology & Preprocessing
To optimize image data for neural network training, a comprehensive preprocessing pipeline was established:
*   **Standardization:** All images are resized to a uniform dimension of **224x224 pixels**.
*   **Normalization:** Pixel values are scaled to a range of by dividing by 255.0.
*   **Image Augmentation:** To improve generalization and prevent overfitting, the `ImageDataGenerator` applies real-time transformations:
    *   **Rotation:** 20°
    *   **Width/Height Shifts:** 0.2
    *   **Shear/Zoom:** 0.2
    *   **Horizontal Flipping:** Enabled
    *   **Fill Mode:** Nearest

### 🤖 Model Architectures
The project evaluates several Deep Learning strategies:
1.  **Custom Sequential CNN:** Features three convolutional blocks (32, 64, and 128 filters) with ReLU activation, max-pooling, and a dense layer with **Dropout (0.5)** for binary risk classification.
2.  **Transfer Learning:** Utilizes pre-trained bases from **ResNet50**, **InceptionV3**, and **MobileNetV2** with custom global average pooling and dense output layers.

### 📊 Key Findings & Accuracies
The following results were observed during the experimental phases:

*   **Initial Transfer Learning Performance:** During 20-epoch training cycles, both **InceptionV3** and **MobileNetV2** models achieved a stable validation accuracy of approximately **79.06%**.
*   **Extended Training Optimization:** By extending training to **50 epochs** and utilizing the augmented dataset, the model demonstrated significant improvement, reaching a peak validation accuracy of **82.19%**.
*   **Model Stability:** The training logs indicate consistent convergence between training and validation loss, suggesting that the combination of dropout and image augmentation successfully mitigated overfitting.

### 📈 Visualizations
To evaluate model performance, the following visual metrics are included:
*   **Disease Distribution:** A bar chart visualizing the frequency of different conditions in the training set.
*   **Training History Plots:** Real-time graphs for **Model Accuracy** and **Model Loss** across all epochs.
*   **Confusion Matrix:** A detailed heatmap highlighting the model's precision in classifying the 47 disease categories.
*   **Sample Predictions:** A grid showing actual retinal scans with their **True vs. Predicted** labels for qualitative assessment.

### 🛠️ Technologies Used
*   **Languages:** Python
*   **Deep Learning:** TensorFlow, Keras
*   **Data Analysis:** Pandas, NumPy
*   **Visualization:** Matplotlib, Seaborn, Plotly (Express & Graph Objects)
*   **Computer Vision:** OpenCV (`cv2`)
*   **Evaluation:** Scikit-learn (Classification Report, Confusion Matrix, Accuracy Score)

### 👨‍💻 Author
**[Rafia Tehseen]**
