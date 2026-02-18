# 🌧 Rain Water Tank Estimation – n8n Mini Project

## 📌 Overview

This mini project is an automated **Rainwater Harvesting Underground Tank Design & Estimation System** built using **n8n workflow automation**.

It collects user inputs, processes rainfall and water demand data, calculates tank dimensions, performs structural checks, estimates cost, and sends an automated design report via email.

---
## 🚀Workflow Diagram

flowchart TD

A[Form Submission] --> B[Geocode Location API]
B --> C[Fetch Wet Month Rainfall API]

A --> D[Get Consumption Data<br>from Google Sheets]
A --> E[Get Runoff Coefficient<br>from Google Sheets]

C --> F[Calculate Annual Rainfall]
D --> G[Calculate Water Demand]
E --> H[Get Runoff Coefficient]

F --> I[Merge Data]
G --> I
H --> I

I --> J[Design Volume Calculation]

J --> K[Calculate Tank Dimensions<br>(Length, Width, Depth)]

K --> L[Update Structural Design Sheet]

L --> M[Fetch Structural & Cost Data]

M --> N[Generate HTML Report]

N --> O[Send Email to User]


## 🛠 Technologies Used

| Technology | Category |
|------------|----------|
| n8n | Workflow Automation |
| Open-Meteo API | API Integration |
| Google Sheets API | for Design & Consumption Datas |
| JavaScript (Code Nodes) | Programming Logic |
| Gmail API | Email Automation |
| HTML & CSS | Report Generation |
| n8n Form Trigger | Webhook Trigger |
