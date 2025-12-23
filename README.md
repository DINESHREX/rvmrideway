RVM Rideway

A production-ready cab booking MVP built with Next.js App Router and Firebase

RVM Rideway is a scalable cab booking MVP designed to handle airport, outstation, and rental bookings with a clean user experience and a backend-ready architecture. The project focuses on server-side validation, structured data storage, and extensibility for real-world production use.

Live Demo

🔗 https://rvm-rideway-mvp.vercel.app/

Problem Statement

Many local and regional cab services rely on manual booking processes or outdated systems, leading to delayed confirmations, lack of transparency, and poor scalability.
RVM Rideway addresses this gap by providing a modern, automated booking workflow that can be extended with payments, notifications, and distance-based pricing.

✨ Key Features

🚖 Airport, Outstation, and Rental booking flows

🔐 Secure server-side booking validation

🗄 Firestore-backed persistent booking storage

💰 Rough fare estimation logic

🧩 Modular architecture using Next.js App Router

⚡ Fast API responses using Firebase Admin SDK

🏗 Tech Stack

Frontend

Next.js 14 (App Router)

React

CSS Modules / Global styles

Backend

Next.js API Routes

Firebase Admin SDK

Database

Firebase Firestore

Planned Integrations

Authentication (Admin / Customer)

Payments (Stripe / Razorpay)

Notifications (WhatsApp & Email)

Distance-based pricing (Google Distance Matrix API)

📁 Project Structure
├── app/            # Next.js App Router pages and API routes
├── components/     # Reusable UI components
├── lib/            # Firebase admin config and utilities
├── models/         # Data models and interfaces
├── public/         # Static assets
├── scripts/        # Utility and deployment scripts
├── middleware.js   # Request middleware
├── .env.example    # Environment variable template
└── README.md

⚙️ Environment Variables

Create a .env.local file based on .env.example.

Variable	Description
FIREBASE_PROJECT_ID	Firebase project ID
FIREBASE_CLIENT_EMAIL	Firebase service account email
FIREBASE_PRIVATE_KEY	Firebase private key (escaped with \n)

⚠️ Important: Replace actual line breaks in the Firebase private key with \n.

🧪 API Documentation
POST /api/bookings

Creates a new cab booking and stores it in Firestore.

Request Body

{
  "name": "John Doe",
  "phone": "9876543210",
  "pickup": "Chennai Airport",
  "drop": "T Nagar",
  "tripType": "Airport"
}


Response

{
  "bookingId": "RVM-1042",
  "estimatedFare": 2450,
  "status": "confirmed"
}

🛠 Local Development Setup
Prerequisites

Node.js >= 18

Firebase project with Firestore enabled

Firebase Service Account JSON key

Installation
git clone https://github.com/DINESHREX/rvmrideway.git
cd rvmrideway
cp .env.example .env.local
npm install
npm run dev


Open http://localhost:3000

🚧 Roadmap

WhatsApp & Email booking confirmations

Online payments (Stripe / Razorpay)

Distance-based dynamic fare calculation

Admin dashboard for booking management

Authentication & role-based access

📌 Use Cases

Cab & taxi service startups

Local transport businesses

Ride booking MVPs for rapid validation

Backend/API learning reference for Next.js + Firebase

👨‍💻 Author

Dinesh Kumar S
Founder – Radi Tech
📌 Full-Stack Developer | AI & Web Solutions
🔗 https://radi-tech.vercel.app

📄 License

This project is licensed under the MIT License.
