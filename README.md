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
Model Performance
Training Results
Epoch	Training Accuracy	Training Loss	Validation Accuracy	Validation Loss
1	61.80%	0.6460	77.32%	0.4867
2	76.18%	0.4951	80.07%	0.4286
3	81.97%	0.4004	81.38%	0.4061
4	85.02%	0.3395	83.71%	0.3722
5	88.18%	0.2744	83.56%	0.4090
Final Performance
Training Accuracy: 88.18%
Validation Accuracy: 83.56%
Training Loss: 0.2744
Validation Loss: 0.4090
The CNN model demonstrates effective learning on the Cats vs Dogs dataset with a validation accuracy of approximately 83.6% after 5 epochs. The model consists of three convolutional blocks followed by fully connected layers with dropout regularization to reduce overfitting.

## 📖 Dataset

The model is trained on the **Microsoft Cats vs Dogs** dataset — 25,000 labeled images of cats and dogs (12,500 each).

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
