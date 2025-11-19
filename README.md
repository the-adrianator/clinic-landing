# Glades Clinic Website

A modern, responsive single-page website for a cosmetic and aesthetic clinic, built with Vue 3 and Tailwind CSS. This project showcases a beautiful, user-friendly interface with smooth animations and a mobile-first design approach.

![Vue](https://img.shields.io/badge/Vue-3.5.24-4FC08D?logo=vue.js&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7.2.2-646CFF?logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.1.17-38B2AC?logo=tailwind-css&logoColor=white)

## 🚀 Features

- **Modern UI/UX Design**: Clean, professional interface with a pink/purple gradient theme
- **Fully Responsive**: Mobile-first design that works seamlessly across all devices
- **Smooth Animations**: AOS (Animate On Scroll) library for engaging scroll-triggered animations
- **Component-Based Architecture**: Modular Vue components for maintainability
- **Accessible**: ARIA labels and semantic HTML for better accessibility
- **Fast Performance**: Optimized with Vite for lightning-fast development and builds
- **Icon Integration**: Beautiful icons using Iconify Vue

## 🛠️ Tech Stack

### Core Technologies
- **Vue 3.5.24** - Progressive JavaScript framework with Composition API
- **Vite 7.2.2** - Next-generation frontend build tool
- **Tailwind CSS 4.1.17** - Utility-first CSS framework

### Key Libraries
- **AOS (Animate On Scroll) 2.3.4** - Scroll animation library
- **@iconify/vue 5.0.0** - Icon component library
- **@vitejs/plugin-vue 6.0.1** - Vue plugin for Vite
- **@tailwindcss/vite 4.1.17** - Tailwind CSS Vite plugin

## 📋 Project Structure

```
clinic-website/
├── src/
│   ├── components/
│   │   ├── About.vue          # About section component
│   │   ├── Contact.vue        # Contact form component
│   │   ├── Footer.vue         # Footer component
│   │   ├── Header.vue         # Navigation header component
│   │   ├── Hero.vue           # Hero section component
│   │   ├── Services.vue       # Services showcase component
│   │   └── Specialists.vue    # Specialists section component
│   ├── assets/                # Images and static assets
│   ├── App.vue                # Main application component
│   ├── main.js                # Application entry point
│   └── style.css              # Global styles
├── public/                    # Public assets
├── index.html                 # HTML entry point
├── vite.config.js             # Vite configuration
└── package.json               # Project dependencies
```

## 🎨 Sections

1. **Header** - Sticky navigation with mobile menu
2. **Hero** - Eye-catching landing section with CTA buttons
3. **Services** - Grid layout showcasing clinic services
4. **About** - Information about the clinic and mission
5. **Specialists** - Team of medical professionals
6. **Contact** - Contact form and information
7. **Footer** - Additional links and information

## 🚦 Getting Started

### Prerequisites

- Node.js (v16 or higher recommended)
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/clinic-website.git
cd clinic-website
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

### Build for Production

```bash
npm run build
```

The production-ready files will be in the `dist` directory.

### Preview Production Build

```bash
npm run preview
```

## 🎯 Key Features Implementation

- **Responsive Navigation**: Mobile hamburger menu with smooth transitions
- **Scroll Animations**: Elements animate into view as you scroll
- **Gradient Backgrounds**: Modern pink-to-purple gradient theme throughout
- **Interactive Elements**: Hover effects and smooth transitions on buttons and cards
- **Semantic HTML**: Proper use of HTML5 semantic elements for better SEO and accessibility

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 📝 License

This project is private and created for portfolio purposes.

## 👤 Author

Developed as a portfolio project to showcase modern web development skills with Vue 3 and Tailwind CSS.

---

**Note**: This is a frontend-only project. For a production deployment, you would need to integrate with a backend API for form submissions and appointment bookings.
