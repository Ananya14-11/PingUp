# PingUp

[![React](https://img.shields.io/badge/React-19.2-61DAFB?logo=react)](https://react.dev)
[![Express](https://img.shields.io/badge/Express-5.2-000000?logo=express)](https://expressjs.com)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb)](https://www.mongodb.com)
[![Clerk](https://img.shields.io/badge/Clerk-Auth-6C47FF)](https://clerk.com)
[![Vercel](https://img.shields.io/badge/Vercel-Deploy-000000?logo=vercel)](https://vercel.com)

**A modern, full-stack social media platform built with React, Express, and MongoDB.** Real-time messaging, ephemeral stories, smart automations, and professional-grade architecture.

**Live Demo:** [ping-up-smoky.vercel.app](https://ping-up-smoky.vercel.app)

---

## 🚀 Features

- **User Authentication & Profile Management** — Seamless Clerk integration with automatic DB sync
- **Social Feed** — Create and browse posts with text + multiple images
- **Ephemeral Stories** — 24-hour stories with automatic expiration via Inngest
- **Real-time Messaging** — Server-Sent Events (SSE) powered instant chat with image support
- **Connection System** — Send/accept connection requests with email reminders
- **Discover & Connections** — Find and manage your network
- **Image Uploads** — Optimized handling via ImageKit
- **Smart Automations** — Inngest-powered user sync, story deletion, and daily notifications
- **Responsive UI** — Modern Tailwind design with smooth interactions

---

## 🛠 Tech Stack

### Frontend
- **React 19** + Vite
- **Redux Toolkit** + React-Redux (centralized state)
- **React Router DOM** v7
- **Tailwind CSS** v4
- **Lucide React** icons
- **Axios** for API calls
- **React Hot Toast** notifications

### Backend
- **Express.js** (Node.js)
- **Mongoose** ODM
- **Clerk** (Auth middleware + webhooks via Inngest)
- **Inngest** (Serverless automations & workflows)
- **ImageKit** (Image optimization & CDN)
- **Multer** + custom upload logic
- **Nodemailer** (transactional emails)

### Database
- **MongoDB** with Mongoose schemas and population

### Authentication
- **Clerk** (frontend + Express middleware) with webhook sync to MongoDB

### Realtime Communication
- **Server-Sent Events (SSE)** for instant messaging

### State Management
- **Redux Toolkit** (slices for auth, posts, messages, UI)

### Deployment
- **Vercel** (Frontend + Serverless API routes)

---

## 📂 Folder Structure

```bash
PingUp/
├── client/                  # React Frontend
│   ├── src/
│   │   ├── components/      # Reusable UI components (PostCard, StoriesBar, etc.)
│   │   ├── features/        # Redux slices
│   │   ├── pages/           # Main views (Feed, Messages, Profile, ChatBox, etc.)
│   │   ├── api/             # Axios instances & API utilities
│   │   └── app/             # Redux store setup
│   ├── public/
│   └── vite.config.js
│
├── server/                  # Express Backend
│   ├── models/              # MongoDB Schemas (User, Post, Story, Message, Connection)
│   ├── controllers/         # Business logic
│   ├── routes/              # API route definitions
│   ├── middlewares/         # Auth protection, error handling
│   ├── configs/             # DB, ImageKit, Nodemailer
│   ├── inngest/             # Automation workflows
│   └── server.js
│
├── .gitignore
└── README.md
