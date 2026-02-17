# HMX Store

Modern Firebase-powered web application distribution platform with authentication, dynamic routing, real-time database integration, and analytics tracking.

---

## Overview

HMX Store is a responsive, single-page web application built using Vanilla JavaScript (ES Modules) and Firebase services.  

It provides a structured system for authenticated users to browse applications, view metadata, and initiate secure external downloads while maintaining real-time analytics and user tracking.

This project demonstrates clean modular architecture, Firebase integration, and production-style frontend structure without using frameworks.

---

## Key Features

### 🔐 Authentication System
- Email & password login
- Account registration
- Password reset via email
- Auth state persistence
- Automatic profile initialization
- Member since metadata tracking

### 📦 App Discovery System
- Real-time app listing from Firebase Realtime Database
- Category-based filtering
- Live search functionality
- Published-status rendering control
- Responsive grid layout

### 📄 App Details View
- Version display
- Download count tracking
- Last updated timestamp
- Dynamic description rendering
- External download confirmation modal

### 📊 Analytics & Data Integrity
- Atomic download counter using Firebase transactions
- User login tracking (createdAt / lastLogin)
- Real-time database synchronization
- Immediate UI update after download

### 🎨 UI / UX System
- SPA-style routing (without frameworks)
- Animated transitions
- Dark / Light mode with localStorage persistence
- 3D card component design
- Toast notification system
- Modal interaction system
- Responsive layout

---

## Tech Stack

**Frontend**
- HTML5
- CSS (Custom design system with variables)
- Vanilla JavaScript (ES Modules)

**Backend Services**
- Firebase Authentication
- Firebase Realtime Database

**Architecture Pattern**
- Centralized state object
- Modular separation:
  - UI Manager
  - Router
  - Auth Manager
  - Data Manager
  - Render Layer

---

## Project Architecture

```
index.html
│
├── UI Components
├── Router System
├── Authentication Manager
├── Data Manager
├── Render Layer
└── Firebase Integration
```

The system uses a centralized `state` object to manage application data and user context.

---

## Database Structure (Example)

```
apps/
  appId/
    name
    category
    version
    description
    icon
    downloadLink
    status: "published"
    downloadCount
    lastUpdated

users/
  uid/
    email
    createdAt
    lastLogin
```

---

## Installation & Setup

1. Clone the repository
2. Replace the Firebase configuration with your own project credentials
3. Enable Email/Password authentication in Firebase
4. Configure the Realtime Database structure
5. Deploy using:
   - Firebase Hosting
   - Netlify
   - Any static hosting provider

---

## Security Considerations

- Only apps marked as `"published"` are rendered
- Download links are externally hosted
- Download counters use atomic transactions
- Authentication is required before dashboard access
- Auth state is enforced before rendering protected views

---

## Future Improvements

- Admin dashboard for app management
- Role-based access control
- File storage integration
- Download verification tokens
- Advanced analytics dashboard
- Payment integration for paid distribution
- Server-side validation layer

---

## What This Project Demonstrates

- Full Firebase integration
- Modular frontend architecture
- SPA routing without frameworks
- Real-time state synchronization
- Clean UI component structure
- Scalable app distribution logic

---

## License

This project is for educational and demonstration purposes.
