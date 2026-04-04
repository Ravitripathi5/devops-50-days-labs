# 📘 Lab 04B - App Service Container Deployment (ACR + CD)

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Deploy a containerized application using Azure Container Registry (ACR) and Azure App Service with Continuous Deployment

---

## ⚙️ Steps Performed

### 🔹 Resource Setup
- Created Resource Group → rg-webapi-containerapp (Central India)
- Created Azure Container Registry → acrwebapidev2024 (Basic SKU)
- Enabled Admin User for ACR authentication

---

### 🔹 Application Setup
- Created Dockerfile using nginx:alpine
- Added index.html and style.css
- Version 1.0 deployed initially

---

### 🔹 Build & Push Image
- Logged into Azure and ACR
- Used ACR build (no local Docker required)
- Image pushed: webapi:v1.0

---

### 🔹 App Service Setup
- Created App Service Plan → asp-webapi-linux (Linux, B1)
- Created Web App (Container-based)
- Configured container source → ACR
- Image → webapi
- Tag → latest

---

### 🔹 Continuous Deployment Setup
- Enabled Continuous Deployment in App Service
- Created Webhook in ACR → webhookwebapicd
- Linked webhook to App Service

---

### 🔹 Application Update
- Updated app version → 2.0.0
- Built and pushed latest image
- Triggered auto deployment via webhook

---

### 🔹 Verification
- Verified via browser → Version 2.0.0 displayed
- Verified via curl → HTTP 200 OK
- Confirmed application health

---

## 🔄 Changes from Original Lab
- Region: East US → Central India
- Web App Name: Auto-generated (instead of static)
- UI: Docker Tab → Container Tab (Azure UI change)
- Webhook Name: Alphanumeric only
- Image Tag: Used latest (for CD)
- Enabled SCM Authentication manually
- Continuous Deployment enabled manually

---

## ❌ Issues Faced
- Webhook not triggering initially
- SCM authentication issue
- Image not updating

---

## ✅ Fix / Solution
- Enabled SCM Basic Authentication
- Used correct webhook URL from Deployment Center
- Switched image tag to latest for CD trigger

---

## 💻 Commands Used
```bash
az login
az acr login --name acrwebapidev2024

az acr build \
  --registry acrwebapidev2024 \
  --image webapi:v1.0 .

az acr build \
  --registry acrwebapidev2024 \
  --image webapi:latest .
