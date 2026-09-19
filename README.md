
# 🚗 Vehicle Prediction — End-to-End MLOps Project

<p align="center">
  <b>An end-to-end production-style Machine Learning pipeline with automated training, model evaluation, AWS model registry, Docker, and CI/CD deployment.</b>
</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![ML](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange?logo=scikit-learn)
![MongoDB](https://img.shields.io/badge/Database-MongoDB%20Atlas-green?logo=mongodb)
![AWS](https://img.shields.io/badge/Cloud-AWS-orange?logo=amazon-aws)
![Docker](https://img.shields.io/badge/Container-Docker-blue?logo=docker)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-black?logo=githubactions)

</p>

url - http://44.192.74.109:5000/

---

## 📌 Overview

This project demonstrates how a Machine Learning application can be transformed into a **complete MLOps workflow**, from data ingestion and validation to model training, evaluation, versioning, deployment, and automated CI/CD.

Instead of treating ML as a single training script, the project follows a modular pipeline architecture where every major stage is independently organized and connected through a training pipeline.

### 🔄 End-to-End Workflow

```text
Dataset
   ↓
MongoDB Atlas
   ↓
Data Ingestion
   ↓
Data Validation
   ↓
Data Transformation
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Registry (AWS S3)
   ↓
Prediction Pipeline
   ↓
FastAPI Application
   ↓
Docker
   ↓
GitHub Actions
   ↓
AWS EC2
```

---

## ✨ Key Features

* 🧩 Modular ML pipeline architecture
* 📥 Automated data ingestion from MongoDB Atlas
* ✅ Schema-based data validation
* 🔄 Feature engineering & data transformation
* 🤖 Automated model training
* 📊 Model evaluation with configurable thresholds
* ☁️ AWS S3-based model registry
* 🚀 Prediction pipeline for real-time inference
* 🌐 Web application using FastAPI
* 🐳 Dockerized application
* ⚙️ GitHub Actions CI/CD
* 🖥️ AWS EC2 deployment
* 🏃 GitHub Self-Hosted Runner
* 📦 Amazon ECR for Docker image storage
* 📝 Custom logging system
* ⚠️ Custom exception handling
* 📓 Jupyter notebooks for EDA and experimentation
* 🔐 Environment-based configuration and secrets

---

## 🏗️ Project Architecture

```text
                         ┌──────────────────┐
                         │   MongoDB Atlas   │
                         │      Dataset      │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │  Data Ingestion  │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ Data Validation  │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │Data Transformation│
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │  Model Trainer   │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ Model Evaluation │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │  AWS S3 Model    │
                         │     Registry     │
                         └────────┬─────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    ▼                           ▼
             Training Route              Prediction Route
                    │                           │
                    └─────────────┬─────────────┘
                                  ▼
                         ┌──────────────────┐
                         │   FastAPI App    │
                         └────────┬─────────┘
                                  │
                                  ▼
                              Docker
                                  │
                                  ▼
                         ┌──────────────────┐
                         │    AWS ECR       │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │     AWS EC2      │
                         │ Ubuntu + Docker  │
                         └──────────────────┘
```

---

## 🛠️ Tech Stack

| Category            | Technologies                      |
| ------------------- | --------------------------------- |
| Language            | Python 3.10                       |
| ML                  | Scikit-learn                      |
| Data Processing     | Pandas, NumPy                     |
| Database            | MongoDB Atlas                     |
| API                 | FastAPI                           |
| Frontend            | HTML, CSS, Jinja Templates        |
| Experimentation     | Jupyter Notebook                  |
| Cloud               | AWS                               |
| Model Storage       | Amazon S3                         |
| Containerization    | Docker                            |
| Container Registry  | Amazon ECR                        |
| Compute             | Amazon EC2                        |
| CI/CD               | GitHub Actions                    |
| Deployment Runner   | GitHub Self-Hosted Runner         |
| Version Control     | Git & GitHub                      |
| Configuration       | YAML / Environment Variables      |
| Logging             | Python Logging                    |
| Testing / Debugging | Custom Exceptions & Demo Pipeline |

---

## 📂 Project Structure

```text
├── .github/
│   └── workflows/
│       └── aws.yaml
│
├── notebook/
│   ├── mongoDB_demo.ipynb
│   └── EDA_and_Feature_Engineering.ipynb
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_validation.py
│   │   ├── data_transformation.py
│   │   ├── model_trainer.py
│   │   ├── model_evaluation.py
│   │   └── model_pusher.py
│   │
│   ├── configuration/
│   │   ├── mongo_db_connections.py
│   │   └── aws_connection.py
│   │
│   ├── constants/
│   │   └── __init__.py
│   │
│   ├── data_access/
│   │   └── proj1_data.py
│   │
│   ├── entity/
│   │   ├── config_entity.py
│   │   ├── artifact_entity.py
│   │   ├── estimator.py
│   │   └── s3_estimator.py
│   │
│   ├── pipeline/
│   │   └── training_pipeline.py
│   │
│   └── utils/
│       ├── main_utils.py
│       ├── logger.py
│       └── exception.py
│
├── static/
├── template/
├── app.py
├── demo.py
├── config/
│   └── schema.yaml
├── Dockerfile
├── .dockerignore
├── requirements.txt
├── setup.py
├── pyproject.toml
├── template.py
└── README.md
```

---

## ⚙️ Getting Started

### 1️⃣ Create the Project Structure

The project template can be generated automatically:

```bash
python template.py
```

The project uses `setup.py` and `pyproject.toml` to make local source packages importable throughout the application.

---

### 2️⃣ Create Virtual Environment

```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Verify the environment:

```bash
pip list
```

---

## 🍃 MongoDB Atlas Setup

MongoDB Atlas is used as the project's data source.

### Setup

1. Create a MongoDB Atlas account and project.
2. Create an **M0 cluster**.
3. Create a database user.
4. Configure network access.
5. Copy the Python connection string.
6. Store the connection string securely as an environment variable.

For local development:

### PowerShell

```powershell
$env:MONGODB_URL="mongodb+srv://<username>:<password>@..."
```

Verify:

```powershell
echo $env:MONGODB_URL
```

The dataset can then be uploaded to MongoDB using the notebook workflow.

---

## 🔄 ML Pipeline Components

### Data Ingestion

Connects to MongoDB Atlas, retrieves records, converts the data into a Pandas DataFrame, and creates the ingestion artifact.

### Data Validation

Uses the project schema configuration to validate:

* Required columns
* Data types
* Dataset structure
* Data consistency

### Data Transformation

Performs preprocessing and feature transformation before model training.

### Model Training

Trains the ML model using the processed dataset and stores the trained model as an artifact.

### Model Evaluation

Compares the newly trained model against the existing model using a configurable evaluation threshold.

```python
MODEL_EVALUATION_CHANGED_THRESHOLD_SCORE = 0.02
```

This helps prevent an inferior model from automatically replacing the existing model.

### Model Pusher

Approved models are pushed to the AWS S3 model registry.

---

## ☁️ AWS Model Registry

AWS S3 is used for centralized model storage.

```text
S3 Bucket
└── model-registry/
    └── trained model artifacts
```

Example configuration:

```python
MODEL_BUCKET_NAME = "my-model-mlopsproj2"
MODEL_PUSHER_S3_KEY = "model-registry"
```

AWS credentials are provided through environment variables rather than being hard-coded into the source code.

---

## 🔮 Prediction Pipeline

The project includes a dedicated prediction pipeline that loads the approved model from the model registry and performs inference through the application.

Two application routes are provided:

```text
/training
```

Used to trigger the training workflow.

```text
/predict
```

Used for model inference.

---

## 🐳 Dockerized Application

The complete application is containerized using Docker.

Build the image:

```bash
docker build -t vehicleproj .
```

Run locally:

```bash
docker run -p 5080:5080 vehicleproj
```

This ensures the application runs consistently across development and deployment environments.

---

## 🔁 CI/CD Pipeline

The project implements an automated deployment workflow using **GitHub Actions**.

```text
Git Push
   ↓
GitHub Actions
   ↓
Build Docker Image
   ↓
Push Image → Amazon ECR
   ↓
Self-Hosted Runner
   ↓
AWS EC2
   ↓
Run Docker Container
   ↓
Live Application
```

The CI/CD workflow is configured inside:

```text
.github/workflows/aws.yaml
```

---

## 🐳 Amazon ECR

Amazon ECR stores the project's Docker image.

Example repository:

```text
vehicleproj
```

The CI/CD pipeline builds and pushes updated images to ECR automatically.

---

## 🖥️ AWS EC2 Deployment

The application is deployed on an Ubuntu EC2 instance.

Deployment environment:

```text
AWS EC2
Ubuntu 24.04
Docker
GitHub Self-Hosted Runner
```

Docker is installed on the EC2 instance and the GitHub runner allows GitHub Actions to execute deployment commands directly on the server.

---

## 🏃 Self-Hosted GitHub Runner

Instead of relying only on GitHub-hosted infrastructure, the project uses a self-hosted runner on the EC2 machine.

```text
GitHub Repository
       │
       ▼
GitHub Actions
       │
       ▼
Self-Hosted Runner
       │
       ▼
AWS EC2
       │
       ▼
Docker Container
```

This provides a direct CI/CD path from repository changes to the deployed application.

---

## 🔐 Secrets & Configuration

Sensitive credentials are managed using environment variables and GitHub repository secrets.

Example GitHub secrets:

```text
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO
```

The MongoDB connection string is also supplied through an environment variable:

```text
MONGODB_URL
```

> 🔒 Credentials and connection strings are intentionally excluded from the repository.

---

## 📊 Observability & Reliability

The project includes supporting components commonly required in production ML systems:

### Logging

Centralized logging helps track pipeline execution and debugging information.

### Exception Handling

Custom exception handling provides meaningful error information across pipeline components.

### Configuration Management

Dataset schema, model thresholds, AWS configuration, and pipeline settings are separated from core business logic.

### Artifacts

Each pipeline stage produces structured artifacts that can be consumed by subsequent stages.

---

## 🚀 Deployment Result

After the CI/CD pipeline successfully completes:

```text
GitHub
   ↓
Docker Build
   ↓
Amazon ECR
   ↓
AWS EC2
   ↓
FastAPI + ML Model
```

The application can then be accessed through the EC2 public IP and configured application port.

```text
http://<EC2-PUBLIC-IP>:5080
```

---

## 🎯 What This Project Demonstrates

This project goes beyond simply training an ML model. It demonstrates the complete lifecycle of an ML application:

**Data → Validation → Transformation → Training → Evaluation → Model Registry → Prediction → Docker → CI/CD → Cloud Deployment**

It brings together **Machine Learning, Software Engineering, Cloud Computing, Containerization, and DevOps practices** into one end-to-end workflow.

---


⭐ If you found this project useful, consider giving the repository a star!
