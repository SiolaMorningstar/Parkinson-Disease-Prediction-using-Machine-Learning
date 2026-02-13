# 🧠 Parkinson’s Disease Detection System
Ensemble Semi-Supervised Learning with Audio Analysis
📌 Project Overview

This project implements a Parkinson’s Disease Detection System using:

🧠 Semi-Supervised Learning

🌲 Random Forest

📈 Gradient Boosting

🤝 Ensemble Voting Classifier

🎤 Voice-based Audio Feature Extraction

The system combines structured clinical datasets (CSV files) and real-time voice recordings to predict whether a person is:

Healthy (0)

Parkinson’s Patient (1)

It is designed to run in Google Colab for easy experimentation and microphone recording.

🚀 Key Features

✅ Combine multiple CSV datasets
✅ Automatic preprocessing & cleaning
✅ Semi-supervised learning (Label Propagation & Label Spreading)
✅ Supervised ensemble models
✅ Voice feature extraction using MFCC, spectral & chroma features
✅ Real-time microphone recording (Colab)
✅ Majority voting final prediction
✅ Model evaluation (Accuracy, Confusion Matrix, ROC Curve)
✅ Feature importance visualization
✅ Audio-based Parkinson prediction

🏗️ System Architecture
CSV Data (Dataset 1 + Dataset 2)
        ↓
Data Cleaning & Preprocessing
        ↓
Semi-Supervised Setup (70% labeled / 30% unlabeled)
        ↓
Model Training:
   - Label Propagation
   - Label Spreading
   - Random Forest
   - Gradient Boosting
        ↓
Ensemble Voting
        ↓
Evaluation & Visualization
        ↓
Audio Feature Extraction (MFCC, Spectral, Chroma)
        ↓
Final Parkinson Prediction

📂 Dataset Requirements

The system expects:

Two CSV files

A binary target column:

status OR

Label OR

class

(If none found, last column is used automatically)

Target values must represent:

0 → Healthy

1 → Parkinson

If labels are non-numeric, automatic mapping is attempted.

🛠️ Installation

Run in Google Colab or local Jupyter Notebook.

Install dependencies:

pip install scikit-learn pandas numpy librosa soundfile matplotlib seaborn pydub

📊 Models Used
1️⃣ Semi-Supervised Models

Label Propagation

Label Spreading

These models use both labeled and unlabeled data.

2️⃣ Supervised Models

Random Forest Classifier

Gradient Boosting Classifier

3️⃣ Ensemble Model

Soft Voting Classifier combining:

Random Forest

Gradient Boosting

🏆 Final Prediction Strategy

Final decision is made using:

Majority Voting Across:
LP + LS + RF + GB + Ensemble

🎤 Audio Processing

The system extracts advanced voice features:

MFCC (Mel-Frequency Cepstral Coefficients)

Chroma Features

Spectral Centroid

Spectral Rolloff

Zero Crossing Rate

Audio can be:

Recorded directly in Google Colab

Uploaded manually (WAV, MP3, etc.)

📈 Evaluation Metrics

Accuracy

Confusion Matrix

Classification Report

ROC Curve & AUC

Feature Importance (Random Forest)

Prediction Distribution

All results are saved as:

parkinson_prediction_results.png

📊 Example Output

The system prints:

FINAL PREDICTION:
This audio file is of Parkinson patient.
Confidence: 87.45%


And generates:

Accuracy comparison bar chart

Confusion matrix heatmap

ROC curve

Feature importance graph

Audio prediction visualization

🔬 Semi-Supervised Learning Strategy

70% labeled data

30% unlabeled data

Unlabeled samples marked as -1

Graph-based propagation spreads labels

This improves performance when labeled medical data is limited.

📌 How to Run

Open in Google Colab

Upload two CSV datasets

Allow microphone access (optional)

Record or upload audio

View prediction results & visualizations

⚠️ Disclaimer

This project is for:

Educational purposes

Research experimentation

It is NOT a medical diagnostic tool and should not replace professional medical advice.

👨‍💻 Author

Alois Ulka Gabriel Rodrigues
GitHub: https://github.com/SiolaMorningstar

🌟 Future Improvements

Deep learning (CNN/LSTM for voice)

Hyperparameter optimization

Web app deployment (Streamlit/Flask)

Cross-validation improvements

Real clinical dataset validation

Model explainability (SHAP)

📜 License

This project is open-source under the MIT License.
