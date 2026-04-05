# 🧠 Deepfake Voice Detection using LCNN

**Author:** Rabia Buse Menteş

---

## 📌 Overview

This project presents a **deepfake voice detection system** based on a Light Convolutional Neural Network (LCNN) using **log-Mel spectrogram features**.

With the rapid advancement of AI-generated speech (TTS & voice conversion), detecting spoofed audio has become critical for preventing **voice phishing (vishing)** and identity fraud.

This system is designed to:

* Detect synthetic (spoofed) speech
* Evaluate performance across different environments
* Analyze **real-world generalization challenges**

---

## ⚙️ Methodology

### 🔊 Feature Extraction

* Log-Mel Spectrograms (Librosa)
* Sampling rate: **16 kHz**
* 80 Mel bands
* FFT size: 1024, Hop length: 256
* Fixed input size: **(1, 80, 300)**

---

### 🧠 Model Architecture

* **LCNN (Light CNN)**
* Max-Feature-Map (MFM) activation
* Convolution + pooling layers
* Fully connected classifier (Bonafide vs Spoof)

---

### 📊 Training

* Optimizer: Adam
* Learning rate: 1e-4
* Loss: CrossEntropyLoss
* Trained on NVIDIA T4 GPU

---

### 📈 Evaluation Metrics

* Accuracy
* Equal Error Rate (EER) *(main metric)*
* ROC & DET curves

---

## 🧪 Datasets

### 📂 ASVspoof2019

* **LA (Logical Access):** synthetic TTS/VC (clean)
* **PA (Physical Access):** replay attacks (noisy, real-world)

### 📂 Custom Dataset

* Turkish speech recordings
* 164 real / 151 fake samples
* Fake audio generated with AI tools (e.g., ElevenLabs)
* Includes **language mismatch + real-world variability**

---

## 📊 Results

| Scenario                 | EER (%)   |
| ------------------------ | --------- |
| LA                       | **1.41**  |
| PA                       | **8.79**  |
| PA → Custom              | **18.76** |
| LA → Custom (fine-tuned) | **10.53** |

### 🔍 Key Observations

* Excellent performance on **LA (clean synthetic data)**
* Performance drops on **PA due to real-world distortions**
* Significant degradation in **cross-dataset evaluation**
* Fine-tuning improves generalization

---

## 📉 Insights

* Deep learning models perform well in **controlled environments**
* Real-world conditions introduce:

  * Noise
  * Language differences
  * Recording variability
* **Domain mismatch** is a major challenge in deepfake detection

---

## 🛠️ Tech Stack

* Python
* PyTorch
* Librosa
* NumPy
* Scikit-learn
* Matplotlib

---

## 📂 Project Structure

```
deepfake-voice-detection/
│
├── notebooks/
│   ├── 01_LA_baseline.ipynb
│   ├── 02_PA_baseline.ipynb
│   ├── 03_LA_custom_dataset.ipynb
│   ├── 04_PA_custom_dataset.ipynb
│
├── src/
├── results/
├── assets/
└── README.md
```

---

## 🚀 How to Run

```
git clone https://github.com/yourusername/deepfake-voice-detection.git
cd deepfake-voice-detection
pip install -r requirements.txt
```

Run notebooks or training scripts.

---

## 📁 Dataset

Datasets are not included due to size.

Download:
👉 https://www.asvspoof.org/

---

## 🔑 Contributions

* LCNN-based deepfake detection system
* Evaluation on **LA & PA datasets**
* Cross-dataset generalization analysis
* Custom dataset (Turkish, real-world conditions)
* Noise robustness analysis
* Fine-tuning for domain adaptation

---

## ⚠️ Limitations

* Small custom dataset
* Domain mismatch (language + recording conditions)
* Not optimized for real-time deployment

---

## 🚀 Future Work

* Transformer models (e.g., Wav2Vec2)
* Larger and multilingual datasets
* Domain adaptation techniques
* Real-time deployment systems

---

## 📬 Contact

* 📧 [busementes01@gmail.com](mailto:busementes01@gmail.com)
* 💼 linkedin.com/in/rabiabusementes

---

