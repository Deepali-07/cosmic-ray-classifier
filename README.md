
# 🌌 Cosmic Ray Classifier

A machine learning-powered application that classifies **cosmic ray events** based on measurable physical parameters such as **energy, angle, magnetic field, and temperature**.  
Built using **Python**, **Scikit-learn**, and **Gradio**, this project bridges space physics with artificial intelligence — providing both **predictions** and **visual insights** through an interactive web interface.

---

## 🚀 Overview

Cosmic rays are high-energy particles originating from outer space.  
This project uses machine learning to classify these events into distinct particle types using simulated or collected data.  
It also provides data visualizations and feature importance insights for better interpretability.

---

## ✨ Key Features

✅ **Cosmic Ray Prediction** — Predict particle type from custom physical parameters  
📊 **Feature Importance Analysis** — Understand which features drive the model’s predictions  
📈 **Data Visualization** — View dataset distributions and 3D projections interactively  
🧠 **Machine Learning Integration** — Random Forest model trained on standardized inputs  
🌐 **Interactive Gradio Interface** — Lightweight, browser-based user interface  

---

## 🧩 Tech Stack

| Component | Technology Used |
|------------|----------------|
| **Language** | Python 3.10+ |
| **Machine Learning** | Scikit-learn |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Plotly |
| **Web Interface** | Gradio |
| **Model Storage** | Joblib / Pickle |

---

## 🗂️ Project Structure

```

cosmic-ray-classifier/
│
├── data/
│   └── cosmic_events.csv           # Dataset
│
├── models/
│   ├── rf_model.pkl                # Trained RandomForest model
│   └── scaler.pkl                  # Scaler used for preprocessing
│
├── visualizations/
│   └── feature_importance.png      # Generated plots
│
├── app.py                          # Gradio web app
├── requirements.txt
├── README.md
└── .gitignore

````

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/yourusername/cosmic-ray-classifier.git
cd cosmic-ray-classifier
````

### 2️⃣ Create and activate virtual environment

```bash
python -m venv env
# Activate
# On Windows:
env\Scripts\activate
# On Mac/Linux:
source env/bin/activate
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Run the Application

Launch the Gradio web app:

```bash
python app.py
```

Once started, open the local server link:

```
http://127.0.0.1:7860
```

You’ll see the interactive interface for:

* Inputting feature values
* Getting model predictions
* Viewing visualizations

---

## 🧠 Model Training (Optional)

If you want to retrain or fine-tune the model, run:

```python
import pandas as pd
from sklearn.ensemble import RandomForestClassifier
from sklearn.preprocessing import StandardScaler
import joblib

# Load data
data = pd.read_csv("data/cosmic_events.csv")
X = data[['energy', 'angle', 'magnetic_field', 'temperature']]
y = data['particle']

# Preprocess
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Train model
model = RandomForestClassifier(random_state=42)
model.fit(X_scaled, y)

# Save model and scaler
joblib.dump(model, "models/rf_model.pkl")
joblib.dump(scaler, "models/scaler.pkl")
```

---

## 📊 Visualizations

### 🔹 1. Feature Importance

Visualizes which parameters most influence particle classification.

### 🔹 2. 3D Scatter Plot

Displays event clustering by energy, angle, and time-of-flight.

### 🔹 3. Distribution Plots

Shows histograms and pairplots for understanding feature relationships.

---

## 📷 Preview

> **Prediction Interface**
> *(Example UI once app is launched via Gradio)*
>
> ![App Screenshot Placeholder](https://via.placeholder.com/800x400.png?text=Gradio+Cosmic+Classifier+UI)

---

## 👩‍🚀 Author

**Deepali Madala**
💫 AI & ML Engineer | Passionate about Space, Physics & AI Integration
📧 (mailto:deepali.madala@gmail.com)
🌍 [LinkedIn](www.linkedin.com/in/deepali-madala-53b252232) | [GitHub](https://github.com/Deepali-07)

> *"Exploring cosmic mysteries through the lens of Artificial Intelligence."*

---

## 🪄 License

This project is released under the **MIT License** — free to use, modify, and distribute with attribution.

---

⭐ **If you found this project helpful, consider giving it a star on GitHub!**

```
