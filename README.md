# HIGIMAC

**A professional cleaning and sanitization services platform.**

![license](https://img.shields.io/github/license/gabemaldito/higimac?style=flat-square&color=0080ff)
![repo-top-language](https://img.shields.io/github/languages/top/gabemaldito/higimac?style=flat-square&color=0080ff)
![last-commit](https://img.shields.io/github/last-commit/gabemaldito/higimac?style=flat-square&color=0080ff)

---

## 📖 Overview

**HIGIMAC** is a mobile application built with **React Native** and **Expo** designed to bridge the gap between cleaning professionals and clients. 

The project features a dual-interface architecture, providing tailored experiences for both service providers and customers within a single unified codebase.

---

## ✨ Key Features

* **Dual-Role Architecture**: Specialized workflows for **Clients** (booking/exploring) and **Professionals** (job management/earnings).
* **Authentication & Onboarding**: Complete user journey from registration to role-specific onboarding.
* **Service Management**: Real-time job tracking, calendars for professionals, and booking history for clients.
* **Centralized Design System**: Custom theme engine managing typography, spacing, and colors.
* **Secure Context API**: Global state management for user authentication and session persistence.

---

## 📂 Project Structure

```bashv
└── higimac/
    ├── app/                # Expo Router (File-based navigation)
    │   ├── (auth)          # Login, Signup, Onboarding
    │   ├── (client)        # Explore, Bookings, Messages, Profile
    │   └── (professional)  # Jobs, Earnings, Calendar, Pro-Profile
    ├── context/            # Global state (AuthContext.tsx)
    ├── src/components/     # Reusable UI components
    ├── theme/              # Design tokens (colors, layout, spacing, typography)
    └── hooks/              # Custom React hooks
```

## 🛠️ Tech Stack

Framework: React Native & Expo

Navigation: Expo Router

Language: TypeScript

State Management: React Context API

## 🎓 Learning Outcomes

This project taught me:
- **Dual-interface architecture**: Managing separate user flows (Client vs Professional) in a single codebase
- **State management at scale**: Using Context API for complex authentication and session persistence
- **Mobile-first design**: Building responsive layouts with React Native
- **Database design**: Modeling relationships for a two-sided marketplace (users, bookings, reviews)
- **Real-time features**: Implementing job tracking and notification systems


  ## 📱 Screenshots

<img width="371" height="794" alt="image" src="https://github.com/user-attachments/assets/32881a9a-f795-4536-9059-8e3861b83609" />
<img width="369" height="783" alt="image" src="https://github.com/user-attachments/assets/da08d6f9-a3cd-4191-aeb4-eae3bda00413" />
<img width="368" height="795" alt="image" src="https://github.com/user-attachments/assets/cc49c592-f1c4-4c3a-883c-e8a3deb5c305" />


## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Expo CLI
- Supabase account

### Installation
```bash
git clone https://github.com/gabemaldito/Hygi-cleaning-service.git
cd higimac
npm install
npx expo start
```

### Development
```bash
# iOS
i

# Android  
a
```

### Build for Production
```bash
eas build --platform all
```


## 🔧 Technical Challenges & Solutions

### Challenge 1: Dual-Role Navigation
**Problem**: Same app, two completely different user flows (Client vs Professional)
**Solution**: Used Expo Router's group-based routing with conditional rendering based on user role stored in AuthContext

### Challenge 2: Real-time Job Updates
**Problem**: Professionals need instant notifications when new jobs are available
**Solution**: Implemented polling + Supabase realtime subscriptions with efficient query caching

### Challenge 3: State Persistence Across App Restart
**Problem**: User session was lost when app closed
**Solution**: AsyncStorage + Context API hydration on app startup




## 📚 Lessons Learned

If I were to rebuild this project today, I would:
- Use **Redux Toolkit** instead of Context API for more predictable state management
- Implement **React Query** for better server state management
- Add **E2E testing** with Detox or Appium
- Structure components with **Compound Components pattern** for better composition
- Use **TypeScript stricter mode** (noUncheckedIndexedAccess, etc.)

