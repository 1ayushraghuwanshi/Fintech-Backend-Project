# Fintech-Backend-Project
🏦 Advanced Backend Project: Bank Transaction System
Node.js Express.js MongoDB JWT

A production-ready backend system simulating real-world bank operations built with Node.js, Express, and MongoDB. This project focuses on idempotency, ledger consistency, and secure transaction flows.

🛠️ Features
🔒 Secure Authentication: JWT-based user registration and login with password hashing (bcrypt).
💳 Account Management: Create and manage user accounts with secure balance checks.
💸 Transaction Processing: Secure money transfer between accounts with pending and completed states.
📚 Ledger Management: Double-entry bookkeeping system to ensure data consistency.
🛡️ Idempotency Validation: Prevents duplicate transaction processing.
📧 Email Notifications: Automated emails for registration and transaction success using nodemailer and Google OAuth.
📊 Data Integrity: MongoDB sessions and transactions for atomic operations.
🏗️ Technical Stack:

Language: JavaScript (Node.js)
Framework: Express.js
Database: MongoDB (using Mongoose)
Authentication: JSON Web Tokens (JWT)
Security: bcryptjs for password hashing, helmet for HTTP headers.
Service: nodemailer for email services.

📋 Prerequisites
Node.js (v16 or higher)
MongoDB account (Atlas recommended)
Google Mail account (for OAuth email services)
Postman (for API testing)

🚀 Installation and Setup
Clone the repository:
bash
git clone https://github.com/1ayushraghuwanshi/Fintech-Backend-Project.git
cd backend-ledger

Install dependencies:
bash
npm install
Email Configuration:-
EMAIL_USER=your_email@gmail.com
CLIENT_ID=your_google_client_id
CLIENT_SECRET=your_google_client_secret
REFRESH_TOKEN=your_google_refresh_token
Run the application:
bash
npm run dev

🧪 API Endpoints
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Login user and set JWT in cookie
POST	/api/account/create	Create a new bank account for user
POST	/api/transaction/transfer	Transfer money between accounts
GET	/api/account/balance	Fetch current account balance
