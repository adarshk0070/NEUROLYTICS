🧠 NEUROLYTICS – Brain Tumor Detection System

A full-stack AI-powered medical diagnosis system built with Node.js, React, MongoDB, and a Python ML Model for MRI-based Brain Tumor Classification.


📦 Prerequisites

Ensure you have installed:

Node.js 16+

npm / yarn

MongoDB 4+ (local or Atlas)

Python 3.8+

Git

VS Code (recommended)

Google OAuth credentials (optional)

🚀 Installation & Setup
1. Clone the Repository
git clone <repository-url>
cd brain-tumor-detection

2. Backend Setup
cd backend
npm install


Create .env file:

cat > .env << EOF
PORT=5000
MONGODB_URI=mongodb://localhost:27017/brain_tumor_db
JWT_SECRET=your_jwt_secret
NODE_ENV=development
ML_API_URL=http://localhost:5001
SMTP_USER=your_email@gmail.com
SMTP_PASSWORD=your_app_password
EOF


Start backend:

npm run dev


➡ Runs on http://localhost:5000

3. Frontend Setup
cd ../frontend
npm install


Create .env:

cat > .env << EOF
VITE_API_BASE_URL=http://localhost:5000
VITE_ML_API_URL=http://localhost:5001
EOF


Start frontend:

npm run dev


➡ Runs on http://localhost:5173

4. ML Model Setup
cd ../ml-model/api
python -m venv venv


Activate environment:

Windows

venv\Scripts\activate


Mac/Linux

source venv/bin/activate


Install dependencies:

pip install -r requirements.txt


Start ML server:

python app.py


➡ Runs on http://localhost:5001

⚡ Quick Start
Start all services (Windows)
start-all.bat

Start all services (Mac/Linux)
chmod +x start-all.sh
./start-all.sh

Manual Mode

Backend:

cd backend
npm run dev


Frontend:

cd frontend
npm run dev


ML Model:

cd ml-model/api
source venv/bin/activate
python app.py

🌐 Access the Application
Service	URL
Frontend	http://localhost:5173

Backend	http://localhost:5000

ML API	http://localhost:5001

API Docs (if enabled)	http://localhost:5000/api/docs
🔌 API Documentation (Short Overview)
Authentication
Method	Endpoint	Description
POST	/api/auth/register	Register user/doctor
POST	/api/auth/login	Login
POST	/api/auth/forgot-password	Password reset link
PUT	/api/auth/reset-password/:token	Reset password
User

Upload MRI: POST /api/user/scan

Get reports: GET /api/user/reports/:id

Doctor

Get patients: GET /api/doctor/patients

Add analysis: PUT /api/doctor/reports/:reportId

Admin

Approve doctor: PUT /api/admin/doctor-requests/:id/approve

Suspend doctor: PUT /api/admin/doctor/:id/suspend

ML Model

Predict tumor: POST /api/model/predict

Health check: /health

👥 User Roles & Workflows
Patient

✔ Upload MRI
✔ Get prediction
✔ View reports
✔ Chat with doctor

Doctor

✔ Manage patients
✔ Review scans
✔ Add expert opinion

Admin

✔ Approve doctors
✔ Monitor logs
✔ Manage system

🧪 Testing

Backend:

cd backend
npm test


Frontend:

cd frontend
npm test


ML:

cd ml-model
python test_model.py

🗄️ Database Schema (Simplified)
User
{
  "name": "String",
  "email": "String",
  "role": "user | doctor | admin",
  "medicalHistory": [],
  "isActive": true
}

Doctor
{
  "userId": "ObjectId",
  "license": "String",
  "specialization": "String",
  "status": "pending | approved | suspended"
}

Report
{
  "userId": "ObjectId",
  "imagePath": "String",
  "aiAnalysis": {
    "result": "Tumor Detected",
    "confidence": 95.5
  }
}

⚙️ Environment Configuration
Backend .env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/brain_tumor_db
JWT_SECRET=your_jwt_secret
ML_API_URL=http://localhost:5001
SMTP_USER=
SMTP_PASSWORD=

Frontend .env
VITE_API_BASE_URL=http://localhost:5000
VITE_ML_API_URL=http://localhost:5001

ML .env
API_PORT=5001
MODEL_PATH=../model/brain_tumor_model.h5

🔧 Troubleshooting (Quick Fixes)
Backend not starting?
mongod


Check MongoDB.

Frontend errors?
rm -rf node_modules
npm install

ML model not loading?
pip install -r requirements.txt

CORS error?

Ensure:

CORS_ORIGIN=http://localhost:5173

🤝 Contributing
git checkout -b feature/my-feature
git add .
git commit -m "Add: my feature"
git push origin feature/my-feature


Submit Pull Request.
