# HealthVue - Vue.js Health Landing Page

A modern, responsive health-focused landing page built with Vue 3, TypeScript, and Tailwind CSS.

## 🏥 Project Overview

HealthVue is a comprehensive health platform landing page that showcases:

- Personal health tracking
- Expert consultations
- AI health insights
- Medication management
- Secure health records
- 24/7 support

## 🚀 Tech Stack

- **Vue 3** - Progressive JavaScript framework
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS v4** - Utility-first CSS framework
- **Vue Router** - Client-side routing
- **Vite** - Build tool and development server

## 📁 Project Structure

```
src/
├── components/           # Reusable Vue components
│   ├── TheHeader.vue    # Navigation header with mobile menu
│   ├── TheFooter.vue    # Footer with contact info and links
│   ├── HeroSection.vue  # Main hero section with CTA
│   ├── FeaturesSection.vue  # Service features grid
│   └── TestimonialsSection.vue  # Customer testimonials
├── views/               # Page components
│   ├── HomeView.vue     # Landing page
│   ├── AboutView.vue    # About page
│   ├── ServicesView.vue # Services and pricing
│   └── ContactView.vue  # Contact form and info
├── router/
│   └── index.ts         # Route definitions
├── assets/
│   └── main.css         # Global styles with Tailwind
├── App.vue              # Root component
└── main.ts              # Application entry point
```

## 🛠️ Setup and Development

### Prerequisites

- Node.js 20.19.0+ or 22.12.0+
- npm or yarn

### Installation

```bash
npm install
```

### Development Server

```bash
npm run dev
```

### Build for Production

```bash
npm run build
```

## 📱 Responsive Design

The application is fully responsive with breakpoints:

- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

## 🎯 Key Features

1. **Modern UI/UX**: Clean, professional design focused on health and wellness
2. **Mobile-First**: Responsive design that works on all devices
3. **Performance**: Optimized with lazy loading and efficient bundling
4. **TypeScript**: Full type safety throughout the application
5. **Reusable Components**: Modular architecture for easy maintenance

Built with ❤️ using Vue.js and Tailwind CSS
