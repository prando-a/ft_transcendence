# ft_transcendence

`ft_transcendence` is the final project of the 42 Common Core.  
This project is designed to push students' limits by challenging to build a real-time multiplayer web application, using unfamiliar technologies, under strict technical constraints.

## 🎯 Project Overview

`ft_transcendence` is a full-stack web application that brings back the classic **Pong** game with a modern twist. Users can register, compete in tournaments, play real-time matches, and even challenge AI opponents — all within a secure, responsive, single-page application.

## ⚙️ Features

- 🧑‍🤝‍🧑 **Multiplayer Pong** – Play live matches against friends or AI, with optional remote and tournament support.
- 🌐 **Single-Page Application** – Fully functional SPA with history navigation support.
- 🐳 **Dockerized** – One command launches the full app stack in isolated containers.
- 🔒 **Security First** – Protection against XSS, SQL injections, and strong password hashing.
- 🔐 **Google OAuth login and JWT** – For robust authentication and session security.
- 🎮 **Different play-modes and additional games** – PvP, 4 player Battle Royale,  Sprinter minigame and... DOOM? 
- 💻 **Accessible Design** – Compatible with latest PC web-browsers

## 🛠️ Technologies Used

- **Frontend:** TypeScript + React, TailwindCSS, WebSockets
- **Backend:** Node.js + Fastify
- **Database:** SQLite
- **Security:** HTTPS, JWT, dotenv, validation
- **Containerization:** Docker
- **Optional Modules:** AI opponent, DevOps monitoring,, Accessibility, Server-side API, and more.

## 🚀 Getting Started

```bash
# In the root directory
make
```
`docker` and `docker-compose` must be installed. If permission is denied when building `sudo` must be used.

### 🔧 Useful Makefile Commands

- `make` – Build and start all containers in detached mode
- `make down` – Stop and remove all containers
- `make build` – Build containers
- `make rebuild` – Force rebuild containers without cache
- `make restart` – Restart all containers
- `make clean` – Remove images, volumes, and networks
- `make fclean` – Fully clean Docker resources and prune system
- `make re` – Full clean and restart
- `make auth-re`, `make game-re`, etc. – Rebuild and restart specific services

> Tip: You can also use `make config` to view the expanded Docker Compose configuration.


## 📦 Project Structure

```
ft_transcendence/
│
├── srcs/                         # Main application source code
│   ├── backend/                  # Backend services
│   │   ├── gateway/              # API Gateway (Fastify)
│   │   │   ├── src/              # Gateway logic (routes, plugins, config)
│   │   ├── nginx/                # Reverse proxy config
│   │   └── services/             # Microservices
│   │       ├── AI/              # AI player logic
│   │       ├── auth/            # Authentication (login, signup, OAuth)
│   │       ├── game/            # Core game logic (Pong + gamemodes)
│   │       ├── sprinter/        # Additional game service
│   │       └── tournament/      # Tournament management service
│   │
│   └── frontend/
│       └── web/                 # TypeScript SPA with Vite + TailwindCSS
│           ├── public/          # Static assets (images, icons, etc.)
│           └── src/             # Application code (pages, components)
├── docker-compose.yml           # Docker orchestration
├── Makefile                     # Automation commands
├── rename_to_env                # Sample env config
└── README.md                    # Project documentation
```

## 📚 Subject Highlights

- No full-feature frameworks unless allowed by modules (React is a library :D).
- Must justify all third-party libraries.
- Must comply with project-specific security and performance constraints.
- Bonus points awarded for implementing additional modules (major/minor).

---

> _"This is not just another school project. It's a test of how far you've come and how well you adapt to the unknown."_  
> — ft_transcendence Subject