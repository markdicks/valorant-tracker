# Valorant Tracker+

> 📊 A public dashboard for Valorant players to track their rank, set improvement goals, and discover curated content — powered by React, .NET, and optional Blazor.

---

## 🚀 Features

- 🎮 **Valorant Stats Viewer**  
  Display player rank, match history, and progression (via Riot API or Tracker integration).

- 🎯 **Goal & Task Tracking**  
  Daily/weekly training checklist and rank progression goals.

- 🧑‍💼 **User Profiles & Authentication**  
  Custom user profiles with email/password + optional Google OAuth, public profile URLs (`/user/<gamertag>`).

- 🎨 **Dynamic Themes**  
  Valorant-style theming with light/dark modes, future expansion per game.

- 📰 **Content Feed**  
  Embed official patch notes, top YouTube clips, and curated Discord servers.

- 🛠️ **Modular Stack**  
  React frontend, .NET 8 API backend, Blazor for optional internal/admin tools.

---

## 🧱 Tech Stack

| Layer        | Tech                                                          |
|--------------|---------------------------------------------------------------|
| Frontend     | React + Vite + TailwindCSS (hosted on Vercel)                |
| Backend API  | ASP.NET Core 8 Web API (hosted on Fly.io)                    |
| Auth         | Firebase Auth (email/password + Google OAuth)                |
| Database     | Supabase (PostgreSQL + Auth-compatible)                      |
| File Storage | Supabase Storage (for profile images, game screenshots, etc.)|
| Admin UI     | Blazor Server (self-hosted, for internal tools only)         |
| CI/CD        | GitHub Actions (build, lint, deploy frontend & backend)      |
| Hosting      | Vercel (Frontend) + Fly.io (API) + Supabase (DB/Auth/Storage)|



---

## 🔧 Local Setup

### 1. Clone the Monorepo

```bash
git clone https://github.com/<your-username>/valorant-tracker.git
cd valorant-tracker
```
### 2. Start the Frontend

```bash
cd client
npm install
npm run dev
```
### 3. Start the Backend

```bash
cd server
dotnet restore
dotnet run
```
> API will run at https://localhost:5001 by default.
### 4. (Optional) Admin Dashboard

```bash
cd admin
dotnet run
```
🛑 Never commit `.env` files.

---

## 📦 Project Structure

```
valorant-tracker/
├── client/      → React + Vite + TailwindCSS frontend (user dashboard, public profiles)
├── server/      → ASP.NET Core 8 Web API (auth, stats aggregation, supabase integration)
├── admin/       → Blazor Server admin panel (moderation tools, feature toggles)
├── infra/       → Infrastructure configs (Fly.io, Vercel, Supabase schema migrations)
├── .github/     → GitHub Actions CI/CD workflows (build, test, deploy frontend/backend)
├── docs/        → Planning, architecture decisions, API specs, DB schemas
└── README.md    → Project overview, setup instructions, roadmap
```

---

## 🧪 CI/CD

| Tool           | Purpose                                             |
|----------------|-----------------------------------------------------|
| GitHub Actions | Linting, testing, build, deploy (frontend + backend)|
| Vercel         | Automatic deploys for frontend (React + Vite)       |
| Fly.io         | Backend API deployment (ASP.NET Core 8)             |
| Supabase       | Managed DB, auth, and storage (no deploy needed)    |

---

## 🌍 Live Demo

> **Coming soon:** Deployed at [https://vtracker.dev](https://google.com)

---

## 📅 Roadmap

- [ ] 🎮 Integrate Riot API or Tracker.gg fallback
- [ ] 🧠 Daily task UI with completion tracking
- [ ] 🛂 OAuth login (Google)
- [ ] 🧩 Theme customization per user
- [ ] 🧪 CI/CD pipeline + production DB
- [ ] 📲 Discord bot integration

---

## 🤝 Contributing

Pull requests welcome. For major changes, open an issue to discuss what you want to change.

---

## 📄 License

GNU GPLv3 License

---

## 📬 Contact

Made by [@markdicks](https://github.com/markdicks)  
Drop issues, feature requests, or feedback in the [Discussions tab](https://github.com/markdicks/valorant-tracker/discussions)
