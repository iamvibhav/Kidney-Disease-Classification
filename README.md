
# 🩺 Renalyze: AI-Powered Kidney CT Scan Classification with End-to-End MLOps (Deep Learning | Docker | AWS)

![License](https://img.shields.io/badge/License-MIT-green.svg)
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![MLflow](https://img.shields.io/badge/MLflow-Tracking-success)
![DVC](https://img.shields.io/badge/DVC-Enabled-purple)
![Docker](https://img.shields.io/badge/Docker-Ready-blue.svg)



---

## 🎯 **About the Project**

**Renalyze** is an AI-powered web application that **classifies kidney CT scans** as either *Normal* or *Tumor*, providing rapid and accessible diagnostic assistance to healthcare professionals and researchers.

Built with a robust deep learning pipeline using **transfer learning (VGG16)**, Renalyze integrates **modern MLOps practices** such as MLflow experiment tracking and DVC data versioning to ensure full reproducibility. Its **Flask-based web interface** offers an intuitive user experience for uploading scans and receiving instant predictions.

The application is **containerized using Docker** for consistent, scalable deployment and orchestrated to **AWS EC2 and ECR via GitHub Actions CICD pipelines**, demonstrating real-world deployment workflows used in industry.

---






## ✨ **Features**

* 🧠 **Deep Learning**: Transfer learning with VGG16 for kidney CT scan classification (Normal vs Tumor)
* 🔬 **Modular ML Pipeline**: Data ingestion, preprocessing, training, evaluation, and prediction stages
* ⚙️ **MLOps Integration**: MLflow for experiment tracking, Dagshub for remote tracking, DVC for data/model versioning
* 🌐 **Web Application**: Flask-based UI for image upload and real-time predictions
* 🚀 **Deployment Ready**: Dockerized app with AWS EC2 & ECR deployment via GitHub Actions CICD
* 🔧 **Configurable & Organized**: Central YAML configs, structured logging, and clean codebase for easy customization



---


## 💻 **Tech Stack**

| Category             | Technologies / Libraries                     |
| -------------------- | -------------------------------------------- |
| **Language**         | Python 3.8+                                  |
| **Deep Learning**    | TensorFlow, Keras, Transfer Learning (VGG16) |
| **ML & Data**        | Scikit-learn, Pandas, NumPy                  |
| **Web Framework**    | Flask, Flask-CORS                            |
| **MLOps & Tracking** | MLflow, Dagshub, DVC                         |
| **Deployment**       | Docker, AWS EC2, AWS ECR, GitHub Actions     |
| **UI & Styling**     | HTML5, CSS3, Bootstrap 4, jQuery             |
| **Utilities**        | PyYAML, JSON, Logging                        |
| **Version Control**  | Git, GitHub                                  |


---

## 🗂️ **Project Structure**

```

Kidney-Disease-Classification/
├── app.py                  # Flask web app entry point
├── main.py                 # ML pipeline orchestrator (training, evaluation)
├── params.yaml             # All training/config parameters
├── requirements.txt        # Python dependencies
├── Dockerfile              # Docker deployment config
├── .gitignore              # Git ignore rules
├── templates/
│   └── index.html          # Web app UI
├── artifacts/              # (gitignored) Trained models, logs, etc.
│   └── training/model.h5   # Saved trained model
├── research/               # Jupyter notebooks for experiments
├── config/                 # YAML config files for pipeline
├── src/
│   └── cnnClassifier/
│       ├── pipeline/       # Pipeline stages (ingestion, training, eval, prediction)
│       ├── components/     # Core logic for each pipeline stage
│       ├── entity/         # Config dataclasses
│       ├── config/         # Configuration manager
│       ├── utils/          # Helper functions
│       └── logging/        # Logging setup
├── scores.json             # Latest evaluation metrics
└── README.md               # Project documentation

````

---

## ⚙️ **Installation**

1. **Clone the repository:**

```bash
git clone https://github.com/iamvibhav/Kidney-Disease-Classification.git
cd Kidney-Disease-Classification
````

2. **Create and activate virtual environment (conda recommended):**

```bash
conda create -n kidney python=3.9
conda activate kidney
```

3. **Install dependencies:**

```bash
pip install -r requirements.txt
```

4. **Initialize DVC:**

```bash
dvc init
dvc pull
```

---

## 🚀 **Usage**

### **Train the Model**

```bash
python main.py
```

Runs the full ML pipeline: data ingestion ➔ training ➔ evaluation ➔ saves best model.

### **Launch the Web App**

```bash
python app.py
```

* Visit [http://localhost:8080](http://localhost:8080).
* Upload a CT scan image and view predictions instantly.

---

## 🔬 **Experiments & Tracking**

**MLflow + Dagshub integration** allows tracking parameters, metrics, and models remotely.

1. **Authorize Dagshub (Windows example):**

```powershell
$env:MLFLOW_TRACKING_URI="https://dagshub.com/iamvibhav/Kidney-Disease-Classification.mlflow"
$env:MLFLOW_TRACKING_USERNAME="iamvibhav"
$env:MLFLOW_TRACKING_PASSWORD="your_token_here"
```
---

## 🚢 **Deployment**

* **AWS CICD ready**: Uses Docker, GitHub Actions, and AWS EC2/ECR for automated deployment pipelines.





---

## 📸 **Screenshots**

> *(Add your app UI, predictions, and MLflow dashboard screenshots here.)*

---

## 🤝 **Contributing**

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

---

## 📝 **License**

This project is licensed under the **MIT License**.

---

## 📧 **Contact**

**Vibhav**
[Portfolio](https://iamvibhav30.vercel.app/) |[GitHub](https://github.com/iamvibhav) | [LinkedIn](https://linkedin.com/in/iamvibhav)




*Built with ❤️ for impactful healthcare AI and as a showcase of full-stack ML engineering.*


---
