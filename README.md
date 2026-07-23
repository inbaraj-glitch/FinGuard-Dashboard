# FinGuard AI -  Next Generation Personal Finance Intelligence

![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?logo=fastapi&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?logo=mysql&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Machine%20Learning-F7931E?logo=scikitlearn&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Deployment-2496ED?logo=docker&logoColor=white)
![Status](https://img.shields.io/badge/Status-In%20Development-yellow)

**FinGuard AI** is a secure, AI-powered personal finance analytics platform that helps users understand, manage, and improve their financial health.

The system securely accepts bank statements in PDF, scanned PDF, Excel, or CSV format and also supports manual transaction entry. It extracts and categorizes transactions, analyzes spending behaviour, predicts future expenses and month-end balance, detects unusual spending, generates personalized savings plans, calculates a Financial Health Score, and delivers risk-based alerts.

> This project is developed for academic, research, and educational purposes. Investment-related content is informational only and must not be treated as professional financial advice.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [System Modules](#system-modules)
- [System Workflow](#system-workflow)
- [Technology Stack](#technology-stack)
- [System Architecture](#system-architecture)
- [Machine Learning Features](#machine-learning-features)
- [Financial Health Score](#financial-health-score)
- [Risk-Based Notifications](#risk-based-notifications)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Environment Configuration](#environment-configuration)
- [Running the Application](#running-the-application)
- [API Documentation](#api-documentation)
- [Main API Endpoints](#main-api-endpoints)
- [Security Implementation](#security-implementation)
- [Dashboard and Charts](#dashboard-and-charts)
- [Future Enhancements](#future-enhancements)
- [Disclaimer](#disclaimer)
- [Author](#author)

---

## Project Overview

Many individuals do not maintain a clear record of their income, expenses, bills, savings, and investments. Bank statements contain useful financial information, but manually reviewing and categorizing transactions is time-consuming and error-prone.

FinGuard AI converts raw bank statement data into meaningful financial insights. It combines secure file processing, data analytics, machine learning, interactive dashboards, financial scoring, and automated alerts in a single platform.

The system is designed to help users:

- Track income and expenses
- Understand category-wise spending
- Detect overspending and unusual transactions
- Forecast future expenses and month-end balance
- Create budgets and savings goals
- Improve their financial habits
- Learn about government-backed and market-based investment options

---

## Problem Statement

Personal financial data is often distributed across bank statements, payment applications, spreadsheets, and handwritten records. Most users find it difficult to identify spending patterns, monitor budgets, predict future cash flow, and make informed savings decisions.

Existing expense trackers mainly record transactions but may not provide secure bank statement processing, predictive analytics, financial behaviour analysis, personalized savings recommendations, or privacy-focused risk alerts.

FinGuard AI addresses this problem by providing a secure and intelligent platform that automatically processes bank statements, analyzes financial behaviour, predicts future financial conditions, and provides actionable recommendations.

---

## Objectives

1. Securely collect bank statements and manually entered transactions.
2. Extract transaction data from PDF, scanned PDF, Excel, and CSV files.
3. Automatically classify transactions into financial categories.
4. Analyze monthly income, expenses, savings, and cash flow.
5. Detect overspending and unusual transaction behaviour.
6. Predict future expenses and month-end account balance.
7. Generate personalized budgets and savings plans.
8. Calculate a Financial Health Score between 0 and 100.
9. Send privacy-aware financial alerts and bill reminders.
10. Provide educational information about investment options.

---

## Key Features

### User Features

- Secure registration and login
- Bank statement upload
- Manual income and expense entry
- Transaction editing and categorization
- Budget planning
- Savings goal management
- Bill and EMI reminders
- Financial Health Score
- Monthly financial report

### Analytics Features

- Monthly spending trends
- Category-wise expense analysis
- Income versus expense comparison
- Savings rate analysis
- Budget versus actual spending
- Recurring expense identification
- Overspending detection
- Cash-flow forecasting
- Financial risk alerts

### AI Features

- Smart budget recommendations
- Future expense prediction
- Month-end balance forecasting
- Personalized saving suggestions
- Unusual spending detection
- Financial behaviour analysis
- Risk classification

### Security Features

- AES-256-GCM file encryption
- Argon2 password hashing
- JWT authentication
- HttpOnly cookies
- Data masking
- File validation
- Role-based access control
- Audit logging
- Secure temporary file removal

---

## System Modules

The application is divided into five major modules.

### 1. User Security and Privacy Management

Handles user registration, authentication, authorization, password protection, encrypted file storage, data masking, consent, and audit logging.

### 2. Bank Statement and Transaction Management

Accepts PDF, scanned PDF, Excel, CSV, and manual entries. It extracts, validates, cleans, categorizes, edits, and stores financial transactions.

### 3. Financial Analytics and Visualization

Calculates income, expenses, savings, budget utilization, category-wise spending, recurring expenses, and cash flow. Results are displayed through interactive charts.

### 4. AI Prediction and Financial Intelligence

Uses machine learning to detect unusual spending, forecast expenses, predict month-end balance, classify financial behaviour, and generate budget and savings recommendations.

### 5. Financial Health, Alerts and Investment Learning

Calculates the Financial Health Score, assigns financial risk levels, sends reminders and notifications, tracks savings goals, and provides educational investment resources.

---

## System Workflow

```text
User Registration / Login
            |
            v
Argon2 Password Verification
            |
            v
JWT Authentication using HttpOnly Cookie
            |
            v
Bank Statement Upload or Manual Entry
            |
            v
File Type and Security Validation
            |
            v
AES-256-GCM Encryption
            |
            v
Statement Processing
    |---------------------------|
    | PDF      -> PyMuPDF       |
    | Excel    -> OpenPyXL      |
    | CSV      -> Pandas        |
    | Scanned  -> OCR + OpenCV  |
    |---------------------------|
            |
            v
Transaction Extraction
            |
            v
Data Cleaning and Validation
            |
            v
Automatic Expense Categorization
            |
            v
MySQL Database Storage
            |
            v
Financial Analytics
            |
            v
Machine Learning Processing
            |
            v
Predictions and Recommendations
            |
            v
Financial Health Score
            |
            v
Risk-Based Alerts and Dashboard
```

---

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML5, CSS3, JavaScript, Bootstrap 5 |
| Backend | Python with FastAPI |
| ASGI Server | Uvicorn |
| Database | MySQL |
| ORM | SQLAlchemy |
| Database Driver | PyMySQL or MySQL Connector |
| Database Migration | Alembic |
| Data Analysis | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| PDF Processing | PyMuPDF |
| Excel Processing | Pandas, OpenPyXL |
| CSV Processing | Pandas |
| OCR Processing | Tesseract OCR, OpenCV |
| Encryption | AES-256-GCM using Python Cryptography |
| Password Security | Argon2 |
| Authentication | JWT with HttpOnly Cookies |
| Charts | Plotly.js |
| Notifications | Firebase Cloud Messaging and Email |
| Background Tasks | Celery and Redis |
| Testing | Pytest, Postman |
| Deployment | Docker |
| Development Tools | VS Code, GitHub, Postman |

---

## System Architecture

```text
+-------------------------------------------------------+
|                  Frontend Application                 |
|       HTML5 | CSS3 | JavaScript | Bootstrap 5         |
+----------------------------+--------------------------+
                             |
                             | HTTPS / REST API
                             v
+-------------------------------------------------------+
|                    FastAPI Backend                    |
| Authentication | Upload | Analytics | ML | Alerts     |
+------------+---------------+---------------+----------+
             |               |               |
             v               v               v
+----------------+  +----------------+  +----------------+
| File Processing|  | Data Analytics |  | Background Jobs|
| PDF / OCR / CSV|  | Pandas / NumPy |  | Celery / Redis |
+----------------+  +----------------+  +----------------+
             |               |               |
             +---------------+---------------+
                             |
                             v
+-------------------------------------------------------+
|                      MySQL Database                   |
| Users | Transactions | Budgets | Goals | Alerts       |
+-------------------------------------------------------+
                             |
                             v
+-------------------------------------------------------+
|               Scikit-learn ML Models                  |
| Forecasting | Anomaly Detection | Classification      |
+-------------------------------------------------------+
```

---

## Machine Learning Features

### Unusual Spending Detection

Identifies transactions that significantly differ from the user's normal spending behaviour.

Possible input features include:

- Transaction amount
- Expense category
- Transaction frequency
- Payment mode
- Transaction time
- Average category spending
- Monthly income
- Recurring status

Recommended model:

```text
Isolation Forest
```

### Future Expense Prediction

Predicts future expenses using historical transaction patterns, recurring bills, EMI payments, salary dates, and category-wise spending.

Possible models:

```text
Linear Regression
Random Forest Regressor
Gradient Boosting Regressor
```

### Month-End Balance Prediction

```text
Predicted Month-End Balance
=
Current Balance
+ Expected Remaining Income
- Predicted Remaining Expenses
```

### Financial Behaviour Classification

Users may be classified as:

- Disciplined Saver
- Balanced Spender
- Irregular Spender
- High Spender
- Financially At-Risk User

### Smart Budget Recommendation

The recommendation engine generates category-wise budgets using income, historical expenses, savings goals, recurring payments, and risk level.

---

## Financial Health Score

The Financial Health Score ranges from **0 to 100**.

| Parameter | Weight |
|---|---:|
| Savings Rate | 25 |
| Spending Control | 20 |
| Budget Adherence | 15 |
| Debt and EMI Ratio | 15 |
| Emergency Fund | 15 |
| Investment Consistency | 10 |
| **Total** | **100** |

### Score Classification

| Score | Financial Status |
|---:|---|
| 80–100 | Excellent |
| 60–79 | Good |
| 40–59 | Needs Improvement |
| 0–39 | High Financial Risk |

### Savings Rate Formula

```text
Savings Rate = (Total Savings / Total Income) x 100
```

---

## Risk-Based Notifications

### High Risk

Examples:

- Negative predicted month-end balance
- Very low savings rate
- High EMI-to-income ratio
- Unusual high-value transaction
- Insufficient balance for an upcoming bill

Notification type:

```text
Silent and privacy-protected priority alert
```

### Medium Risk

Examples:

- Budget utilization above 80%
- Savings goal likely to be missed
- Increasing monthly expense trend

Notification type:

```text
Important warning notification
```

### Low Risk

Examples:

- Normal bill reminder
- Savings goal progress
- Monthly financial summary

Notification type:

```text
Standard notification
```

Sensitive values should not be displayed on the device lock screen.

---

## Dataset

The project can be developed and tested using synthetic financial data to avoid exposing real personal banking information.

The sample combined dataset contains:

- Synthetic users
- Bank-style transactions
- Income and expense categories
- Monthly budgets
- Savings goals
- Bill reminders
- Unusual spending labels
- Financial risk labels
- Raw data quality issues for cleaning practice

Recommended dataset file:

```text
data/FinGuard_All_In_One_Raw_Dataset.csv
```

Example transaction columns:

```text
transaction_id
user_id
transaction_date
description
transaction_type
category
amount
withdrawal_amount
deposit_amount
balance_after
payment_mode
merchant
is_recurring
is_unusual
risk_level
```

> Do not upload real bank statements, account numbers, card numbers, UPI IDs, addresses, phone numbers, or customer IDs to a public GitHub repository.

---

## Project Structure

```text
finguard-ai/
|
|-- app/
|   |-- main.py
|   |
|   |-- api/
|   |   |-- routes/
|   |       |-- auth.py
|   |       |-- users.py
|   |       |-- statements.py
|   |       |-- transactions.py
|   |       |-- budgets.py
|   |       |-- savings.py
|   |       |-- analytics.py
|   |       |-- predictions.py
|   |       |-- alerts.py
|   |       |-- investments.py
|   |
|   |-- core/
|   |   |-- config.py
|   |   |-- database.py
|   |   |-- security.py
|   |   |-- encryption.py
|   |
|   |-- models/
|   |   |-- user.py
|   |   |-- transaction.py
|   |   |-- budget.py
|   |   |-- savings_goal.py
|   |   |-- bill.py
|   |   |-- alert.py
|   |
|   |-- schemas/
|   |   |-- user.py
|   |   |-- transaction.py
|   |   |-- analytics.py
|   |   |-- prediction.py
|   |
|   |-- services/
|   |   |-- pdf_service.py
|   |   |-- excel_service.py
|   |   |-- csv_service.py
|   |   |-- ocr_service.py
|   |   |-- categorization_service.py
|   |   |-- analytics_service.py
|   |   |-- notification_service.py
|   |
|   |-- ml/
|   |   |-- preprocessing.py
|   |   |-- anomaly_model.py
|   |   |-- expense_forecast.py
|   |   |-- balance_prediction.py
|   |   |-- behaviour_classifier.py
|   |   |-- saved_models/
|   |
|   |-- tasks/
|   |   |-- celery_app.py
|   |   |-- reminder_tasks.py
|   |   |-- report_tasks.py
|   |
|   |-- templates/
|   |-- static/
|
|-- data/
|   |-- sample/
|
|-- migrations/
|-- tests/
|-- uploads/
|   |-- encrypted/
|
|-- .env.example
|-- .gitignore
|-- alembic.ini
|-- docker-compose.yml
|-- Dockerfile
|-- requirements.txt
|-- README.md
```

---

## Installation

### Prerequisites

Install the following software:

- Python 3.11 or above
- MySQL Server
- Redis Server
- Tesseract OCR
- Git
- Docker, optional

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/finguard-ai.git
cd finguard-ai
```

### 2. Create a Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### Linux or macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Create the MySQL Database

```sql
CREATE DATABASE finguard_db
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;
```

### 5. Configure Environment Variables

```bash
copy .env.example .env
```

Linux or macOS:

```bash
cp .env.example .env
```

Update the values inside the `.env` file.

### 6. Run Database Migrations

```bash
alembic upgrade head
```

---

## Environment Configuration

Create a `.env` file in the root directory.

```env
APP_NAME=FinGuard AI
APP_ENV=development
DEBUG=True

HOST=127.0.0.1
PORT=8000

DATABASE_URL=mysql+pymysql://root:your_password@localhost:3306/finguard_db

JWT_SECRET_KEY=replace_with_a_secure_random_value
JWT_ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30

ENCRYPTION_MASTER_KEY=replace_with_a_secure_base64_key

REDIS_URL=redis://localhost:6379/0

SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USERNAME=your_email@example.com
SMTP_PASSWORD=your_app_password

FIREBASE_CREDENTIALS_PATH=credentials/firebase-service-account.json

TESSERACT_CMD=C:/Program Files/Tesseract-OCR/tesseract.exe
```

> Never commit `.env`, encryption keys, passwords, Firebase credentials, real bank statements, or user financial data to GitHub.

---

## Running the Application

### Start the FastAPI Server

```bash
uvicorn app.main:app --reload
```

Application URL:

```text
http://127.0.0.1:8000
```

### Start Redis

```bash
redis-server
```

### Start the Celery Worker

```bash
celery -A app.tasks.celery_app worker --loglevel=info
```

### Start Scheduled Reminder Tasks

```bash
celery -A app.tasks.celery_app beat --loglevel=info
```

---

## API Documentation

FastAPI automatically provides interactive API documentation.

### Swagger UI

```text
http://127.0.0.1:8000/docs
```

### ReDoc

```text
http://127.0.0.1:8000/redoc
```

---

## Main API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/v1/auth/register` | Register a new user |
| POST | `/api/v1/auth/login` | Authenticate a user |
| POST | `/api/v1/auth/logout` | End the user session |
| POST | `/api/v1/statements/upload` | Upload a bank statement |
| POST | `/api/v1/transactions/manual` | Add a transaction manually |
| GET | `/api/v1/transactions` | Retrieve user transactions |
| PUT | `/api/v1/transactions/{id}` | Update a transaction |
| DELETE | `/api/v1/transactions/{id}` | Delete a transaction |
| GET | `/api/v1/analytics/summary` | Get financial summary |
| GET | `/api/v1/analytics/spending-trends` | Get monthly spending trends |
| GET | `/api/v1/analytics/category-analysis` | Get category-wise analysis |
| POST | `/api/v1/predictions/expenses` | Predict future expenses |
| GET | `/api/v1/predictions/month-end-balance` | Predict month-end balance |
| GET | `/api/v1/predictions/unusual-spending` | Detect unusual spending |
| GET | `/api/v1/health-score` | Get Financial Health Score |
| POST | `/api/v1/budgets` | Create or update a budget |
| POST | `/api/v1/savings-goals` | Create a savings goal |
| GET | `/api/v1/alerts` | Retrieve financial alerts |
| GET | `/api/v1/investment-learning` | Retrieve investment education |

---

## Security Implementation

### Password Security

Passwords are never stored as plain text. Argon2 is used to generate secure password hashes.

### Authentication

JWT access tokens are stored in HttpOnly cookies to reduce direct JavaScript access to authentication tokens.

Recommended cookie configuration:

```python
httponly=True
secure=True
samesite="lax"
```

### File Encryption

Uploaded bank statements are encrypted using AES-256-GCM before storage.

AES-GCM provides:

- Confidentiality
- Integrity verification
- Authentication of encrypted data

### Data Privacy

The system masks sensitive information such as:

```text
Account Number: XXXXXXXX4582
Card Number: XXXX-XXXX-XXXX-7845
UPI ID: userXXXX@bank
Transaction Reference: REFXXXX123
```

### File Validation

The application validates:

- File extension
- MIME type
- File size
- Duplicate file upload
- Corrupted file
- Password-protected PDF
- Unsupported statement structure

### Secure File Handling

Decrypted files should exist only during processing and must be removed immediately after extraction.

---

## Dashboard and Charts

Plotly.js is used to create interactive financial dashboards.

Recommended charts:

- Income versus Expense Bar Chart
- Category-wise Expense Pie Chart
- Monthly Spending Line Chart
- Budget versus Actual Chart
- Financial Health Score Gauge
- Savings Goal Progress Chart
- Risk-Level Distribution Chart
- Payment Mode Analysis
- Daily Spending Heatmap
- Predicted Month-End Balance Chart

Suggested dashboard cards:

```text
Total Income
Total Expense
Current Savings
Savings Rate
Predicted Month-End Balance
Financial Health Score
Unusual Transactions
Upcoming Bills
```

---

## Testing

Run the test suite using:

```bash
pytest
```

Run tests with coverage:

```bash
pytest --cov=app tests/
```

Recommended testing areas:

- Authentication
- JWT cookie validation
- File upload validation
- PDF and OCR extraction
- Transaction categorization
- Financial calculations
- ML model prediction
- Encryption and decryption
- Authorization
- API response validation

---

## Docker Deployment

Build the application:

```bash
docker compose build
```

Start all services:

```bash
docker compose up
```

Run in detached mode:

```bash
docker compose up -d
```

Stop services:

```bash
docker compose down
```

Docker Compose can manage:

- FastAPI application
- MySQL database
- Redis
- Celery worker
- Celery Beat

---

## Future Enhancements

- Multi-bank statement format support
- Tamil, Hindi, and multilingual interfaces
- Bank SMS and email transaction extraction
- Voice-based expense entry
- Mobile application
- Explainable AI recommendations
- Family finance management
- Shared household budgets
- Credit score education
- Emergency fund planning
- Real-time banking API integration with user consent
- Advanced fraud-risk screening
- Tax planning education
- Export reports to PDF and Excel

---

## Disclaimer

FinGuard AI is an educational personal finance analytics project.

- It does not provide certified financial advice.
- It does not guarantee investment returns.
- It should not automatically execute investments.
- Investment content must link to official or verified educational resources.
- Users must verify financial decisions with qualified professionals.
- Real banking credentials must never be collected or stored.
- Public demonstrations should use only synthetic or anonymized data.

---

## Author

**Inbaraj S**

An IT professional committed to developing innovative, data-driven solutions. Focused on continuous learning and delivering impactful technology projects.
---

## Acknowledgements

This project uses open-source technologies including FastAPI, Pandas, NumPy, Scikit-learn, PyMuPDF, OpenCV, Tesseract OCR, Plotly.js, SQLAlchemy, MySQL, Celery, Redis, and Docker.

---

## Project Status

```text
Current Status: Under Development
Project Type: AI + Data Analytics + FinTech + Cybersecurity
Primary Backend: FastAPI
Database: MySQL
```

---

<p align="center">
  Developed with Python, FastAPI, Data Analytics, Machine Learning, and Secure Financial Processing.
</p>
