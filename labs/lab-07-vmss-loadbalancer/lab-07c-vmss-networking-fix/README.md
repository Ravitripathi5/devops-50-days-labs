# 📘 Lab 07C - VMSS Networking & Connectivity Fix

## 📅 Date
05-Apr-2026

---

## 🎯 Objective
Fix networking issues in VMSS and ensure outbound connectivity for application setup

---

## ⚙️ Steps Performed

### 🔹 Initial Deployment
- Created VMSS with default networking
- Attempted package installation

---

### 🔹 Issue Encountered
- No internet connectivity in VM instances
- Unable to install packages (apt update failed)

---

### 🔹 Troubleshooting
- Checked NSG rules
- Verified subnet configuration
- Identified private subnet issue

---

### 🔹 Fix Implemented
- Disabled private subnet configuration
- Recreated VMSS with proper outbound access

---

### 🔹 Validation
- Verified internet connectivity
- Successfully installed packages

---

## 🔄 Changes from Original Lab

| Component | Lab Value | Your Value | Reason |
|----------|----------|-----------|--------|
| Region | East US 2 | Central India | Latency optimization |
| Networking | Default | Fixed outbound access | Connectivity issue |

---

## ❌ Issues Faced
- No outbound internet connectivity
- Package installation failure

---

## ✅ Fix / Solution
- Reconfigured networking
- Ensured outbound internet access
- Recreated VMSS

---

## 💻 Commands Used
```bash
sudo apt update
