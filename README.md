# Cyber Security Hub

An interactive React application to practice basic cybersecurity skills — port scanning, password strength checking, and a cybersecurity quiz.

## Table of Contents

* [Features](#features)
* [Technologies](#technologies)
* [Requirements](#requirements)
* [Local Setup](#local-setup)
* [Deploy to Cloudflare Pages](#deploy-to-cloudflare-pages)
* [Project Structure](#project-structure)
* [License](#license)

## Features

* **Dashboard** with an overview and navigation.
* **Port Scanner** (simulation) with a chart of open/closed ports.
* **Password Checker** — heuristic strength evaluation with visual feedback.
* **Cybersecurity Quiz** with real-time feedback and scoring.
* Animations via *Framer Motion*, stylish components from *shadcn/ui*, and icons via *lucide-react*.

## Technologies

| Technology    | Purpose              |
| ------------- | -------------------- |
| React 18      | Front-end library    |
| Vite          | Dev/build tool       |
| Tailwind CSS  | Styling              |
| shadcn/ui     | UI components        |
| lucide-react  | SVG icons            |
| Framer Motion | Animations           |
| Recharts      | Chart visualizations |

> **Note**: You can adapt this project to use Create React App or Next.js if preferred.

## Requirements

* **Node.js ≥ 18**
* **pnpm** (recommended), or **npm** / **yarn**

## Local Setup

```bash
# Clone the repository
git clone https://github.com/<username>/<repo>.git
cd <repo>

# Install dependencies
pnpm install       # or npm install / yarn install

# Start the dev server
pnpm dev           # or npm run dev / yarn dev

# Open in browser
http://localhost:5173   # default for Vite
```

### Production Build

```bash
pnpm build    # generates /dist folder

# Preview the build (optional)
pnpm preview  # serves /dist locally
```

## Deploy to Cloudflare Pages

1. Go to **Cloudflare > Pages** and create a new project.
2. Connect your GitHub account and select the repo.
3. Configuration:

   * **Framework preset**: `Vite`
   * **Build command**: `pnpm build`
     (or `npm run build` / `yarn build`)
   * **Output directory**: `dist`
4. Click **Deploy**.
   In \~1–2 minutes, you’ll receive a public URL like: `https://<project>.pages.dev`
5. (Optional) Add a custom domain in **Pages > Custom domains**.

> Cloudflare will rebuild the site automatically on each push to `main` (or another selected branch).

## Project Structure (Vite)

```
├── public/                # static files
├── src/
│   ├── CyberSecuritySite.jsx
│   ├── App.jsx           # or main.jsx, imports the main component
│   ├── index.css         # Tailwind directives
│   └── ...
├── tailwind.config.js
├── vite.config.js
└── package.json
```
