<p align="center">
  <video src="demo.mp4" controls width="600"></video><br>
</p>

# Transcendence

A full‑stack TypeScript project that delivers a browser‑based arcade experience with multiple game modes and real‑time interactions. It includes a Fastify backend with a database via Prisma and a front‑end that renders and controls game modes such as Pong and Snake. End‑to‑end tests are provided with Playwright.

# Team
* [Anna](https://github.com/akrepkov)
* [Lena](https://github.com/elenavoronin)
* [Jan](https://github.com/jmolenaa)
* [Djoyke (me)](https://github.com/DjoykeAbyah)

Check out the [Original repository](https://github.com/akrepkov/transcendence) and [kanban board](https://github.com/users/akrepkov/projects/1) to get a glimpse into how we managed the project.


## Overview

- Frontend
  - Landing page with selectable game modes: Pong, Snake, Practice, and AI.
  - Smooth navigation between modes with overlay and in‑game “back” controls.
  - Profile view to manage account data and explore social features.
  - Tailwind CSS for styling.
  - Playwright tests validating navigation, URL changes, and view state.
- Backend
  - Fastify server providing REST APIs and serving static assets.
  - Authentication and session support (JWT and cookies).
  - Real‑time features powered by WebSockets (for gameplay and presence).
  - Prisma ORM to manage the database schema and access.
  - File uploads (e.g., avatars) via multipart handling.
  - Structured logging.

## Key Features

- Multiple game modes: Pong, Snake, Practice, AI.
- Real‑time gameplay and updates over WebSockets.
- User accounts and profiles:
  - Update username.
  - Update profile picture (avatar).
  - Change password (securely hashed).
- Social and presence:
  - Maintain a friend list.
  - View your own stats and your friends’ stats.
  - See friends’ online/offline status in real time.
- Robust tooling: linting, formatting, and E2E tests.

## Tech Stack

- Language: TypeScript, Javascript
- Frontend: Browser-based app, Tailwind CSS
- Backend: Fastify (+ static, cookie, websocket, multipart plugins)
- Auth: JSON Web Tokens, bcrypt for password hashing
- ORM/DB: Prisma (+ generated client)
- Tooling: ESLint, Prettier, Husky
- Testing: Playwright (@playwright/test)
- Package manager: npm

## Frontend

- Renders the landing page and handles navigation to each game mode.
- Updates view state and URLs per selected mode.
- Provides a profile page to:
  - Edit username, avatar, and password.
  - Display your statistics, game history, and friends list.
  - Show friends’ online status indicators.
- Integrates with the backend for authentication, profile updates, stats, and presence.

## Backend

- Serves REST endpoints for authentication, user/profile management, stats, and games.
- Issues and validates JWTs; manages sessions via cookies when needed.
- Persists user data, friendships, and game stats with Prisma.
- Handles avatar uploads via multipart form data.
- Exposes WebSocket endpoints for real‑time gameplay and friend presence updates.
- Serves static assets (front‑end build and public files).

## Prerequisites

by running `make` docker will install all prerequisites

## Environment Variables

environment variables are present in the repo since this project is not meant for deployment
