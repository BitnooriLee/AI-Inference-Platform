# AI Inference Platform

Production-style LLM serving platform built with Kubernetes, vLLM, FastAPI, Prometheus, and Grafana.

A cloud-native inference platform designed to deploy, scale, monitor, and operate open-source large language models (LLMs) in a production-like environment.

---

## Why This Project

Most AI projects focus on training models or building chat applications.

This project focuses on the infrastructure layer required to serve LLMs reliably in production:

* Model Serving
* API Gateway
* Containerization
* Kubernetes Orchestration
* Observability
* Autoscaling
* Cloud Infrastructure

The goal is to bridge the gap between AI research and AI operations.

---

## System Architecture

```text
                    ┌─────────────┐
                    │    User     │
                    └──────┬──────┘
                           │
                           ▼

                ┌────────────────────┐
                │   FastAPI Gateway  │
                │ Authentication     │
                │ Rate Limiting      │
                └─────────┬──────────┘
                          │
                          ▼

                ┌────────────────────┐
                │       vLLM         │
                │  Model Serving     │
                └─────────┬──────────┘
                          │
                          ▼

                ┌────────────────────┐
                │   Qwen / Llama     │
                │      Models        │
                └────────────────────┘


                          ▲
                          │

       ┌──────────────────┼──────────────────┐
       │                  │                  │
       ▼                  ▼                  ▼

┌─────────────┐  ┌─────────────┐  ┌─────────────┐
│ Prometheus  │  │ Grafana     │  │ Loki        │
│ Metrics     │  │ Dashboards  │  │ Logs        │
└─────────────┘  └─────────────┘  └─────────────┘
```

---

## Technology Stack

### Infrastructure

* Terraform
* Google Cloud Platform (GCP)
* Google Kubernetes Engine (GKE)

### Containerization

* Docker
* Kubernetes
* Helm

### AI Serving

* vLLM
* Qwen
* Llama

### Backend

* FastAPI
* Python

### Observability

* Prometheus
* Grafana
* Loki

### CI/CD

* GitHub Actions

---

## Core Features

### Model Serving

Deploy open-source LLMs using vLLM.

Supported models:

* Qwen 3
* Llama 3
* Future model extensions

---

### API Gateway

FastAPI-based inference gateway.

Responsibilities:

* Request validation
* Authentication
* Rate limiting
* Model routing
* Health checks

---

### Kubernetes Deployment

All workloads run inside Kubernetes.

Capabilities:

* Rolling updates
* Self-healing
* Horizontal scaling
* Resource management

---

### Observability

Platform-wide monitoring.

Metrics:

* Requests per second
* Token throughput
* GPU utilization
* Latency
* Error rates

Visualization:

* Grafana dashboards
* Prometheus metrics collection

---

### Logging

Centralized logging pipeline.

Capabilities:

* Inference logs
* Error tracking
* Audit trails

---

## Infrastructure as Code

Entire infrastructure is provisioned through Terraform.

Resources:

* VPC
* GKE Cluster
* Service Accounts
* Monitoring Components

Benefits:

* Reproducibility
* Version control
* Automated provisioning

---

## Project Roadmap

### Phase 1

* Terraform fundamentals
* GKE deployment
* FastAPI gateway
* vLLM deployment

### Phase 2

* Prometheus monitoring
* Grafana dashboards
* Centralized logging

### Phase 3

* Autoscaling
* Multiple model routing
* Canary deployments

### Phase 4

* RAG integration
* Vector database
* Production hardening

---

## Learning Objectives

This project focuses on practical experience with:

* Cloud Engineering
* Kubernetes Operations
* Infrastructure as Code
* AI Infrastructure
* Model Serving
* Observability
* Production Reliability

---

## Resume Summary

Architected and deployed a Kubernetes-based AI inference platform using vLLM, FastAPI, and Terraform. Implemented observability, autoscaling, and cloud-native deployment workflows for serving open-source large language models in a production-style environment.
