# GiftInn Musanze - Luxury Hotel Website

<p align="center">
  <img src="public/icons/giftinn-logo.svg" width="120" alt="GiftInn Logo" />
</p>

<p align="center">
  A premium, editorial-style hotel website for <strong>GiftInn Musanze</strong>, built with React + Vite.
  It combines luxury UI/UX, room discovery, booking flows, live notifications, and PWA-ready behavior.
</p>

<p align="center">
  <img alt="React" src="https://img.shields.io/badge/React-19-1f1a16?style=for-the-badge&logo=react&logoColor=61dafb" />
  <img alt="Vite" src="https://img.shields.io/badge/Vite-7-1f1a16?style=for-the-badge&logo=vite&logoColor=ffd62e" />
  <img alt="Tailwind" src="https://img.shields.io/badge/TailwindCSS-4-1f1a16?style=for-the-badge&logo=tailwindcss&logoColor=38bdf8" />
  <img alt="PWA" src="https://img.shields.io/badge/PWA-Enabled-1f1a16?style=for-the-badge&logo=pwa&logoColor=ffffff" />
</p>

---

## Table of Contents

1. [Overview](#overview)
2. [Design System](#design-system)
3. [Core Features](#core-features)
4. [Pages & User Flow](#pages--user-flow)
5. [Video Showcase](#video-showcase)
6. [Project Structure](#project-structure)
7. [Local Setup](#local-setup)
8. [PWA & Notifications](#pwa--notifications)
9. [Deployment Notes](#deployment-notes)
10. [Future Upgrades](#future-upgrades)

---

## Overview

GiftInn Musanze is designed as a modern boutique-hotel experience on the web.
The interface is intentionally editorial and luxurious, using warm gold accents, deep charcoal backgrounds, and a high-end serif/sans pairing to communicate trust and exclusivity.

### Goals

- Present the hotel as a premium destination in Musanze.
- Convert visitors to bookings with low-friction flows.
- Support live guest communication (in-app + device notifications).
- Be installable as an app-like PWA with branded shortcuts.

---

## Design System

### Visual Direction

- **Style:** Editorial luxury (inspired by premium travel brands)
- **Mood:** Elegant, calm, aspirational
- **Layout Rhythm:** Alternating dark/light content chapters, large image cards, clear CTAs

### Brand Palette

- `#c8a96e` - Warm Gold (premium accents)
- `#1a1410` - Deep Charcoal Brown (grounded luxury)
- `#faf8f3` - Warm Ivory (soft premium canvas)
- `#5a4e42` - Supporting warm text tone
- `#e8e0d0` - Sand borders/dividers

### Typography

- **Cormorant Garamond** for hero/headlines/editorial identity
- **Jost** for body text/navigation/form controls

---

## Core Features

- Premium hero experience with parallax feel and cinematic overlays
- Fully responsive luxury navbar + mobile menu
- Room listing grid with interactive overlays
- Dedicated room details page with gallery and metadata
- Booking overlay/form from room details
- Full booking page with availability and payment-method selection
- Live in-app notifications + device/browser notifications
- Notification permission prompt for user device
- PWA support: manifest, service worker, app shortcuts, branded icon assets
- WhatsApp + Email booking request handoff
- Live chat widget with transcript forwarding
- Multi-language structure (EN/RW/FR)

---

## Pages & User Flow

### Main Pages

- `/` - Home (brand overview + premium storytelling)
- `/rooms` - Rooms listing
- `/rooms/:id` - Room details + gallery + booking overlay
- `/booking` - Full booking workflow
- `/about` - Story, values, location
- `/amenities` - Services grid
- `/gallery` - Visual showcase + virtual tour section
- `/reviews` - Testimonials
- `/contact` - Contact + map
- `/blog` - SEO/marketing updates

### Booking Funnel

1. Browse room cards
2. Open room details
3. Click **Book Now**
4. Complete overlay form:
   - Name
   - Phone
   - Check-in / Check-out (date + time)
   - Room type
   - Guests
   - Payment method
5. Submit request to WhatsApp + Email

---

## Video Showcase

Use this section to attach walkthroughs for clients, investors, or team demos.

### Suggested Demo Videos

- **Home + Luxury UI Tour**
- **Rooms to Booking Flow**
- **Realtime Notifications + PWA Install**

### Video Links (Replace with your own)

- `Home Tour:` https://your-video-link.com/home-tour
- `Booking Walkthrough:` https://your-video-link.com/booking-flow
- `PWA + Notifications:` https://your-video-link.com/pwa-notifications

### Optional Embedded Video Block

```html
<video width="100%" controls>
  <source src="docs/videos/giftinn-demo.mp4" type="video/mp4" />
</video>
```

---

## Project Structure

```text
src/
  components/
    Navbar.jsx
    Footer.jsx
    ChatWidget.jsx
    NotificationCenter.jsx
    NotificationPermissionPrompt.jsx
    RoomCard.jsx
  context/
    LanguageContext.jsx
    NotificationContext.jsx
  data/
    siteContent.js
  hooks/
    useRealtimeAvailability.js
    useSeo.js
  pages/
    HomePage.jsx
    RoomsPage.jsx
    RoomDetailsPage.jsx
    BookingPage.jsx
    AboutPage.jsx
    AmenitiesPage.jsx
    GalleryPage.jsx
    ReviewsPage.jsx
    ContactPage.jsx
    BlogPage.jsx
public/
  manifest.json
  sw.js
  icons/
    giftinn-logo.svg
    giftinn-badge.svg
```

---

## Local Setup

```bash
npm install
npm run dev
```

### Build

```bash
npm run build
npm run preview
```

### Lint

```bash
npm run lint
```

---

## PWA & Notifications

### Included

- `public/manifest.json` with app shortcuts
- `public/sw.js` service worker registration
- Device notification permission request UI
- Native notifications for in-app live updates

### Important

Device notifications require:

- HTTPS in production
- Browser permission granted by the user

---

## Deployment Notes

- Works on Vite-compatible hosts (Vercel, Netlify, Render, VPS)
- Ensure static files from `public/` are served at root (`/manifest.json`, `/sw.js`, `/icons/*`)
- Configure HTTPS for full notification and PWA behavior

---

## Future Upgrades

- Real payment gateway integration (Stripe/Flutterwave/PayPal)
- Real booking backend + room availability API
- Admin dashboard for reservation management
- Push notification backend (FCM/Web Push)
- CMS-backed blog + offers manager

---

## License

This project is currently intended for GiftInn product development and customization.
