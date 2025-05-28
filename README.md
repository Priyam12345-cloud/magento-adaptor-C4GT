# magento-adaptor
# 🛒 ONDC-Compliant Magento Adaptor

## 🔗 Overview

This repository contains a fully functional **ONDC-compliant adaptor for the Magento e-commerce platform**, developed under the **C4GT Bounty Program**. The adaptor allows seamless integration of Magento-based seller platforms with the **Open Network for Digital Commerce (ONDC)**, enabling features such as:

- ✅ Catalog synchronization  
- ✅ Order lifecycle management  
- ✅ Post-order fulfillment and complaints  
- ✅ Real-time API monitoring and admin interface  

> 📦 Built with Magento 2.x | 🌐 ONDC Protocol v1.2.5 | 🛠️ Tech Stack: PHP, XML, React.js (for frontend), Node.js (backend for API bridge)

---

## 🧠 Project Logic & Architecture

### 🔄 Architecture Diagram

![ONDC-Magento-Adaptor Architecture](./docs/ondc-magento-architecture.png)

### 🧩 Key Components

| Component          | Description |
|-------------------|-------------|
| `code/`           | Magento module code implementing ONDC request handlers |
| `design/`         | Admin interface design assets for seller dashboard |
| `etc/`            | Module config files: module.xml, di.xml, routes.xml |
| `bootstrap.php`   | Entry point for API mocking during local development |
| `deployment.yml`  | CI/CD workflow for validation & deployment |
| `README.md`       | Documentation |
| `.htaccess`       | Server configuration for module paths |

---

## 🔧 Features

### ✅ Full ONDC Protocol Support
- Discovery APIs
- Order Placement, Status, and Fulfillment
- Complaint Management (post-fulfillment)
- JSON ↔ XML bridge between ONDC spec & Magento APIs

### 📊 Seller Admin Dashboard
- Built with React.js
- Track real-time orders from ONDC
- Sync inventory and prices
- View complaints, delivery status, and logs

### 🔐 Secure & Scalable
- Input validation & request sanitization
- Logs for ONDC protocol flows
- Stateless design for scale

---

## 🚀 Getting Started

### 📦 Prerequisites

- Magento 2.4.x installed (`app/code/` available)
- PHP 7.4+
- MySQL / MariaDB
- Node.js for frontend dashboard

### ⚙️ Installation Steps

```bash
cd <your-magento-root>/app/code
git clone https://github.com/<your-username>/magento-adaptor-C4GT Ondc/Adaptor

# Enable module
php bin/magento module:enable Ondc_Adaptor
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento cache:flush
