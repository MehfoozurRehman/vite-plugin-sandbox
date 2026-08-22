# Vite React Express Boilerplate

A modern full-stack starter boilerplate featuring a Vite-powered React frontend and a lightweight Express backend.

## Overview

`vite-test` provides a rapid development environment for building full-stack web applications with concurrent hot module replacement for both frontend client code and Express API routes.

## Tech Stack

- **Frontend**: React (v17), [Vite](https://vitejs.dev/) (v2), React Router DOM v6
- **Backend API**: Node.js & Express (v4)
- **Tooling**: Babel, Concurrently, Nodemon, ESLint, Prettier, Stylelint

## Prerequisites

- Node.js (v16 or v18 recommended)
- Package manager (`pnpm` or `npm`)

## Getting Started

1. **Install dependencies**:
   ```bash
   pnpm install
   # or
   npm install
   ```

2. **Configure Environment Variables**:
   Create a `.env` file based on `.env.example`:
   ```bash
   cp .env.example .env
   ```

3. **Run Concurrently in Development Mode**:
   ```bash
   pnpm dev
   # or
   npm run dev
   ```

4. **Access the Application**:
   Open `http://localhost:3000` (or `http://localhost:5173`) in your web browser.

## Available Scripts

- `npm run dev` - Concurrently starts both Express backend and Vite frontend with live reload.
- `npm run client:dev` - Starts only the Vite frontend dev server.
- `npm run server:dev` - Starts only the Express server with Nodemon.
- `npm run build` - Compiles both server and client for production.
- `npm start` - Starts the compiled Express server in production.
- `npm test` - Runs linting and code style checks.

## Author

Created by [Mehfooz-ur-Rehman](https://github.com/MehfoozurRehman).
