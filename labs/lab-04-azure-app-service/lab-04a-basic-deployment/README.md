# 📘 Lab 04A - App Service Basic Deployment

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Deploy a Node.js application on Azure App Service and expose it via public URL

---

## ⚙️ Steps Performed
- Created Resource Group → rg-webapp-production
- Created App Service Plan → asp-nodejs-webapp-production (Linux, B1)
- Created Web App → webapp-nodejs-demo-2024
- Selected Runtime → Node 20 LTS
- Configured Environment Variables:
  - NODE_ENV = production
  - PORT = 8080
- Integrated GitHub repository:
  - Repo: Ravitripathi5/nodejs-docs-hello-world
  - Branch: main
- Deployment method:
  - Initially GitHub Actions (failed)
  - Switched to Oryx (success)
- Verified application using default Azure URL

---

## 🔄 Changes from Original Lab
- Region: East US → Central India
- Runtime: Node 18 → Node 20 LTS
- Used Environment Variables (new UI)
- Did NOT use WEBSITE_NODE_DEFAULT_VERSION
- Used forked GitHub repo
- Branch: main (instead of master)
- Deployment: GitHub Actions → Oryx

---

## ❌ Issues Faced
- GitHub Actions deployment failed
- SCM authentication issue
- App not loading initially

---

## ✅ Fix / Solution
- Enabled SCM Basic Authentication
- Switched deployment method to Oryx
- Restarted App Service after configuration

---

## 🌐 Application URL
https://webapp-nodejs-demo-2024.azurewebsites.net

---

## 💻 Commands Used
(To be updated if CLI used)

---

## 📚 Learnings
- App Service deployment flow
- Runtime configuration importance
- GitHub integration with Azure
- Troubleshooting deployment failures

---

## 🧠 Real DevOps Insight
Handled real-world issues:
- Deployment failure
- Authentication issue
- Runtime mismatch

Used debugging approach instead of following only lab steps
