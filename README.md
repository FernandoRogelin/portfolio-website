# Fernando Rogelin - Portfolio

A modern, responsive portfolio website built with Vue 3, TypeScript, and TailwindCSS, featuring smooth animations and internationalization support.

## 🌐 Live Demo

Visit the live portfolio at [fernandorogelin.com](https://fernandorogelin.com)

## 📋 About The Project

This portfolio showcases my professional experience, skills, and projects as a Full Stack Developer. The website features a clean, modern design with smooth scroll animations and support for both English and Portuguese languages.

### Key Features

- **Responsive Design**: Fully optimized for desktop, tablet, and mobile devices
- **Internationalization (i18n)**: Support for English and Portuguese with persistent language preference
- **Smooth Animations**: Beautiful scroll-based animations using AOS (Animate On Scroll)
- **Modern UI**: Glassmorphism effects, gradient backgrounds, and smooth transitions
- **Type-Safe**: Built with TypeScript for enhanced code quality and developer experience
- **Performance Optimized**: Fast loading times with Vite's optimized build system

## 🚀 Built With

### Core Technologies

- **[Vue 3](https://vuejs.org/)** (v3.5.22) - Progressive JavaScript framework with Composition API
- **[TypeScript](https://www.typescriptlang.org/)** (v5.9.0) - Typed superset of JavaScript
- **[Vite](https://vite.dev/)** (v7.1.11) - Next generation frontend tooling

### Styling

- **[TailwindCSS](https://tailwindcss.com/)** (v4.1.17) - Utility-first CSS framework
- **[@tailwindcss/vite](https://github.com/tailwindlabs/tailwindcss/tree/next/packages/%40tailwindcss-vite)** (v4.1.17) - Vite plugin for TailwindCSS v4
- **[PostCSS](https://postcss.org/)** (v8.5.6) - CSS transformation tool
- **[Autoprefixer](https://github.com/postcss/autoprefixer)** (v10.4.22) - CSS vendor prefixing

### Libraries & Plugins

- **[vue-i18n](https://vue-i18n.intlify.dev/)** (v9.14.5) - Internationalization plugin for Vue 3
- **[AOS](https://michalsnik.github.io/aos/)** (v2.3.4) - Animate On Scroll library
- **[@vitejs/plugin-vue](https://github.com/vitejs/vite-plugin-vue)** (v6.0.1) - Official Vite plugin for Vue

### Development Tools

- **[Vue TSC](https://github.com/vuejs/language-tools)** (v3.1.1) - TypeScript type checking for Vue
- **[Vue DevTools](https://github.com/vuejs/devtools-next)** (v8.0.3) - Development tools for Vue
- **[@types/aos](https://www.npmjs.com/package/@types/aos)** (v3.0.7) - TypeScript definitions for AOS
- **[@types/node](https://www.npmjs.com/package/@types/node)** (v22.18.11) - TypeScript definitions for Node.js

## 📂 Project Structure

```
portfolio-website/
├── public/                 # Static assets
├── src/
│   ├── assets/            # Images, styles, and other assets
│   │   ├── images/        # Profile photo and project images
│   │   └── main.css       # Global styles and TailwindCSS imports
│   ├── components/        # Vue components
│   │   ├── AboutSection.vue
│   │   ├── ContactSection.vue
│   │   ├── ExperienceSection.vue
│   │   ├── HeroSection.vue
│   │   ├── LanguageSwitcher.vue
│   │   ├── ProjectsSection.vue
│   │   └── SkillsSection.vue
│   ├── i18n/              # Internationalization
│   │   ├── locales/       # Translation files
│   │   │   ├── en.ts      # English translations
│   │   │   └── pt.ts      # Portuguese translations
│   │   └── index.ts       # i18n configuration
│   ├── App.vue            # Root component
│   └── main.ts            # Application entry point
├── index.html             # HTML template
├── package.json           # Project dependencies
├── tsconfig.json          # TypeScript configuration
├── vite.config.ts         # Vite configuration
└── README.md              # Project documentation
```

## 🛠️ Installation & Setup

### Prerequisites

- Node.js (v20.19.0 or higher, or v22.12.0+)
- npm or yarn

### Installation

1. Clone the repository
   ```sh
   git clone https://github.com/fernandorogelin/portfolio.git
   ```

2. Navigate to the project directory
   ```sh
   cd portfolio-website
   ```

3. Install dependencies
   ```sh
   npm install
   ```

### Development

Run the development server with hot-reload:
```sh
npm run dev
```

The application will be available at `http://localhost:5173`

### Production Build

Build the project for production:
```sh
npm run build
```

Preview the production build locally:
```sh
npm run preview
```

### Type Checking

Run TypeScript type checking:
```sh
npm run type-check
```

## 🌍 Internationalization

The portfolio supports two languages:
- **English (EN)** - Default language
- **Portuguese (PT)** - Brazilian Portuguese

Language preference is saved in localStorage and persists across sessions. Users can switch languages using the toggle button in the top-right corner of the page.

## 📱 Sections

### Hero Section
- Profile photo with gradient animation
- Professional title and description
- Social media links (LinkedIn, GitHub, Twitter, Instagram, Facebook, Steam)
- Call-to-action button

### About Section
- Professional introduction
- Background and experience overview
- Career highlights

### Experience Section
- Timeline-based layout
- Work experience at Deskbee and Usabit
- Key achievements and responsibilities
- Company details and locations

### Skills Section
- Categorized technical skills
- 8 categories including:
  - Languages
  - Frontend
  - Backend
  - Databases
  - Cloud & DevOps
  - Tools & Others
  - Mobile
  - Currently Learning

### Projects Section
- Featured projects showcase
- Project descriptions and technologies used
- Live demo and GitHub repository links

### Contact Section
- Email contact button
- Social media links
- Copyright footer

## 🎨 Design Features

- **Gradient Backgrounds**: Cyan to blue gradient themes throughout
- **Glassmorphism**: Frosted glass effects with backdrop blur
- **Smooth Animations**: Fade-up and fade-down animations on scroll
- **Hover Effects**: Interactive hover states on buttons and cards
- **Responsive Typography**: Fluid text sizing across breakpoints
- **Custom Icons**: SVG icons for social media and UI elements

## 📄 License

This project is open source and available for personal and educational use.

## 📞 Contact

Fernando Rogelin - [fernando.rogelin@hotmail.com](mailto:fernando.rogelin@hotmail.com)

Portfolio Website: [fernandorogelin.com](https://fernandorogelin.com)

LinkedIn: [fernando-rogelin](https://www.linkedin.com/in/fernando-rogelin/)

GitHub: [@fernandorogelin](https://github.com/fernandorogelin)

---

⭐ If you like this project, please give it a star on GitHub!