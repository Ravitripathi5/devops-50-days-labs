
# 📘 Lab 04C - App Service Deployment Slots & Runtime Troubleshooting

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Implement deployment slots in Azure App Service and handle runtime compatibility issues during deployment

---

## ⚙️ Steps Performed

### 🔹 Environment Setup
- Used existing App Service
- Verified runtime configuration

---

### 🔹 Deployment Slot Creation
- Created new deployment slot (staging)
- Configured slot settings via Environment Variables
- Deployed application to staging slot

---

### 🔹 Slot Testing
- Accessed staging slot URL
- Validated application behavior before production swap

---

### 🔹 Slot Swap
- Swapped staging → production
- Verified production deployment

---

### 🔹 Issue Encountered
- Application failed with HTTP 500 error

---

### 🔹 Troubleshooting
- Checked logs
- Identified runtime mismatch
- Found application built on .NET 6
- Azure App Service runtime was newer (.NET 8)

---

### 🔹 Resolution
- Adjusted deployment approach
- Ensured runtime compatibility
- Removed dependency causing failure

---

## 🔄 Changes from Original Lab

### 🔹 Region
- East US → Central India

### 🔹 UI Navigation
- Configuration → Environment Variables (Azure UI update)

### 🔹 Application Source
- Original DB-based app replaced with simplified version

### 🔹 Runtime (CRITICAL)
- Lab: .NET 6  
- Actual: .NET 8 (App Service default)

---

## ❌ Issues Faced
- HTTP 500 error after deployment
- Runtime incompatibility (.NET version mismatch)
- Application dependency failure (DB config)

---

## ✅ Fix / Solution
- Identified runtime mismatch
- Adjusted deployment approach
- Simplified application
- Ensured compatibility with App Service runtime

---

## 💻 Commands Used
(To be updated if CLI used)

---

## 🌐 Application URL
(To be added)

---

## 📚 Learnings
- Deployment slots concept (staging → production)
- Zero downtime deployment using slot swap
- Importance of runtime compatibility
- Debugging HTTP 500 errors in App Service

---

## 🧠 Real DevOps Insight
Handled real-world production issue:

- Runtime mismatch (.NET 6 vs .NET 8)
- Application dependency failure
- Used logs + debugging for root cause analysis

---

## 📊 Change Log Summary

| Component | Lab Value | Your Value | Reason |
|----------|----------|-----------|--------|
| Region | East US | Central India | Latency + availability |
| UI | Configuration | Environment Variables | Azure UI update |
| App | DB-based | Simplified | Avoid failure |
| Runtime | .NET 6 | .NET 8 | Compatibility |

---

## 💥 Interview Answer
During execution, we faced a .NET runtime mismatch issue causing HTTP 500. We resolved it by adjusting deployment approach and ensuring runtime compatibility.
