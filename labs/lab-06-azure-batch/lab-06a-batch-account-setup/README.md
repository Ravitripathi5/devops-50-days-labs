# 📘 Lab 06A - Azure Batch Account Setup

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Create and configure Azure Batch Account with compute pool and validate job execution setup

---

## ⚙️ Steps Performed

### 🔹 Resource Setup
- Created Resource Group → Central India
- Created Storage Account (same region)

---

### 🔹 Batch Account Setup
- Created Azure Batch Account
- Linked with Storage Account

---

### 🔹 Compute Pool Configuration
- Selected VM Size → Standard_D2s_v3
- Configured node pool
- Set node count → 1

---

### 🔹 Validation
- Verified pool creation
- Checked node status
- Ensured Batch account readiness

---

## 🔄 Changes from Original Lab

| Component | Lab Value | Your Value | Reason |
|----------|----------|-----------|--------|
| Region | East US | Central India | Latency optimization |
| Storage | East US | Central India | Same region dependency |
| VM Size | Standard_D2s_v3 | Same (validated) | Availability check |
| Node Count | 2 nodes | 1 node | Quota optimization |

---

## ❌ Issues Faced
- VM quota limitation
- Pool creation constraints

---

## ✅ Fix / Solution
- Reduced node count
- Validated VM size availability before creation

---

## 💻 Commands Used
(To be updated if CLI used)

---

## 📚 Learnings
- Azure Batch account architecture
- Compute pool configuration
- Importance of region alignment
- Handling quota limitations

---

## 🧠 Real DevOps Insight
Handled real-world constraint:

- VM quota limitation
- Resource alignment (Batch + Storage same region)

Optimized deployment for successful execution

---

## 🌐 Resources Created
- Batch Account
- Storage Account
- Compute Pool

---
