# TaskFlow — Task Management Application

A full-stack task manager built for the Thiranex Task Management assignment.

## Features
- JWT user authentication and protected user-specific tasks
- Create, read, update and delete tasks
- Status, priority and due-date tracking
- Responsive dashboard with task statistics and filters
- MongoDB persistence through Mongoose
- Production deployment ready for Render + Vercel

## Stack
**Frontend:** React + Vite + CSS  
**Backend:** Node.js + Express  
**Database:** MongoDB Atlas  
**Auth:** JWT + bcrypt

## Local setup

### Backend
```bash
cd backend
npm install
```
Create `backend/.env`:
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_long_random_secret
CORS_ORIGIN=http://localhost:5173
PORT=5000
```
Then run:
```bash
npm start
```

### Frontend
```bash
cd frontend
npm install
```
Create `frontend/.env`:
```env
VITE_API_URL=http://localhost:5000
```
Then run:
```bash
npm run dev
```

## Deployment
- Deploy `backend` as a Render Web Service with `npm install` / `npm start`.
- Add `MONGODB_URI`, `JWT_SECRET` and `CORS_ORIGIN` in Render environment variables.
- Deploy `frontend` as a Vercel Vite project with root directory `frontend`.
- Add `VITE_API_URL` pointing to the Render backend URL.

Never commit `.env` files or database credentials.
