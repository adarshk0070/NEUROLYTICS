---
description: Repository Information Overview
alwaysApply: true
---

# Repository Information Overview

## Repository Summary
A comprehensive brain tumor detection system combining full-stack web development with machine learning. The application features user authentication, real-time chat, medical report management, and AI-powered MRI scan analysis for brain tumor detection.

## Repository Structure
The repository contains a main project directory "brain after review" with a subproject "brain-tumor-detection" that includes three interconnected components: a Node.js backend API, a React frontend, and a Python machine learning API.

### Main Repository Components
- **Backend**: Node.js/Express server managing authentication, database operations, file uploads, and real-time communication
- **Frontend**: React application providing user interfaces for patients, doctors, and administrators
- **ML-Model**: Python API serving a TensorFlow-based CNN model for brain tumor detection from MRI scans

## Projects

### Backend (Node.js API)
**Configuration File**: brain-tumor-detection/backend/package.json

#### Language & Runtime
**Language**: JavaScript
**Runtime**: Node.js
**Build System**: npm
**Package Manager**: npm

#### Dependencies
**Main Dependencies**:
- express (web framework)
- mongoose (MongoDB ODM)
- bcryptjs (password hashing)
- jsonwebtoken (JWT authentication)
- multer (file uploads)
- socket.io (real-time communication)
- cors (CORS handling)
- axios (HTTP client)
- nodemailer (email sending)

#### Build & Installation
```bash
cd brain-tumor-detection/backend
npm install
```

#### Testing
**Framework**: Jest
**Test Location**: __tests__/
**Naming Convention**: *.test.js
**Configuration**: jest.config.js
**Run Command**:
```bash
npm test
```

### Frontend (React Application)
**Configuration File**: brain-tumor-detection/frontend/package.json

#### Language & Runtime
**Language**: JavaScript
**Runtime**: Node.js
**Build System**: Vite
**Package Manager**: npm

#### Dependencies
**Main Dependencies**:
- react (UI framework)
- react-dom (DOM rendering)
- @tanstack/react-query (data fetching)
- axios (HTTP client)
- bootstrap (CSS framework)
- socket.io-client (real-time communication)
- framer-motion (animations)
- @google/generative-ai (AI integration)

#### Build & Installation
```bash
cd brain-tumor-detection/frontend
npm install
npm run build
```

#### Testing
**Framework**: Jest
**Test Location**: __tests__/
**Naming Convention**: *.test.js
**Configuration**: jest.config.js
**Run Command**:
```bash
npm test
```

### ML-Model (Python API)
**Configuration File**: brain-tumor-detection/ml-model/api/requirements.txt

#### Language & Runtime
**Language**: Python
**Runtime**: Python 3.x
**Build System**: pip
**Package Manager**: pip

#### Dependencies
**Main Dependencies**:
- fastapi (web framework)
- uvicorn (ASGI server)
- pillow (image processing)
- numpy (numerical computing)
- tensorflow (ML framework)
- h5py (HDF5 file handling)
- python-multipart (form data handling)

#### Build & Installation
```bash
cd brain-tumor-detection/ml-model/api
pip install -r requirements.txt
```

#### Testing
**Framework**: Python unittest
**Test Location**: test_model.py
**Run Command**:
```bash
python test_model.py
```