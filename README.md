# Vite React Express Boilerplate

A starter for a full-stack app: a Vite and React front end with an Express API in the same repo. Both run together in development, and the production server serves the built client.

**Status:** Starter. It is a working template with one demo API route (`GET /api/hello`) and a welcome screen, and it is meant to be copied as the base of a new project rather than shipped as an app.

## The problem

Starting a React app with a separate Express API means repeating the same setup: a bundler, a dev server that runs both halves, a proxy so the front end can call the API, and a production server. This repo puts that setup in one place.

## What it does

- Renders a welcome page with a button component, using CSS modules (`src/app/App.jsx`, `src/app/components/`).
- Exposes a demo endpoint, `GET /api/hello`, which returns `{ message: 'Hello World!' }` (`src/lib/router.js`).
- Serves the built client from `dist/app` and returns the app shell for any other path (`src/server.js`).
- Runs the Vite dev server with a proxy in `vite.config.js`, so requests to the API reach Express during development.

## How it's built

- React 17 with React Router DOM 6 on the front end, bundled by Vite 2.
- Express 4 for the API. `src/server.js` mounts the router under `/api` and parses JSON bodies.
- Server code is compiled with Babel into `dist/` by `server:build`, and the production build also runs `vite build`.
- `concurrently` and `nodemon` run the client and server together in `pnpm dev`.
- ESLint, Prettier and Stylelint are configured, with lint-staged in `.lintstagedrc.json`.

## Running it locally

```bash
pnpm install
cp .env.example .env   # set PORT
pnpm dev               # client and API together
pnpm build             # babel for the server, vite for the client
```

Other scripts: `clean` (removes `dist`), `serve` (Vite preview) and `format`.

## What's left

- The only API route is the hello demo. A real project would add its own routes and a data layer.
- There is no authentication, database or test setup.
