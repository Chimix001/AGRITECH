# 🍅 TomatoGuard – AI-Powered Tomato Leaf Disease Detection

TomatoGuard is an AI-powered agricultural disease detection system that uses Deep Learning and Computer Vision to identify diseases in tomato plants from leaf images.

The system allows users to capture or upload an image of a tomato leaf and uses a trained Convolutional Neural Network (CNN) to classify it as either healthy or affected by Tomato Leaf Mold.

The goal is to explore how Artificial Intelligence can support farmers in identifying plant diseases early and making more informed agricultural decisions.

## 🎯 Project Objectives

- Develop a Deep Learning model for tomato leaf disease detection.
- Apply Computer Vision techniques to analyze tomato leaf images.
- Identify healthy tomato leaves and leaves affected by Leaf Mold.
- Explore how AI-powered disease detection can improve agricultural practices.
- Establish a foundation for a more comprehensive AI-powered agricultural assistant.

## 🧠 Model Architecture

The project uses a custom-built Convolutional Neural Network (CNN) developed with TensorFlow and Keras.

The model architecture consists of:

1. Image resizing and normalization.
2. Data augmentation.
3. Five convolutional layers with ReLU activation.
4. Max pooling layers for dimensionality reduction.
5. Fully connected dense layers.
6. Dropout layers to reduce overfitting.
7. A Softmax output layer for classification.

### Model Configuration

| Parameter | Value |
|---|---|
| Framework | TensorFlow / Keras |
| Architecture | Custom CNN |
| Image dimensions | 256 × 256 |
| Color channels | 3 (RGB) |
| Batch size | 32 |
| Maximum epochs | 50 |
| Optimizer | Adam |
| Learning rate | 0.001 |
| Loss function | Sparse Categorical Crossentropy |
| Regularization | Dropout |
| Early stopping | Enabled |

## 📊 Dataset

The model was trained using a dataset containing 2,543 tomato leaf images across two classes.

| Class | Number of Images |
|---|---:|
| Tomato Leaf Mold | 952 |
| Tomato Healthy | 1,591 |
| **Total** | **2,543** |

### Supported Classes

- `Tomato_Leaf_Mold`: Identifies tomato leaves affected by Leaf Mold.
- `Tomato_healthy`: Identifies healthy tomato leaves.

The dataset was divided into training, validation and testing subsets using an 80:10:10 batch-based split.

## ⚙️ Data Preprocessing

The following preprocessing techniques were implemented:

- Resizing images to 256 × 256 pixels.
- Normalizing pixel values to the range [0, 1].
- Random horizontal and vertical flipping.
- Random rotation.
- Random zoom.
- Random contrast adjustment.
- Class weighting to address class imbalance.

Data augmentation was incorporated into the model so that it is applied during training rather than validation or testing.

## 📈 Model Performance

The model was evaluated on a held-out test dataset.

**Test Accuracy: 96.23%**

### Classification Report

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Tomato Leaf Mold | 0.99 | 0.91 | 0.95 |
| Tomato Healthy | 0.95 | 0.99 | 0.97 |
| **Overall Accuracy** | | | **0.96** |

Additional evaluation techniques included:

- Confusion matrix.
- Classification report.
- Training and validation accuracy curves.
- Training and validation loss curves.
- Prediction confidence scores.

The model achieved a test accuracy of 96.23% on the evaluated test split. Performance on images captured in real farming environments still needs to be independently validated.

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/TomatoGuard.git
cd TomatoGuard
```

### 2. Install dependencies

```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn
```

### 3. Prepare the dataset

Organize the dataset into the following directory structure:

```text
Tomato/
├── Tomato_Leaf_Mold/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
└── Tomato_healthy/
    ├── image1.jpg
    ├── image2.jpg
    └── ...
```

Update the dataset path in the notebook to point to your dataset directory.

### 4. Run the notebook

Open the notebook in Google Colab or Jupyter Notebook and execute the cells to:

- Load and explore the dataset.
- Preprocess the images.
- Build and train the CNN.
- Evaluate model performance.
- Generate predictions.
- Save the trained model.

## 💾 Model Export

The trained model is saved in Keras format:

```python
model.save("tomato_disease_model.keras")
```

The exported model can subsequently be integrated into an API or application for image-based disease detection.

## 🔮 Future Improvements

Planned improvements include:

- Support for additional tomato diseases.
- Transfer learning using architectures such as MobileNetV2 and EfficientNet.
- Real-time image-based disease detection.
- Grad-CAM visualizations to explain model predictions.
- FastAPI backend for model inference.
- Mobile-friendly interface for farmers.
- Disease management and treatment recommendations.
- Support for additional crops.

## ⚠️ Limitations

The current model supports only two classes: Tomato Leaf Mold and Tomato Healthy.

It should not be interpreted as a comprehensive tomato disease diagnostic system. Other diseases, pests, nutrient deficiencies and environmental conditions are outside its current classification scope.

Predictions should be treated as preliminary indicators rather than definitive agricultural diagnoses.

## 🤝 Contributions

Contributions, suggestions and improvements are welcome.

Feel free to fork the repository, open an issue or submit a pull request.

## 📄 License

A license will be added to the repository when the project license is determined.
