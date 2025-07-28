
# 🚀 First MLOps Project: Diabetes Classification API 🧠💉

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-🚀-green)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue?logo=docker)
![License](https://img.shields.io/badge/license-MIT-brightgreen)

---

## 📚 About the Project

This project is a beginner-friendly **MLOps project** that demonstrates how to:

✅ Train a simple ML model (diabetes classification)  
✅ Serve it using a **FastAPI REST API**  
✅ Containerize it with **Docker**  
✅ (Optionally) Deploy on **Kubernetes** or **cloud platforms**

---

## 🎯 Problem Statement

Given a person's medical data (like glucose, BMI, age, etc.), predict whether they have **diabetes** or not.

This is a classic **binary classification problem** solved using `scikit-learn`.

---

## 📁 Project Structure
first-mlops-project/
├── main.py               # FastAPI App
├── train.py              # Model training script
├── model.pkl             # Trained ML model
├── requirements.txt      # Python dependencies
├── Dockerfile            # Docker container definition
└── README.md             # Project documentation

+------------------+      📊 Train      +------------------+
|  Historical Data |  ───────────────▶ |  ML Model (.pkl)  |
+------------------+                   +------------------+
                                              │
                                              ▼
                                     🚀 Model Loaded Into
                                 +------------------------+
                                 |     FastAPI Server     |
                                 +------------------------+
                                              │
                                              ▼
                              🐳 Docker Containerization
                          +------------------------------+
                          |  REST API in Docker Image    |
                          +------------------------------+
                                              │
                                              ▼
                        📦 Pushed to Docker Registry (Optional)
                                              │
                                              ▼
                          ☸️ Kubernetes Deployment via YAML
                      +--------------------------------------+
                      |  Kubernetes Pod Exposes REST API     |
                      |     (ClusterIP/NodePort/Ingress)     |
                      +--------------------------------------+
                                              │
                                              ▼
                             🌐 Accessible via: `http://<host>:8000`

🚀 Getting Started (Locally)
1️⃣ Clone the repo
git clone https://HARSHITHA-G-M/DiabMl-ops
cd DiabMl-ops

2️⃣ Train the Model
python train.py

3️⃣ Run Locally (No Docker)
pip install -r requirements.txt
uvicorn main:app --reload
Open: http://localhost:8000/docs

🐳 Running with Docker
✅ 1. Build Docker Image
docker build -t diabetes-api .

✅ 2. Run the Container
docker run -p 8000:8000 diabetes-api
Open: http://localhost:8000/docs

✅ 2. Deploy on Kubernetes ☸️
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
🔗 Open: http://<your-node-ip>:8000/docs


🌐 API Demo 
Access the live API at:
GET    /         → Health check
POST   /predict  → Send patient data, get prediction

Sample Input (JSON)
{
  "glucose": 148,
  "bmi": 33.6,
  "age": 50,
  "blood_pressure": 72,
  "insulin": 94
}

🧪 Tech Stack
Component	Tech
💻 Language	Python 3.10
🤖 ML Model	Scikit-Learn
🚀 API Server	FastAPI + Uvicorn
🐳 Container	Docker
🧠 Deployment	Kubernetes-ready

💡 Future Ideas
✅ Add GitHub Actions CI/CD pipeline
☁️ Deploy on GCP/AWS using Kubernetes
📈 Add model monitoring (Prometheus, Grafana)
🗃️ Use MLflow or DVC for model versioning

🙌 Author
by HARHSHITHA G M

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
