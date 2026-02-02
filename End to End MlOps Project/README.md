End-to-End MLOps Pipeline for Phishing Detection

This project implements a complete end-to-end MLOps pipeline for detecting phishing websites using machine learning.
It covers the full lifecycle of a production ML system including data ingestion, validation, model training, evaluation, versioning, and API-based deployment.

The project is designed to demonstrate reproducible training, automated workflows and containerized deployment.

Project Objective

The goal of this project is to build a scalable and automated machine learning system that:

ingests structured network and URL related data,

validates and preprocesses incoming data,

trains and evaluates a phishing detection model,

stores trained artifacts and predictions,

and exposes the trained model through an API.

Key Features

End-to-end machine learning pipeline

Automated data ingestion and validation

Model training and evaluation pipeline

Artifact and model version management

REST API for inference

Dockerized application

CI workflow using GitHub Actions

Tech Stack

Python

Scikit-learn

Pandas, NumPy

FastAPI

Docker

GitHub Actions

MongoDB (for data storage)

AWS ECR / EC2 (for deployment – optional)

Project Structure
.
├── app.py                     # API entry point
├── main.py                    # pipeline execution
├── push_data.py               # data ingestion utility
├── requirements.txt
├── Dockerfile
├── setup.py
├── test_mongodb.py
├── data_schema/               # schema validation
├── valid_data/                # validated datasets
├── Artifacts/                 # pipeline artifacts
├── final_model/               # trained model
├── prediction_output/         # inference results
├── templates/                 # UI / API templates
└── .github/workflows/         # CI pipeline

MLOps Pipeline Overview

Data ingestion from source

Data validation using predefined schema

Data transformation and feature preparation

Model training

Model evaluation and comparison

Artifact generation and versioning

Deployment through API

Continuous integration using GitHub Actions

How to Run Locally
1. Create virtual environment
python -m venv venv
source venv/bin/activate

2. Install dependencies
pip install -r requirements.txt

3. Run training pipeline
python main.py

Run API
python app.py


The API will start locally and can be used for inference.

Docker Build & Run
docker build -t phishing-mlops .
docker run -p 8080:8080 phishing-mlops

CI Pipeline

This repository uses GitHub Actions to automate:

dependency installation

basic checks

pipeline execution

The workflow configuration is available in:

.github/workflows

Cloud Deployment (Optional)

This project supports container-based deployment using:

AWS ECR for container registry

AWS EC2 for hosting

AWS credentials are configured using GitHub secrets.

What this project demonstrates

Building a production-oriented ML pipeline

Separation of training and serving logic

Reproducible experiments

Backend stability through modular pipelines

Real-world MLOps practices using Docker and CI/CD

Author

Abhishek
B.Tech CSE (AI & ML), K.R. Mangalam University
