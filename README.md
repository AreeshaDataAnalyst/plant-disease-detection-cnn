# plant-disease-detection-cnn
PlantGuard AI is a CNN-based plant disease detection system that classifies plant leaf images into 38 categories using TensorFlow and the PlantVillage dataset, with a Gradio interface for image predictions.
# 🌿 PlantGuard AI: Plant Disease Detection Using CNN

PlantGuard AI is a deep learning project that identifies plant diseases from leaf images using a Convolutional Neural Network (CNN). The model is trained on the PlantVillage dataset and predicts the most likely plant disease categories from an uploaded image.

The project includes image preprocessing, data augmentation, model training, performance evaluation, and an interactive web interface built with Gradio.

## 📌 Project Overview

Plant diseases can affect crop quality and agricultural productivity. Manually identifying diseases from leaf images can be time-consuming. This project explores how deep learning can help automate plant disease classification from images.

PlantGuard AI processes a plant leaf image and returns the top five predicted classes with their confidence scores.

## ✨ Features

- 🌱 Plant disease classification using a CNN.
- 🖼️ Plant leaf image preprocessing and resizing.
- 🔄 Data augmentation using random flipping, rotation, and zooming.
- 📊 Training and validation accuracy and loss visualizations.
- 🧪 Model evaluation on a separate test dataset.
- 📈 Classification report with precision, recall, and F1-score.
- 🔍 Confusion matrix for analyzing classification performance.
- 🖥️ Interactive Gradio interface for image predictions.
- 💾 Model, class labels, and evaluation results saved to files.

## 🗂️ Dataset

**Dataset:** PlantVillage Full

The project uses the PlantVillage dataset, which contains labeled plant leaf images for disease classification.

- Total images: 54,304
- Number of classes: 38
- Input: Plant leaf images
- Output: Predicted plant disease or healthy-plant category

The notebook loads the dataset using the Hugging Face Datasets library.

## 🛠️ Technologies Used

- Python
- TensorFlow and Keras
- Convolutional Neural Networks (CNN)
- Hugging Face Datasets
- NumPy and Pandas
- Matplotlib and Seaborn
- Scikit-learn
- Pillow (PIL)
- Gradio
- Google Colab / Jupyter Notebook

## ⚙️ Methodology

### 1. Dataset Loading
Load the PlantVillage dataset and retrieve the plant leaf images and their corresponding class labels.

### 2. Image Preprocessing
Convert images to RGB format, resize them to the model's input dimensions, and normalize pixel values for training and prediction.

### 3. Data Augmentation
Apply random horizontal flipping, rotation, and zooming during training to introduce image variations.

### 4. CNN Model Development
Build a CNN using convolutional layers, max-pooling layers, global average pooling, and dropout to learn visual patterns associated with different plant categories.

### 5. Model Training
Train the model using training data and monitor validation performance. Use EarlyStopping, ModelCheckpoint, and ReduceLROnPlateau callbacks to help manage training.

### 6. Model Evaluation
Evaluate the trained model on the test dataset and analyze its performance using test accuracy, loss, a classification report, and a confusion matrix.

### 7. Image Prediction
Provide an interactive Gradio interface where users can upload a plant leaf image and view the model's top five predictions.

## 🚀 Getting Started

### Option 1: Run on Google Colab

1. Download or clone this repository.
2. Open `Plant_disease_detection.ipynb` in Google Colab.
3. Run the notebook cells in order.
4. Allow the required libraries and dataset to load.
5. Train the CNN model and review the evaluation results.
6. Launch the Gradio interface to test plant leaf images.

A GPU-enabled runtime is recommended to speed up model training.

### Option 2: Run Locally

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/plant-disease-detection-cnn.git
```

Navigate to the project directory:

```bash
cd plant-disease-detection-cnn
```

Install the main dependencies:

```bash
pip install tensorflow datasets scikit-learn seaborn matplotlib pandas numpy pillow gradio
```

Launch Jupyter Notebook:

```bash
pip install notebook
jupyter notebook
```

Open `Plant_disease_detection.ipynb` and execute the cells in order.

**Note:** The notebook includes Google Colab-specific functionality. Some cells may need modification before running locally. Dataset access and package compatibility may also depend on your environment.

## 📁 Project Structure

```text
plant-disease-detection-cnn/
│
├── Plant_disease_detection.ipynb
├── README.md
├── plantguard_disease_model.keras
├── plantguard_labels.json
└── plantguard_results.json
```

The model and JSON files are generated when the corresponding notebook cells run successfully. Include them in the repository only if you want to distribute the trained model and results.

## 📊 Model Evaluation

The project evaluates its CNN model using:

- **Test Accuracy:** Overall proportion of correct test predictions.
- **Test Loss:** Model loss on the test dataset.
- **Precision:** How often predictions for a class are correct.
- **Recall:** How many actual samples of a class are identified.
- **F1-Score:** Combined measure of precision and recall.
- **Confusion Matrix:** Comparison of actual and predicted classes.

Actual performance metrics should be added here after running the notebook.

- Test Accuracy: Add your measured result.
- Test Loss: Add your measured result.

## 💾 Output Files

After successful execution, the notebook saves:

- `plantguard_disease_model.keras`: Trained CNN model.
- `plantguard_labels.json`: Class labels used for prediction.
- `plantguard_results.json`: Dataset information and evaluation metrics.

## 🌐 Gradio Interface

The Gradio interface allows users to upload a plant leaf image and view the top five predicted classes with their confidence scores.

The interface provides a simple way to experiment with the trained model without manually running prediction code.

## ⚠️ Limitations

- The model's performance depends on the quality and characteristics of the training data.
- PlantVillage images may have simpler backgrounds than images taken in real agricultural environments.
- Lighting conditions, camera quality, leaf orientation, and background clutter can affect predictions.
- A high confidence score does not guarantee a correct diagnosis.
- The model should not replace expert agricultural advice or laboratory testing.

## 🔮 Future Improvements

- Apply transfer learning using architectures such as MobileNetV2 or EfficientNet.
- Test the model on real-world plant images.
- Improve generalization under different lighting and background conditions.
- Deploy the model as a web application or mobile application.
- Add more plant species and disease categories.
- Explore model optimization for faster inference.

## 🎯 Applications

- Educational deep learning projects.
- Agricultural image classification research.
- Plant disease screening experiments.
- AI-powered agricultural assistance prototypes.

## 👨‍💻 Author

**Your Name**

GitHub: https://github.com/YOUR-USERNAME

## 📄 License

This project is intended for educational and research purposes. Add a license file if you plan to distribute the project under a specific open-source license.

## 🙌 Acknowledgments

- PlantVillage dataset contributors.
- TensorFlow and Keras teams.
- Hugging Face Datasets.
- Scikit-learn and Gradio communities.

---

**PlantGuard AI: Exploring deep learning for smarter plant disease detection.**
