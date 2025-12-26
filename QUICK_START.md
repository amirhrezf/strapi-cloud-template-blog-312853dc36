# Quick Start Guide - Local Strapi Development

## Setup Summary

This project is configured for local development with SQLite database. All dependencies are installed and environment variables are configured.

## Starting the Server

To start the Strapi development server, run:

```bash
npm run develop
```

This will:
- Start the Strapi server on `http://localhost:1337`
- Create/use SQLite database at `.tmp/data.db`
- Enable auto-reload on file changes
- Open the admin panel at `http://localhost:1337/admin`

## First Time Setup

If this is your first time running the project:
1. Navigate to `http://localhost:1337/admin` in your browser
2. Create your first administrator account
3. Start using the admin panel

## Stopping the Server

Press `Ctrl+C` in the terminal where the server is running, or:

```bash
pkill -f "strapi develop"
```

## Pushing Changes to Strapi Cloud

After making changes locally:

```bash
git add .
git commit -m "Your commit message"
git push origin main
```

Strapi Cloud will automatically deploy changes from the `main` branch.

## Important Notes

- **Database**: Uses SQLite (`.tmp/data.db`) - created automatically on first run
- **Environment**: `.env` file contains local secrets (not pushed to GitHub)
- **Port**: Server runs on port `1337` by default
- **Auto-reload**: Changes to content types and code will automatically reload the server

## Troubleshooting

If the server doesn't start:
1. Make sure port 1337 is not in use: `lsof -ti:1337`
2. Check that `.env` file exists
3. Verify dependencies are installed: `npm install`
4. Check server logs for errors




