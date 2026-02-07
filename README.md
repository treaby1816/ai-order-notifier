# 📦 AI Order Notifier (Telegram/SMS)

![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)
![Role](https://img.shields.io/badge/Role-AI_Automation_Expert-purple?style=for-the-badge)
![Tech](https://img.shields.io/badge/Tech-n8n_|_Twilio_|_Telegram_API-yellow?style=for-the-badge)

## 📋 Executive Summary
An intelligent logistics engine architected by **Adewole Felix Bamidele**. This system solves the problem of "missed orders" by using an AI brain to instantly classify incoming orders and route high-priority alerts to warehouse staff via **Telegram** and **SMS**.

## ⚡ Automation Architecture

```mermaid
graph LR
    A["New Order (Shopify/Woo)"] -->|Webhook| B("n8n Controller")
    B -->|"Extract Details"| C{"AI Priority Classifier"}
    C -->|"High Value / Rush"| D["🚨 Trigger Urgent Alert"]
    C -->|Standard| E["Log to Spreadsheet"]
    
    D -->|"API Call"| F["Telegram Group: 'Warehouse Ops'"]
    D -->|"API Call"| G["Twilio SMS: Logistics Manager"]


