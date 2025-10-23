# 🎵 Deep Learning Music Genre Classification (MGC)

This project is a complete system for automatically identifying the **genre of a music clip** using a **Deep Learning model**.  
It transforms raw audio into a visual representation (**Mel Spectrogram**), uses a **Convolutional Neural Network (CNN)** to analyze it, and provides the result through a simple **web application** (Streamlit).

---
This folder contains the model files **you trained during this project** (not an externally pretrained model):  
➡️ **[Drive folder — model & artifacts](https://drive.google.com/drive/u/0/folders/1RtIEAfXU6dQxd9kbLCTaaSqbpXqetO0N)**

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
The trained model outputs a predicted genre which the Streamlit web app displays to the user.

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

## ⚙️ Environment Setup & Installation

### 1. Clone the repository
```bash
git clone <repository_url>
cd <repository_directory>
```

### 2. Activate Environment
(Using a separate environment manager like Conda is highly recommended.)

```bash
Copy code
conda create -n genre_classifier python=3.x
conda activate genre_classifier
```

### 3. Install Dependencies
```bash
Copy code
pip install -r requirement.txt
```

## ▶️ Deployment & Execution
The application is packaged as a single Streamlit script.

Run the application:

```bash
Copy code
streamlit run Music_Genre_App.py
Note: Ensure the pre-trained model weights (saved .h5 file) are present in the expected path before running the app.
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

Streamlit — app deployment
