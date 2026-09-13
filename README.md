# QuickTask — Modern Responsive Task Management Web Application

> *"Organize your day, one task at a time."*

QuickTask is a clean, modern SaaS task management application designed for optimal productivity. Built with React, Vite, and React Router, it features an elegant dark navy & gold design system, rich micro-interactions, complete task CRUD workflows, and responsive layouts across all device form factors.

---

## 🚀 Live Local Demo

The Vite development server is running locally:
- **Local URL**: [http://localhost:5173/](http://localhost:5173/)
- **Network URL**: `http://192.168.29.234:5173/`

### Demo Login Credentials
- **Email**: `test@example.com`
- **Password**: `password123`
*(Or click the **Auto-Fill** button on the login screen for 1-click access)*

---

## ✨ Features

- **SaaS Landing Page (`/`)**:
  - Hero section with live interactive task preview card
  - 4 Feature cards (Add Tasks, Track Progress, Search & Filter, Stay Organized)
  - About section and clean footer
- **Authentication**:
  - **Login (`/login`)**: Email & password validation, password reveal toggle, remember me checkbox, test credential auto-fill.
  - **Registration (`/register`)**: Full name, email, password strength check, password confirmation matching.
  - Protected routes redirecting unauthenticated visitors to `/login`.
- **Dashboard (`/dashboard`)**:
  - Dynamic time-of-day greeting (`Good morning, Alex 👋`)
  - 4 Live Statistics Cards: Total Tasks, Completed, Pending, High Priority
  - Combined real-time search across titles, descriptions, and categories
  - Segmented status tabs (`All`, `Pending`, `Completed`)
  - Multi-criteria filter options (`Priority` + `Category`)
  - Modern Task Table with responsive card fallback for mobile devices
- **Dedicated Task Views**:
  - `/tasks`: All tasks overview
  - `/pending`: Active tasks requiring attention
  - `/completed`: Accomplished tasks with reopen toggle
- **Full Task CRUD**:
  - **Add Task Modal**: Title, description, priority selector, due date, category
  - **Edit Task Modal**: Full editing with immediate reactive updates
  - **Delete Task Dialog**: Two-step confirmation dialog
  - **Complete & Reopen**: Visual strikethrough, badge updates, and celebration confetti
- **Personalization & Settings**:
  - **Settings (`/settings`)**: Full application dark theme switch, notification toggles, sound effects, JSON task export, and demo reset tool.
  - **Profile (`/profile`)**: Avatar gallery picker, user details, job role, and completion badges.
- **LocalStorage State Persistence**: All task edits, creations, profile updates, and theme choices persist across page reloads.

---

## 🛠️ Project Structure

```
├── public/
│   └── logo.svg                 # QuickTask SVG Brand Mark
├── src/
│   ├── components/
│   │   ├── common/
│   │   │   ├── Button.jsx       # Variant-based button (primary, secondary, outline, danger)
│   │   │   ├── ConfirmDialog.jsx# Deletion confirmation modal
│   │   │   ├── Input.jsx        # Inputs with password reveal & validation
│   │   │   ├── Logo.jsx         # QuickTask brand logo
│   │   │   ├── Modal.jsx        # Accessible dialog wrapper with backdrop
│   │   │   ├── ProtectedRoute.jsx # Route guard
│   │   │   └── ToastContainer.jsx # Floating toast notification stack
│   │   ├── layout/
│   │   │   ├── AppLayout.jsx    # Dashboard shell
│   │   │   ├── Navbar.jsx       # Top navigation, global search, notifications, theme toggle
│   │   │   └── Sidebar.jsx      # Left sidebar navigation with task count badges
│   │   └── tasks/
│   │       ├── FilterBar.jsx    # Search + Priority + Status filter controls
│   │       ├── StatsCard.jsx    # Metric counter cards
│   │       ├── TaskCard.jsx     # Responsive card view
│   │       ├── TaskFormModal.jsx# Add / Edit task modal form
│   │       └── TaskTable.jsx    # Task list table with row actions
│   ├── context/
│   │   ├── AuthContext.jsx      # User session, registration & profile state
│   │   ├── TaskContext.jsx      # Task CRUD, stats calculation & seed data
│   │   ├── ThemeContext.jsx     # Light / Dark theme toggling
│   │   └── ToastContext.jsx     # Global notification alerts
│   ├── pages/
│   │   ├── DashboardPage.jsx    # Main dashboard
│   │   ├── LandingPage.jsx      # Public SaaS homepage
│   │   ├── LoginPage.jsx        # Login screen
│   │   ├── ProfilePage.jsx      # User profile & avatar settings
│   │   ├── RegisterPage.jsx     # Account creation
│   │   ├── SettingsPage.jsx     # Application & theme preferences
│   │   └── TasksViewPage.jsx    # Dedicated /tasks, /pending, /completed views
│   ├── styles/
│   │   ├── auth.css             # Authentication styling
│   │   ├── dashboard.css        # Responsive layouts & table grids
│   │   ├── index.css            # Design tokens, variables & typography
│   │   └── landing.css          # Landing page styles
│   ├── utils/
│   │   ├── initialData.js       # Default sample tasks & user
│   │   └── storage.js           # LocalStorage helpers
│   ├── App.jsx                  # React Router root
│   └── main.jsx                 # Vite application mount
├── package.json
└── vite.config.js
```

---

## 💻 Available Scripts

- `npm run dev`: Runs the local Vite development server.
- `npm run build`: Bundles production assets into `/dist`.
- `npm run preview`: Previews the production build locally.
