# Custom-Dual-Input-CNN-for-COVID-19-Classification

Feature Fusion using X-ray and CT Scan Images

📌 Objective
This project aims to design a dual-input deep learning model that leverages two separate CNNs to process X-ray and CT scan images independently. After feature extraction, the model performs feature fusion to combine insights from both imaging modalities, followed by classification into COVID or Non-COVID cases.

📂 Dataset
Dataset Name: Extensive COVID-19 X-Ray and CT Chest Images Dataset

Source: Mendeley Data

Contents:

X-ray Images (COVID & Non-COVID)

CT Scan Images (COVID & Non-COVID)

🧩 Project Structure
├── data/
│   ├── xray/
│   └── ct/
├── src/
│   ├── data_preprocessing.py
│   ├── model.py
│   ├── train.py
│   ├── evaluate.py
│   └── visualize.py
├── saved_models/
├── notebooks/
├── README.md
└── requirements.txt

🛠️ Steps Performed
1. Data Preprocessing
Loaded and preprocessed X-ray and CT images separately.

Resized images to 224×224 pixels.

Normalized pixel values to [0, 1].

Created paired datasets (X-ray + CT) for each patient.

Split dataset into train, validation, and test sets.

2. Dual CNN Implementation
Designed two separate CNNs:

CNN 1: For X-ray images

CNN 2: For CT images

Used convolutional layers, batch normalization, ReLU activation, and max-pooling layers for feature extraction.

3. Feature Fusion
Extracted feature vectors from both CNNs.

Fused them via concatenation to form a unified feature representation.

4. Fully Connected Network (FCN)
Passed the fused features through FC layers.

Applied dropout layers to reduce overfitting.

Output layer for binary classification: COVID / Non-COVID.

5. Model Training
Used Binary Cross-Entropy Loss.

Optimized with Adam / RMSprop.

Monitored training and validation performance.

6. Evaluation
Tested model on unseen data.

Computed:

Accuracy

Precision

Recall

F1-Score

Confusion Matrix

7. Visualization
Plotted training and validation loss curves.

Visualized feature maps from CNN layers to understand learned features.

🧩 Visualizations
📊 Training vs. Validation Curves

🖼️ Feature Maps from CNN layers

🧩 Confusion Matrix

🔥 Future Improvements
Experiment with advanced fusion strategies (e.g., attention mechanisms).

Use pre-trained CNN backbones for feature extraction.

Add explainability techniques like Grad-CAM.

🚀 Installation & Usage
Clone the repository:

git clone https://github.com/Hamza3087/Custom-Dual-Input-CNN-for-COVID-19-Classification.git
cd Custom-Dual-Input-CNN-for-COVID-19-Classification

Install dependencies:
pip install -r requirements.txt

Run:
jupyter notebook dual

