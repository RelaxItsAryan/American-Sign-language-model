# 🤟 ASL Alphabet Recognition using Deep Learning

A deep learning-based American Sign Language (ASL) Alphabet Recognition system built with **PyTorch**, **OpenCV**, and **Kaggle's ASL Alphabet Dataset**. The model classifies hand-sign images representing the 26 English alphabet letters (A–Z).

---

## 📌 Overview

This project trains a neural network to recognize American Sign Language alphabet gestures from images.

The workflow includes:

- Downloading the ASL Alphabet Dataset
- Image preprocessing and normalization
- Dataset creation and train-test splitting
- Training a deep neural network using PyTorch
- Evaluating performance using accuracy, confusion matrix, and classification reports
- Predicting letters from custom images
- Saving the trained model for future use

---

## 🚀 Features

✅ Recognizes all 26 ASL alphabet letters (A–Z)

✅ Image preprocessing and normalization

✅ Fully connected neural network classifier

✅ Training and validation accuracy tracking

✅ Confusion matrix visualization

✅ Classification report generation

✅ Single-image prediction support

✅ Model checkpoint saving

---

## 🛠️ Tech Stack

- Python
- PyTorch
- OpenCV
- NumPy
- Scikit-Learn
- Matplotlib
- KaggleHub
- TQDM

---

## 📂 Dataset

Dataset used:

- ASL Alphabet Dataset from Kaggle

The dataset contains hand-sign images for all 26 English alphabet letters.

Example classes:

```text
A
B
C
D
...
X
Y
Z
```

---

## 🧠 Model Architecture

```text
Input Layer (64×64×3 = 12,288 features)
        ↓
Linear (12288 → 512)
        ↓
ReLU
        ↓
Dropout (0.4)
        ↓
Linear (512 → 256)
        ↓
ReLU
        ↓
Dropout (0.3)
        ↓
Linear (256 → 26)
        ↓
Softmax (Prediction)
```

---

## 📊 Training Configuration

| Parameter | Value |
|------------|--------|
| Epochs | 30 |
| Batch Size | 64 |
| Learning Rate | 0.001 |
| Optimizer | Adam |
| Loss Function | CrossEntropyLoss |
| Validation Split | 20% |

---

## 📥 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/asl-recognition.git
cd asl-recognition
```

Install dependencies:

```bash
pip install torch torchvision
pip install opencv-python
pip install numpy
pip install matplotlib
pip install scikit-learn
pip install kagglehub
pip install tqdm
```

---

## ▶️ Running the Project

### 1. Download Dataset

The notebook automatically downloads the dataset:

```python
path = kagglehub.dataset_download(
    "grassknoted/asl-alphabet"
)
```

### 2. Build Dataset

Images are:

- Resized to 64×64
- Flattened into feature vectors
- Normalized to range [0,1]

### 3. Train Model

Run all notebook cells sequentially.

The model will:

- Train for 30 epochs
- Save the best-performing weights
- Display training and validation accuracy

### 4. Evaluate

The notebook generates:

- Accuracy plots
- Confusion Matrix
- Classification Report

### 5. Test Custom Images

```python
predict_image("sample.jpg")
```

Example output:

```text
🏆 Predicted letter: A

A     ██████████████████ 95.3%
H     █                  2.1%
R     █                  1.3%
```

---

## 💾 Saving the Model

The trained model is saved as:

```text
asl_final_model.pth
```

Saved metadata includes:

```python
{
    "model_state",
    "label_map",
    "num_classes",
    "input_size"
}
```

---

## 📈 Results

The model successfully learns ASL alphabet gestures and achieves high classification performance on the validation dataset.

Evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## 📁 Project Structure

```text
ASL-Recognition/
│
├── ASL_complete_v2.ipynb
├── asl_final_model.pth
├── README.md
│
├── Dataset/
│   ├── A/
│   ├── B/
│   ├── C/
│   └── ...
│
└── Outputs/
    ├── Training Curves
    ├── Confusion Matrix
    └── Predictions
```

---

## 🔮 Future Improvements

- Real-time webcam prediction
- CNN-based architecture for higher accuracy
- Transfer Learning using ResNet/EfficientNet
- Hand landmark detection using MediaPipe
- Sentence-level sign language recognition
- Deployment as a web application using Flask or Streamlit

---

## 👨‍💻 Author

**Aryan**

Built as a deep learning project for recognizing American Sign Language (ASL) alphabet gestures using PyTorch.

---

## 📜 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it for educational and research purposes.
