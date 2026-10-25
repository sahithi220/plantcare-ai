# PlantCare AI (LeafLens)

AI-powered plant care that analyzes leaf images for possible diseases and offers care recommendations. The app also includes scan history, plant health statistics, and a conversational gardening assistant.

## Features

- Upload a plant image for an AI-generated plant and disease assessment.
- Review suggested remedies and treatment options.
- Save and revisit previous scans.
- Chat with an AI assistant about plant care.
- View plant health statistics and trends.

## Requirements

- Node.js and npm
- A Gemini API key

## Run locally

1. Install dependencies:

   ```powershell
   npm install
   ```

2. Copy `.env.example` to `.env` and set `GEMINI_API_KEY` to your Gemini API key.

3. Start the development server:

   ```powershell
   npm run dev
   ```

   The app is available at `http://localhost:3000`.

## Scripts

- `npm run dev` starts the development server.
- `npm run build` creates a production build in `dist`.
- `npm run preview` serves the production build locally.
- `npm run lint` runs the TypeScript check.

## Deploy to Render

This repository includes a Render Blueprint in `render.yaml`.

1. Sign in to [Render](https://render.com/) and create a new Blueprint Instance from this GitHub repository.
2. Set `GEMINI_API_KEY` in the service's Environment settings. Do not commit the key to the repository.
3. Deploy the service. Render builds the frontend and starts the Express server; the server listens on Render's assigned `PORT`.

The free web service uses a temporary filesystem. Plant scan history stored in SQLite can be lost when the service restarts or redeploys. Use persistent storage and configure the database path if scan history must survive restarts.

## GitHub repository description

AI-powered plant care app that identifies plant diseases from leaf images and provides treatment recommendations, scan history, and a gardening assistant.
