# 🧾 Digital Receipt Microservice + API Gateway

This project is part of a scalable microservices architecture for generating and managing digital receipts with PDF and QR code support.

---

## 📦 Folder Structure

API-GATEWAY/
├── receipt-gateway/ # Express Gateway configuration
├── receipt-service/ # Receipt generation microservice
├── .gitignore
└── README.md

## 📍 Services

### 1. `receipt-service` (Microservice)

-Generates digital receipt PDFs with a QR code

- Input: `customerName`, `items`, `totalAmount`
- Output: PDF file with embedded QR code

Run:

```bash
cd receipt-service
npm install
node receipt-service.js

2. receipt-gateway (Express Gateway)
Controls access to microservices

Rate limits: 5 requests per minute

Routes: POST /v1/receipt

cd receipt-gateway
npm install
npm start

🔐 Features
✅ API Gateway routing and rate limiting

✅ Receipt schema validation

✅ QR code + PDF generation

✅ Clean folder structure

✅ Postman-friendly routes

🔗 Example Request
POST http://localhost:8080/v1/receipt

json
Copy
Edit
{
  "customerName": "Suraj",
  "items": ["USB Cable", "Notebook"],
  "totalAmount": 299.50
}


🚀 Future Plans
Add API Key auth via Express Gateway

Dockerize the services

Deploy to Railway/Render with CI/CD

## ✅ Final Steps

Now just run:

```bash
git add .
git commit -m "add .gitignore and README.md"
git push
