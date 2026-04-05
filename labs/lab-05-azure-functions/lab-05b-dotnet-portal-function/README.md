# 📘 Lab 05B - Azure Function (.NET Portal-Based Deployment)

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Create an Azure Function using portal-based development with .NET runtime and validate execution

---

## ⚙️ Steps Performed

### 🔹 Resource Setup
- Created Resource Group → Central India
- Created Storage Account
- Created Function App:
  - OS → Windows
  - Plan → Consumption
  - Runtime → .NET

---

### 🔹 Function Creation
- Used “Develop in portal” option
- Created function via Azure Portal
- Template used → HTTP Trigger

---

### 🔹 Function Configuration
- Configured trigger settings
- Verified authorization level
- Updated function code using Code + Test section

---

### 🔹 Testing
- Used portal test feature
- Validated API response
- Checked execution logs

---

### 🔹 Monitoring
- Used Monitor tab
- Checked invocation logs
- Verified execution success

---

## 🔄 Changes from Original Lab

| Component | Lab Value | Your Value | Reason |
|----------|----------|-----------|--------|
| Region | East US | Central India | Latency optimization |
| Creation Method | Develop in portal | Same (with proper config) | Compatibility |
| Runtime | .NET 8 isolated | Portal-compatible runtime | Stability |
| UI Navigation | Old UI | Updated Azure UI | Portal update |

---

## ❌ Issues Faced
- Function creation not working initially
- Runtime mismatch confusion
- Portal UI differences

---

## ✅ Fix / Solution
- Selected Windows OS + Consumption plan
- Used portal-compatible runtime
- Followed updated Azure navigation

---

az group create \
  --name rg-functions-lab2 \
  --location centralindia
