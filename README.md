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


🛠️ Technical Know-How
1. Intelligent Routing (The "AI Brain")
The system doesn't just notify; it thinks. It analyzes the order value and shipping method. If an order is marked "Express Shipping" or exceeds $500, it bypasses the standard queue and triggers a "Red Alert" notification.

2. Multi-Channel Delivery
Built with redundancy in mind. Alerts are sent simultaneously to a Telegram Group (for the floor staff) and via Twilio SMS (for the manager), ensuring 100% deliverability even if one channel fails.

3. Payload Formatting
Engineered the API payload to parse raw JSON order data into a clean, human-readable message (e.g., "📦 URGENT: Order #1024 - 50x Units - Needs Packing ASAP").

Architected by: Adewole Felix Bamidele

AI Automation Expert & Solutions Architect
