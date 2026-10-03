# STADENCHAT

Mobile-first Progressive Web App (PWA) starter for public/private group communities.

## Current starter features
- Responsive landing/dashboard UI
- Demo group listings and online-user panel
- PWA manifest and service worker
- Express API health endpoint and demo groups endpoint
- PostgreSQL-ready environment configuration

## Important
This is a starter scaffold, not a production chat or payment system yet. Authentication, persistent database models, real-time messaging, paid-group access, and M-Pesa verification must be implemented and tested before public launch. Do not collect real payments with this starter.

## Run locally
1. Install Node.js 20+.
2. In the project root run `npm install`.
3. Run `npm install --prefix server` and `npm install --prefix client`.
4. Copy `.env.example` to `server/.env` and set values.
5. Run `npm run dev`.
6. Frontend: http://localhost:5173, API: http://localhost:10000.

## GitHub
Create a new repository named `stadenchat`, then from this folder:
```bash
git init
git add .
git commit -m "Initial STADENCHAT PWA scaffold"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/stadenchat.git
git push -u origin main
```

## Render deployment
- Create a PostgreSQL database on Render when database support is added.
- Create a Web Service connected to the GitHub repository.
- Build command: `npm install && npm install --prefix server && npm install --prefix client && npm run build`
- Start command: `npm start`
- Add environment variables in Render: `JWT_SECRET`, `DATABASE_URL`, `CLIENT_URL`.
- The server serves the built frontend in production.

Keep secrets in Render environment variables, never commit `.env`.
