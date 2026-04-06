# 📘 Lab 07A - VMSS + Load Balancer Setup

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Deploy Azure VM Scale Set (VMSS) with Load Balancer and ensure proper traffic distribution across instances

---

## ⚙️ Steps Performed

### 🔹 VMSS Deployment
- Created Virtual Machine Scale Set
- Selected VM size → Standard_D2s_v3
- Configured instances

---

### 🔹 Load Balancer Setup
- Created Load Balancer
- Configured frontend IP
- Added backend pool (VMSS instances)

---

### 🔹 Health Probe
- Created Health Probe (Port 80)
- Configured probe for backend health monitoring

---

### 🔹 Load Balancing Rule
- Created rule to distribute traffic
- Linked frontend → backend pool

---

### 🔹 Web Server Setup
- Custom data script failed
- Installed nginx manually using Run Command

---

### 🔹 Validation
- Accessed Load Balancer public IP
- Verified traffic distribution across VMSS instances

---

## 🔄 Changes from Original Lab

| Component | Lab Value | Your Value | Reason |
|----------|----------|-----------|--------|
| Region | East US 2 | Central India | Latency optimization |
| VM Size | Standard_B2s | Standard_D2s_v3 | Availability + performance |
| Nginx Setup | Custom Data Script | Manual install | Script failure |
| Network Design | Public VM access | Load Balancer access | Secure architecture |
| Load Balancer Config | Not detailed | Added Rules + Probe | Required for traffic |

---

## ❌ Issues Faced
- Custom data script failed during VMSS provisioning
- Backend instances unhealthy initially

---

## ✅ Fix / Solution
- Used Run Command to install nginx manually
- Configured Health Probe properly
- Added Load Balancing Rule

---

## 💻 Commands Used
```bash
sudo apt update
sudo apt install nginx -y
