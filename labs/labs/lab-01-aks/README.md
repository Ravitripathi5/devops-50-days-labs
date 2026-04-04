# 📘 Lab 01 - AKS Cluster Setup

## 📅 Date
04-Apr-2026

## 🎯 Objective
Deploy AKS cluster in Azure

## ⚙️ Steps Performed
- Created resource group
- Created AKS cluster
- Connected using kubectl

## 🔄 Changes from Original Lab
- Region changed to Central India

## ❌ Issues Faced
- Quota issue

## ✅ Fix / Solution
- Changed VM size

## 💻 Commands Used
```bash
az group create --name rg-aks --location centralindia
az aks create --resource-group rg-aks --name myaks --node-count 2
