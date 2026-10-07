# Interview AI

An AI-powered interview preparation platform that analyzes your resume against a job description and generates a personalized interview report, practice questions, skill gap analysis, and a tailored resume PDF.

## Features

- **AI Interview Report** – Generates technical & behavioral questions, match score, and skill gaps using Google Gemini
- **Preparation Plan** – Day-wise study plan customized to the job role
- **Resume Builder** – AI-tailored, ATS-friendly resume generated as a downloadable PDF
- **Secure Auth** – JWT-based authentication with token blacklisting on logout

## Tech Stack

### Backend
- Node.js + Express 5
- MongoDB + Mongoose
- Google GenAI (Gemini)
- Puppeteer (PDF generation)
- pdf-parse, multer, bcryptjs, JWT, Zod

### Frontend
- React 19 + Vite
- React Router v7
- SCSS (feature-scoped styles)
- Axios

## Getting Started

### Prerequisites
- Node.js >= 18
- MongoDB instance (local or Atlas)
- Google GenAI API key

### Backend Setup
```bash
cd Backend
npm install
# Create a .env file with:
# MONGODB_URI=your_mongo_uri
# JWT_SECRET=your_jwt_secret
# GOOGLE_GENAI_API_KEY=your_api_key
npm run dev
```

### Frontend Setup
```bash
cd Frontend
npm install
npm run dev
```

The frontend runs on `http://localhost:5173` and the backend on `http://localhost:3000`.

## Project Structure

```
interview-ai/
+-- Backend/
¦   +-- server.js
¦   +-- src/
¦       +-- app.js
¦       +-- config/        # DB connection
¦       +-- controllers/   # Auth & Interview logic
¦       +-- middlewares/   # JWT auth, file upload
¦       +-- models/        # Mongoose schemas
¦       +-- routes/        # API route definitions
¦       +-- services/      # AI & PDF generation
+-- Frontend/
    +-- src/
        +-- features/
            +-- auth/      # Login, Register, Protected routes
            +-- interview/ # Home, Report pages, context
```

## Author

**Sohil Sharma** – [github.com/sohilsharma0910](https://github.com/sohilsharma0910)

