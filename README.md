# 🎙️ Deepfake Voice Detection System

This project presents a deepfake speech detection system using a Light Convolutional Neural Network (LCNN). The system is trained and evaluated on the ASVspoof2019 dataset and a custom Turkish speech dataset.

## 🚀 Features

* LCNN-based deepfake detection model
* Log-Mel spectrogram feature extraction
* Cross-dataset evaluation (LA, PA → Custom)
* Noise robustness analysis
* Equal Error Rate (EER) evaluation

## 📊 Results

| Experiment  | EER    |
| ----------- | ------ |
| LA Baseline | 1.41%  |
| PA Baseline | 11.01% |
| LA → Custom | 6.67%  |
| PA → Custom | 18.76% |

## 📂 Datasets

* ASVspoof2019 (LA & PA)
* Custom Turkish dataset (real + AI-generated speech)

## ⚙️ Technologies

* Python
* PyTorch
* Librosa
* NumPy

## 🧠 Key Insights

* High performance in matched datasets (LA)
* Significant performance drop in cross-dataset scenarios
* Domain mismatch is a critical challenge

## ▶️ How to Run

```bash
pip install -r requirements.txt
```

Run training:

```bash
python src/train.py
```

## 📌 Future Work

* Improve cross-dataset generalization
* Explore pretrained models (Wav2Vec2)
* Build a real-time detection web app

## 👩‍💻 Author

Rabia Buse Menteş


