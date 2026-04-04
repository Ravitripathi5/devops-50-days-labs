# 📘 Lab 05A - Azure Function HTTP Trigger API

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Create a serverless API using Azure Functions with HTTP trigger, monitoring, and testing

---

## ⚙️ Steps Performed

### 🔹 Step 1: Login
- Authenticated Azure CLI using az login

---

### 🔹 Step 2: Resource Group
- Created → rg-functions-lab-prod (Central India)

---

### 🔹 Step 3: Storage Account
- Created → stfunctionslabprod24
- SKU → Standard_LRS

---

### 🔹 Step 4: Function App
- Name → func-api-lab-prod-24
- Runtime → Node.js 20
- OS → Linux
- Plan → Consumption

---

### 🔹 Step 5: Application Insights
- Created → appi-functions-lab-prod
- Linked with Function App

---

### 🔹 Step 6: Function Creation (UI)
- Created HTTP Trigger → UserInfoAPI

---

### 🔹 Step 7: Function Code
```javascript
module.exports = async function (context, req) {
    const name = (req.query.name || (req.body && req.body.name)) || 'Anonymous';
    const department = (req.query.department || (req.body && req.body.department)) || 'General';

    context.res = {
        status: 200,
        body: {
            status: "success",
            message: `Hello ${name} from ${department}`
        }
    };
};

🔹 Step 8: Testing (GET)
curl -X POST \
  "https://func-api-lab-prod-24.azurewebsites.net/api/UserInfoAPI" \
  -H "Content-Type: application/json" \
  -d "{\"name\":\"Ravi\",\"department\":\"DevOps\"}"

🔹 Step 9: Testing (POST)
curl -X POST \
  "https://func-api-lab-prod-24.azurewebsites.net/api/UserInfoAPI" \
  -H "Content-Type: application/json" \
  -d "{\"name\":\"Ravi\",\"department\":\"DevOps\"}"

  Changes from Original Lab
Component	Lab Value	Your Value	Reason
Region	East US 2	Central India	Better latency
Runtime	Node 18	Node 20	Node 18 EOL
Security	Not mentioned	TLS 1.2	Azure default
Monitoring	Instrumentation Key	Connection String	Modern approach
API Response	Basic	Structured JSON	Real-world API
Testing	Basic	GET + POST	Better validation
