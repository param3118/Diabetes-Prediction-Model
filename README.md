# 🌳 Decision Tree Classifier – Diabetes Prediction

This project implements and analyzes a **Decision Tree Classifier** to predict diabetes based on various patient features. The analysis evaluates performance on both **noiseless** and **noisy** datasets, with and without pruning, to study the effects of noise and pruning on accuracy and tree complexity.

---

## 📑 Table of Contents
- [About the Project](#-about-the-project)
- [Datasets](#-datasets)
- [Methodology](#-methodology)
- [Results](#-results)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Technologies Used](#-technologies-used)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📖 About the Project
The objective of this assignment is to **train and evaluate a Decision Tree classifier** for diabetes prediction. We compare results on:
- **Noiseless Dataset** (`diabetes.csv`)
- **Noisy Dataset** (`diabetes_noise.csv`)

Additionally, the effect of **pruning** on decision tree depth, node count, and model performance is studied.

---

## 📂 Datasets
- **`diabetes.csv`** → Clean (noiseless) dataset with patient health features.  
- **`diabetes_noise.csv`** → Dataset with artificially introduced noise.  

Each dataset includes **medical features** such as glucose level, BMI, age, blood pressure, etc., with the target label indicating **diabetes presence (Yes/No)**.

---

## ⚙️ Methodology
1. Preprocessed the datasets (handled missing values, normalized features).  
2. Built a **Decision Tree classifier** using `scikit-learn`.  
3. Evaluated the model on **accuracy, precision, and recall**.  
4. Applied **tree pruning** to reduce overfitting.  
5. Compared results for **noisy vs noiseless datasets**.  

---

## 📊 Results

### 📌 Noiseless Dataset (`diabetes.csv`)
| Metric       | Before Pruning | After Pruning |
|--------------|----------------|---------------|
| **Accuracy** | 0.7143         | 0.7597        |
| **Precision**| 0.6913         | 0.7597        |
| **Recall**   | 0.6970         | 0.7606        |
| **Tree Size**| Height: 16, Nodes: 153 | Height: 7, Nodes: 35 |

---

### 📌 Noisy Dataset (`diabetes_noise.csv`)
| Metric       | Before Pruning | After Pruning |
|--------------|----------------|---------------|
| **Accuracy** | 0.4811         | 0.6054        |
| **Precision**| 0.4593         | 0.5944        |
| **Recall**   | 0.4600         | 0.5954        |
| **Tree Size**| Height: 21, Nodes: 371 | Height: 12, Nodes: 94 |

---

### ✅ Key Insights
- Pruning significantly improved **performance** and reduced **tree complexity**.  
- Noisy data led to **lower accuracy and unstable precision/recall**.  
- The **noiseless dataset after pruning** achieved the **best balance** of performance and interpretability.  

---

## 📁 Project Structure
```bash
diabetes_decision_tree/
│── diabetes.ipynb          # Jupyter Notebook with code & analysis
│── data/
│   ├── diabetes.csv        # Noiseless dataset
│   ├── diabetes_noise.csv  # Noisy dataset
│── results/                # Plots, evaluation metrics, and confusion matrices
│── README.md               # Documentation
│── requirements.txt        # Python dependencies

⚙️ Installation

Clone this repository and install dependencies:
# Clone repo
git clone https://github.com/<your-username>/diabetes-decision-tree.git
cd diabetes-decision-tree

## 🛠 Technologies Used

Python 3.8+

Pandas, NumPy – Data handling

Matplotlib, Seaborn – Visualization

Scikit-learn – Decision Tree model

Jupyter Notebook – Interactive environment

## Contributions are welcome!

Fork this repository

Create a new branch (feature-branch)

Commit your changes

Push to the branch

Open a Pull Request


