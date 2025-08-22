# PM Platform Clean — Full-Stack Scaffold (Fixed)

Tech: **Node.js (Express)** + **SQLite** + **Vue 3 (Vite)**

## Quick Start

### 0) Requirements
- Node.js >= 20
- npm

### 1) Backend
```bash
cd backend
cp .env.example .env   # adjust if needed
npm install
npm run reset:db       # creates app.db and seeds admin + roles/permissions
npm run dev            # runs on http://localhost:3000
```

Admin seed user: **admin@local** / **admin123**

### 2) Frontend
```bash
cd ../frontend
npm install
npm run dev            # http://localhost:5173
```

The Vite dev server proxies `/api` to the backend port 3000.

## Implemented
- Signup (pending) with fields: username, email, password, role
- Login (blocked if pending / suspended)
- Admin endpoints + Admin UI
  - Accept / Reject (with reason)
  - Modify role on accept
  - Suspend / Activate / Delete (suspended-only)
- User endpoints:
  - Get profile, update phone
  - View notifications
- Role hierarchy + permissions seeded; admin has all.
