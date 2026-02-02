# End-to-End MLOps Pipeline for Phishing Detection

This repository contains an end-to-end MLOps pipeline for building, deploying and maintaining a machine learning system to detect phishing websites using network and URL-based features.

The project demonstrates how a machine learning solution can be taken from raw data to a production-ready, containerized and automated system with continuous integration and deployment support.

---

## Project Objective

The objective of this project is to design and implement a complete production-oriented machine learning workflow that:

- ingests phishing and legitimate website data
- validates incoming data using a predefined schema
- performs feature preparation and transformation
- trains and evaluates a machine learning model
- stores trained artifacts and prediction results
- exposes the trained model through a REST API
- supports automated workflows and containerized deployment

---

## Key Features

- End-to-end machine learning pipeline
- Automated data ingestion and validation
- Data preprocessing and feature engineering
- Model training and evaluation
- Artifact generation and version management
- REST API for model inference
- Docker-based deployment
- CI pipeline using GitHub Actions
- Optional cloud deployment support using AWS

---

## Tech Stack

- Python
- Scikit-learn
- Pandas, NumPy
- FastAPI
- MongoDB
- Docker
- Git
- GitHub Actions
- AWS ECR and EC2 (optional)

---

## Project Structure

```
.
├── app.py                      # REST API entry point
├── main.py                     # pipeline execution script
├── push_data.py                # data ingestion utility
├── requirements.txt
├── Dockerfile
├── setup.py
├── test_mongodb.py
├── data_schema/                # schema definition for validation
├── valid_data/                 # validated datasets
├── Artifacts/                  # pipeline artifacts
├── final_model/                # trained model
├── prediction_output/          # inference results
├── templates/                  # API / UI templates
└── .github/workflows/          # CI workflows
```

---

## MLOps Pipeline Overview

The pipeline is organized into the following stages:

1. Data ingestion from source and database
2. Schema-based data validation
3. Data transformation and feature preparation
4. Model training
5. Model evaluation and comparison
6. Model and artifact versioning
7. API-based model serving
8. Continuous integration using GitHub Actions

---

## How to Run the Project Locally

### 1. Create a virtual environment

```bash
python -m venv venv
```

Activate the environment:

Linux / Mac

```bash
source venv/bin/activate
```

Windows

```bash
venv\Scripts\activate
```

---

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Run the training pipeline

```bash
python main.py
```

This will execute the complete pipeline and generate model and data artifacts.

---

## Run the Inference API

```bash
python app.py
```

After starting the server, the trained model can be accessed through the REST API for inference.

---

## Docker Build and Run

Build the container:

```bash
docker build -t phishing-mlops .
```

Run the container:

```bash
docker run -p 8080:8080 phishing-mlops
```

---

## CI Pipeline

This project uses GitHub Actions to automate:

- dependency installation
- pipeline execution
- and basic validation checks

The workflow configuration can be found in:

```
.github/workflows
```

---

## Cloud Deployment (Optional)

The project supports container-based deployment using:

- AWS Elastic Container Registry (ECR)
- AWS EC2

AWS credentials are configured using GitHub Secrets in the repository settings.

---

## What This Project Demonstrates

- Design of a complete production-oriented ML system
- Automation of training and evaluation workflows
- Separation of pipeline logic and serving logic
- Reproducible experiments and artifact tracking
- Backend stability using modular pipeline components
- Practical usage of Docker and CI/CD in machine learning systems

---

## Author

Abhishek  
B.Tech – Computer Science and Engineering (AI & ML)  
K.R. Mangalam University, India
