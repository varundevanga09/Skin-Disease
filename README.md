# 🔬 Skin Disease Detection — Deep Learning Diagnosis System

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

> A computer-aided diagnosis system that classifies skin diseases from uploaded images using an ensemble of deep learning models — deployed as a full-stack Flask web application.

---

## 🧠 The Problem

Accurate skin disease diagnosis is extremely challenging due to:
- Low contrast between lesions and surrounding skin
- Visual similarity between diseased and healthy tissue
- Requirement for high specialist expertise

This system provides an **objective, automated first-pass diagnosis** to assist dermatologists and improve early detection.

---

## 🏗️ System Architecture

```
User Uploads Image
        │
        ▼
┌───────────────┐
│  Flask App    │  ◀── Authentication (SQLite)
│  (Frontend)   │
└──────┬────────┘
       │
       ▼
┌───────────────────────────────────────────┐
│           Preprocessing Pipeline          │
│  Noise Removal → Grayscale → Normalize    │
└──────────────────┬────────────────────────┘
                   │
       ┌───────────┼───────────┐
       ▼           ▼           ▼
  Inception    MobileNet   ZeroShot
  ResNet V2      V2          NN
       │           │           │
       └───────────┼───────────┘
                   ▼
          Final Classification
          (Disease / No Disease)
```

---

## 🤖 Models Used

| Model | Architecture | Strength |
|-------|-------------|---------|
| Inception ResNet V2 | Deep residual + inception | High accuracy on complex patterns |
| Inception V3 | Inception modules | Efficient feature extraction |
| MobileNet | Depthwise separable convolutions | Lightweight, fast inference |
| MobileNet V2 | Inverted residuals | Better accuracy vs MobileNet |
| ZeroShot Neural Network | Zero-shot learning | Generalization to unseen classes |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Deep Learning | TensorFlow / Keras |
| Web Framework | Flask |
| Frontend | HTML, CSS, JavaScript |
| Database | SQLite (user authentication) |
| Model Format | HDF5 (.h5) |
| Experimentation | Jupyter Notebook |
| Language | Python |

---

## ✨ Features

- **Multi-Model Ensemble** — compare predictions across 5 architectures for higher reliability
- **Image Preprocessing** — automatic noise removal, grayscale conversion, normalization
- **User Authentication** — secure signup/login system
- **Web Interface** — clean UI for image upload and result display
- **Pre-trained Model** — ready to run with included `model1.h5`

---

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/varundevanga09/Skin-Disease.git
cd Skin-Disease

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the application
python app.py

# 4. Open in browser
# Navigate to http://localhost:5000
```

---

## 📁 Project Structure

```
Skin-Disease/
├── static/                     # CSS, JS, images
├── templates/                  # HTML templates
├── data/train/                 # Training dataset
├── Final_project.ipynb         # Model training notebook
├── notebook.ipynb              # Experimentation notebook
├── app.py                      # Flask application
├── model1.h5                   # Trained model weights
├── signup.db                   # SQLite user database
└── README.md
```

---

## 📊 Results

The system successfully classifies skin conditions using multi-model inference, providing reliable predictions even on challenging image conditions with low lesion contrast.

---

## 📬 Contact

**Varun Devanga** — [LinkedIn](https://linkedin.com/in/varundevanga09) · [GitHub](https://github.com/varundevanga09)
