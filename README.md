# JobFlow – Full Stack Job Application Tracker

A production-style full-stack web application for tracking job applications, interview stages, and application progress with secure authentication and modern deployment practices.

---

## Features

### Authentication & Security
- User Registration & Login
- JWT-based Authentication
- Protected API Routes
- Password Hashing using bcrypt
- OAuth2 Password Flow

### Job Application Management
- Add Job Applications
- Track Application Status
- Store Applied Dates & Notes
- User-specific Application Data
- Update Application Progress

### Frontend
- Responsive UI built with React + TypeScript
- Protected Frontend Routes
- API Integration using Axios
- Modal-based Application Creation
- Component-Based Architecture

### Backend
- RESTful API Architecture using FastAPI
- SQLAlchemy ORM Integration
- PostgreSQL Database Management
- Alembic Database Migrations
- Dependency Injection with FastAPI

### Deployment & DevOps
- Dockerized Backend
- Environment Variable Management
- Frontend deployed on Vercel
- Backend deployed on Render

---

## Tech Stack

### Backend
- Python
- FastAPI
- SQLAlchemy
- Alembic
- PostgreSQL
- JWT Authentication
- OAuth2
- bcrypt

### Frontend
- React
- TypeScript
- Vite
- Axios
- React Router

### DevOps & Deployment
- Docker
- Render
- Vercel

---

## Project Structure

```bash
backend/
│
├── app/
│   ├── models/
│   ├── routers/
│   ├── schemas/
│   ├── security.py
│   ├── database.py
│   └── main.py
│
├── alembic/
│
└── requirements.txt

frontend/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── context/
│   ├── api/
│   └── assets/
│
└── package.json
```

---

## Authentication Flow

1. User registers with email and password
2. Password is securely hashed using bcrypt
3. User logs in using OAuth2 password flow
4. Backend generates JWT access token
5. Frontend stores token and sends it with protected API requests
6. Protected routes validate JWT before granting access

---

## Database Design

### Users Table
- id
- full_name
- email
- hashed_password
- created_at

### Applications Table
- id
- user_id
- company
- role
- status
- applied_date
- notes
- created_at

---

## Installation & Setup

### Clone Repository

```bash
git clone <your-repo-link>
cd jobflow
```

---

## Backend Setup

### Create Virtual Environment

```bash
python -m venv .venv
```

### Activate Virtual Environment

#### Windows

```bash
.venv\Scripts\activate
```

#### Mac/Linux

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Backend Server

```bash
uvicorn backend.app.main:app --reload
```

Backend runs on:

```bash
http://localhost:8000
```

---

## Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Frontend runs on:

```bash
http://localhost:5173
```

---

## Docker Setup

### Build Docker Image

```bash
docker build -t jobflow .
```

### Run Docker Container

```bash
docker run -p 8080:8080 jobflow
```

---

## API Endpoints

### Authentication

| Method | Endpoint | Description |
|---|---|---|
| POST | `/register` | Register User |
| POST | `/login` | Login User |
| GET | `/me` | Get Current User |

### Applications

| Method | Endpoint | Description |
|---|---|---|
| POST | `/applications` | Create Application |
| GET | `/applications` | Get User Applications |
| PATCH | `/applications/{id}` | Update Status |
| DELETE | `/applications/{id}` | Delete Application |

---

## Deployment

### Frontend
Deployed using Vercel

### Backend
Deployed using Render

---

## What I Learned

- Building RESTful APIs using FastAPI
- JWT Authentication & Authorization
- Database Design & ORM Relationships
- Alembic Database Migrations
- Frontend-Backend Integration
- Protected Routing in React
- Dockerization & Deployment
- Environment Variable Management
- Full Stack Application Architecture

---

## Future Improvements

- Refresh Tokens
- Redis Token Blacklisting
- Search & Filtering
- Pagination
- CI/CD Pipeline
- GitHub Actions
- Role-Based Access Control
- Analytics Dashboard
- Email Notifications
- Unit & Integration Testing

---

## Author

Anikait Bansal
