# 📘 Lab 05C - Azure Function (Python + Monitoring + Alerts)

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Deploy a Python-based Azure Function with proper dependency handling, monitoring, and alerting

---

## ⚙️ Steps Performed

### 🔹 Resource Setup
- Created Resource Group → Central India
- Created Storage Account
- Created Function App (Python 3.11)

---

### 🔹 Runtime Configuration
- Explicitly selected Python 3.11
- Avoided default Node.js runtime

---

### 🔹 Deployment
- Used Azure Portal + CLI
- Created function via UI
- Managed files using Kudu (Advanced Tools)

---

### 🔹 Dependency Management
- Created requirements.txt manually via Kudu
- Installed dependencies for Python function

---

### 🔹 Function Logic
- Implemented fallback logic (file copy instead of image resize)
- Maintained event-driven workflow

---

### 🔹 Monitoring Setup
- Enabled Application Insights
- Used Log Stream for real-time logs
- Verified invocation logs

---

### 🔹 Alert Configuration
- Configured email alert for function execution
- Enabled proactive monitoring

---

## 🔄 Changes from Original Lab

| Component | Lab Value | Your Value | Reason |
|----------|----------|-----------|--------|
| Region | East US | Central India | Performance |
| Runtime | Python 3.11 | Python 3.11 (manual) | UI default mismatch |
| Deployment | UI only | UI + CLI | Faster + DevOps approach |
| Editor | App Service Editor | Kudu | Deprecated |
| Dependencies | requirements.txt (UI) | Kudu-based | Required manual install |
| Logic | Pillow image resize | File copy fallback | Stability |
| Monitoring | Basic | Log Stream + App Insights | Observability |
| Alerts | Not included | Configured | Production readiness |

---

## ❌ Issues Faced
- Default runtime mismatch (Node.js shown)
- Dependency installation not working via portal
- Pillow library issues
- Old UI references not matching

---

## ✅ Fix / Solution
- Explicitly selected Python 3.11
- Used Kudu for dependency management
- Implemented fallback logic
- Used updated Azure UI navigation

---

## 💻 Commands Used
```bash
az login

az group create \
  --name rg-functions-lab3 \
  --location centralindia

az storage account create \
  --name stfunctionlab3 \
  --resource-group rg-functions-lab3 \
  --location centralindia \
  --sku Standard_LRS
