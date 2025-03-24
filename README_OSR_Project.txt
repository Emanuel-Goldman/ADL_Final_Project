# 🧠 Open Set Recognition with EVT on MNIST

This project tackles the problem of **Open Set Recognition (OSR)** using the MNIST dataset. Unlike traditional classification, OSR requires models not only to classify known classes, but also to detect and label previously **unseen** classes as *Unknown*. The project integrates **Extreme Value Theory (EVT)** and other techniques to achieve this goal.

---

## 📌 Objective

Build an image classification system that:
- Accurately classifies digits `0-9` from MNIST (Closed Set).
- Detects and flags out-of-distribution (OOD) samples (e.g., CIFAR-10 or FashionMNIST) as `Unknown` (Open Set).

---

## 🧠 Methods

The solution includes two main models:

### 🔹 Baseline Model
A standard neural network classifier trained on MNIST.

### 🔹 OSR Model
Enhancements include:
- Modeling the embedding space distributions.
- EVT-based tail modeling for thresholding rare activations.
- Uncertainty-based detection (e.g., Monte Carlo Dropout).
- Autoencoders for reconstruction-based anomaly detection.

**Note:** The model is trained only on MNIST. No OOD data is used for training.

---

## 🧪 Evaluation

The model is evaluated on:
- **Closed Set Accuracy** using the MNIST test set.
- **Binary OSR Accuracy** (Known vs Unknown) using CIFAR-10 and/or FashionMNIST as unseen classes.
- **Full OSR Accuracy** across 11 classes (digits `0–9` + `Unknown`).
- Optional: Visualizations using t-SNE or PCA for embedding space.

---

## 📂 Project Structure

```
project-root/
├── Final_project_notebook.ipynb    # Full notebook: training + evaluation
├── summary.pdf                     # Project summary & explanation
├── models/                         # Trained model weights
├── utils/                          # Helper functions and utilities
├── data/                           # MNIST + OOD datasets (ignored by Git)
├── .gitignore                      # Files/folders to be excluded from Git
└── README.md                       # This file
```

---

## 🚀 Running the Project

1. **Clone the repository:**
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. **Install requirements:**
```bash
pip install -r requirements.txt
```

3. **Run the notebook:**
Open `Final_project_notebook.ipynb` in Jupyter or Colab.  
Set `eval_mode = True` to skip training and only run evaluation.

---

## 📝 Summary

See `summary.pdf` for:
- Methodology and reasoning
- Hyperparameters and tuning
- Visual results and figures
- Limitations and future directions

---

## 🏫 Course Info

**Advanced Deep Learning — Final Project**  
Ben-Gurion University, Department of Computer Science  
Instructors: Oren Freifeld & Ron Shapira Weber  
**Due Date:** February 28, 2025

---

## 📬 Contact

For questions or collaboration, feel free to contact me via GitHub.
