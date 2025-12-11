# anonymous-feedback-app
A secure, anonymous feedback platform built with Python (FastAPI)
Developed by Gamble Entertainment LLC

**Overview**: The Anonymous Staff Feedback Application allows employees and former staff to submit workplace feedback anonymously, while still ensuring the submission comes from a real member of the organization.

**The system is designed for**:

Healthcare & hospice organizations
Corporate teams
High-turnover industries needing honest feedback
Environments where staff fear retaliation
This repository contains the full Python backend API responsible for data handling, verification, and administrator tools.

**This repository contains**:

Python Backend API (FastAPI)
REST endpoints for feedback submission, admin management, and verification
Database integration
Authentication & token-based verification
Admin dashboard support (API side)

**Core Features**:

**Employee / Former Staff Interface**:

Submit feedback anonymously
Select feedback category (patient care, management, safety, workplace environment, etc.)

**Verification via**:

Employee ID,
Work email domain,
Organization-issued access token,
Optional file uploads,
Confirmation response upon successful submission

**Administrator Dashboard (API Ready)**

**Admin portal connects to this backend and allows**:

Secure admin login,
View and filter all submissions,
Export submissions (CSV/JSON),
Auto-flag keywords (e.g., compliance, harassment, patient safety),
Trend and sentiment analytics support

**Security & Compliance**:

100% anonymous (no stored personal identifiers),
HTTPS/SSL recommended for deployment,
Encrypted database fields,
HIPAA-level data handling patterns (for healthcare organizations),
Verification system decoupled from identity

| Layer             | Technology                                    |
| ----------------- | --------------------------------------------- |
| Backend Framework | **FastAPI (Python)**                          |
| Language          | Python 3.10+                                  |
| Database          | PostgreSQL (Supabase) or Firebase             |
| Storage           | AWS S3 / Supabase Storage                     |
| Auth              | JWT                                           |
| Hosting Options   | AWS, Fly.io, Render, Vercel Python Serverless |
| API Docs          | Swagger & ReDoc Auto-Docs                     |


#Getting Started (Local)
1. Clone the repository
git clone https://github.com/gerrenSmith/anonymous-feedback-app.git
cd anonymous-feedback-app/backend

2. Create a virtual environment
python3 -m venv venv
source venv/bin/activate

3. Install dependencies
pip install -r requirements.txt

4. Start the API
uvicorn app.main:app --reload

Environment Variables

Create a .env file:

DATABASE_URL=your_database_connection
JWT_SECRET=your_secret_key
AWS_ACCESS_KEY=your_key
AWS_SECRET_KEY=your_secret
STORAGE_BUCKET=your_bucket

**Core API Endpoints**
Submit Feedback

POST /feedback/submit

Verify Staff

POST /verify/check

Admin Login

POST /admin/login

View All Feedback

GET /admin/feedback

Export

GET /admin/export

**Developer**

Gamble Entertainment LLC

Developer: Gerren Smith Jr

GitHub: https://github.com/gerrenSmith

Email: gerrensmith32@gmail.com
