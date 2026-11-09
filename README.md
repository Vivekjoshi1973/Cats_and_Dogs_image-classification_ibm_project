# 🐱🐶 Cats and Dogs Image Classification

A **Cats vs Dogs image classifier** built with a **CNN (Convolutional Neural Network)** and served through a **Flask** web app — upload an image and get an instant prediction.

> IBM Project — developed by **Vivek Joshi**

---

## 📸 Demo

Upload an image through the web UI and the app predicts whether it's a **Cat** 🐱 or a **Dog** 🐶.

Screenshots of the app in action are available in the [`Screenshots/`](Screenshots/) folder.

---

## 🧠 Model

- **Architecture:** Convolutional Neural Network (CNN)
- **Input size:** 128 × 128 RGB images
- **Classes:** Cat, Dog
- **Framework:** Deep learning on the classic Cats vs Dogs dataset

## 🌐 Web App

A Flask-based frontend that lets you:

1. Upload any cat/dog image
2. Preprocess it (resize to 128×128, normalize pixel values to `[0, 1]`)
3. Run inference and display the prediction with the uploaded image
4. Loading animation while the prediction runs

> **Note:** `app.py` currently ships with placeholder (random) prediction logic for demo purposes — plug in your trained CNN model to make real predictions.

---

## 📂 Project Structure

```
Cats_and_Dogs_image-classification_ibm_project/
├── app.py                  # Flask app: upload, preprocess & predict
├── templates/
│   └── index.html          # Frontend UI
├── static/
│   ├── style.css           # Styling
│   ├── script.js           # Loading bar & spinner logic
│   └── *.jpg               # Sample images
├── Screenshots/            # App screenshots
├── requirements.txt        # Python dependencies
└── LICENSE                 # MIT License
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.9+

### Installation

```bash
git clone https://github.com/Vivekjoshi1973/Cats_and_Dogs_image-classification_ibm_project.git
cd Cats_and_Dogs_image-classification_ibm_project
pip install -r requirements.txt
```

### Run the App

```bash
python app.py
```

Open **http://localhost:5000** in your browser, upload an image, and click **Predict**.

---

## 📦 Dependencies

| Package  | Purpose                        |
|----------|--------------------------------|
| Flask    | Web server & routing           |
| NumPy    | Array operations / preprocessing |
| Pillow   | Image loading & resizing       |
| gunicorn | Production WSGI server         |

---

## 📖 Dataset

The model is trained on the **Microsoft Cats vs Dogs** dataset — 25,000 labeled images of cats and dogs (12,500 each).

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
