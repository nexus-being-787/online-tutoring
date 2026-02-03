# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

# Project Description & Generation Prompt

This project was built based on the following comprehensive specification. You can use this prompt to recreate the application's core logic and design.

## Master Prompt
**Role:** Senior Frontend Developer & UI/UX Designer  
**Project:** "EduPrime" - A Modern Online Learning Platform  
**Tech Stack:** React (Vite), Tailwind CSS, React Router DOM v6, Lucide React Icons.

### 1. Design System & UI Theme
* **Theme:** "Dark Mode Cyberpunk/Glassmorphism".
* **Colors:** Deep slate background (`bg-slate-950` / `#020617`), White text (`text-slate-200`), Neon Accents (Cyan-500, Purple-600, Blue-600).
* **Styling:** extensive use of `backdrop-blur`, semi-transparent borders (`border-white/10`), and CSS gradients for text/buttons.
* **Animations:** Smooth page transitions (fade-in), floating particle background on Home, 3D tilt effects on course cards, and hover glows.

### 2. Core Architecture
* **Routing:** Use `react-router-dom`. The `App.jsx` must strictly define routes to prevent the Home page from appearing as a footer on other pages. Use an `index` route for Home.
* **State Management:** Create a `CourseContext` (Context API) to manage:
    * `user` (Mock auth state).
    * `enrolledCourses` (Array of course objects).
    * Functions: `login` (simulated delay), `logout`, `enroll`.
    * **Data Source:** Use local Mock Data. Do NOT implement a real backend/Firebase yet.

### 3. Pages & Features
* **Navbar:** Sticky, glass-effect. Shows "Login" button if guest, or "User Avatar + Profile/Settings/Logout" dropdown if logged in. Includes a floating **Chat Widget** toggle.
* **Home Page:**
    * **Hero Section:** "Master the Future Without Limits" (with Typewriter text effect).
    * **Background:** Custom `<Particles />` component with floating glowing orbs.
    * **Stats Strip:** Hoverable stats (e.g., "50k+ Students").
* **Courses Page:** A grid of course cards with a working **Search Bar** and **Category Filter** pills.
* **Course Details Page:**
    * **Tabbed Interface:** Switch between Overview, Curriculum, Instructor, and Reviews.
    * **Sticky Sidebar:** "Enroll Now" card that follows scroll.
* **Course Player (Learning Mode):**
    * Video player simulation.
    * **Interactive Quizzes:** Toggle between "Video" and "Quiz" mode. Quizzes provide instant feedback (Green/Red) and a score result screen.
* **Dashboard (My Learning):**
    * Displays enrolled courses.
    * **Confetti/Celebration:** Visual welcome animation for returning users.
    * **Progress Bars:** Visual indicator of course completion.
* **Authentication:**
    * **Login Page:** Split-screen design (Brand left, Form right). Simulated login process with a spinner (`Loader2`).
* **User Pages:**
    * **Profile:** Edit name, email, and bio.
    * **Settings:** Toggle notifications and security settings.

### 4. Interactive Components
* **Course Card:** 3D Tilt effect on mouse hover (`perspective` & `rotateX/Y`).
* **Chat Widget:** A floating support bot that auto-replies to keywords (e.g., "price", "react").

**Goal:** Create a visually stunning, highly interactive UI that feels like a production-ready SaaS product, prioritizing user experience and fluid animations.
