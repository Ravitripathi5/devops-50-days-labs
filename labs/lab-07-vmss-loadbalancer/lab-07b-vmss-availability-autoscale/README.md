# 📘 Lab 07B - VMSS Availability Zones & Autoscale Setup

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Deploy VMSS across Availability Zones and configure autoscaling for high availability

---

## ⚙️ Steps Performed

### 🔹 VMSS Deployment
- Created VM Scale Set
- Selected VM Size → Standard_D2s_v3
- Configured Availability Zones → 1, 3

---

### 🔹 Autoscale Configuration
- Enabled autoscaling
- Defined scaling rules (CPU-based)
- Configured min/max instances

---

### 🔹 Validation
- Verified VM instances across zones
- Tested scaling behavior

---

## 🔄 Changes from Original Lab

| Component | Lab Value | Your Value | Reason |
|----------|----------|-----------|--------|
| Region | East US 2 | Central India | Latency optimization |
| AZ | 1,2,3 | 1,3 | VM size limitation |
| VM Size | Standard_B2s | Standard_D2s_v3 | Availability + performance |

---

## ❌ Issues Faced
- VM size not supported in all zones

---

## ✅ Fix / Solution
- Selected supported Availability Zones (1,3)
- Validated VM SKU compatibility

---

## 💻 Commands Used
(To be updated if CLI used)

---

## 📚 Learnings
- Availability Zones in Azure
- High availability design
- Autoscaling configuration

---

## 🧠 Real DevOps Insight
Handled real-world constraint:

- VM SKU not supported across all AZs  
- Adjusted architecture accordingly

---

## 💥 Interview Answer
Adjusted Availability Zones based on VM size compatibility and implemented autoscaling for high availability.
