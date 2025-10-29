# 🎵 Deep Learning Music Genre Classification 

This project is a complete system for automatically identifying the **genre of a music clip** using a **Deep Learning model**.  
It transforms raw audio into a visual representation (**Mel Spectrogram**), uses a **Convolutional Neural Network (CNN)** to analyze it.

---

## 💡 How the Project Works (The Classification Flow)

The system processes music in **four logical stages**:

### 1. Step 1 — Raw Audio Input
The process begins with an audio file (like **MP3** or **WAV**).  
The user uploads this file through the web application.

### 2. Step 2 — Creating the *“Picture of Audio”* (Feature Extraction)
A raw audio signal is too complex for a standard deep learning model. We use **librosa** to perform audio analysis and convert the signal into a **Mel Spectrogram**.

> **What is a Mel Spectrogram?**  
> A Mel Spectrogram is a **2D image-like representation** of the audio’s frequencies over time. It’s like a picture of the sound and works well with CNNs.

### 3. Step 3 — The Deep Learning Classifier (CNN)
The spectrogram image is fed into a CNN (built in **TensorFlow / Keras**) which learns patterns that correspond to genres.  
Training setup highlights:
- Optimizer: **Adam**
- Loss: **Categorical Cross-Entropy**

### 4. Step 4 — Genre Prediction and Web App
The trained model outputs a predicted genre.

---

## 🛠️ Technical Requirements & Setup

### 📦 Dependency Manifest

| Package       | Version (recommended) | Purpose                              |
|---------------|------------------------|--------------------------------------|
| `tensorflow`  | 2.10.0                 | Deep Learning Core (Model)           |
| `librosa`     | 0.10.1                 | Audio Analysis / Feature Extraction  |
| `numpy`       | 1.24.3                 | Numerical Operations                 |
| `streamlit`   | latest                 | Web app / Deployment                 |

---




```
```

## 📈 Contextual Performance
Using Mel Spectrograms + CNN is a proven approach for music classification.

## 📊 Results

The model was evaluated on both the training and test sets. Key evaluation scores:

| Dataset         | Accuracy (or Evaluation Metric) |
|-----------------|---------------------------------:|
| Training set    | 0.9922370910644531              |
| Test set        | 0.903171956539154               |



## 🌟 Acknowledgements
Librosa — audio processing

TensorFlow / Keras — deep learning
