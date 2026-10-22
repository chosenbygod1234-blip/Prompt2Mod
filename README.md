# Prompt 2 Mod AI Backend

Small Node.js/Express backend for the Prompt 2 Mod Android app.

## Deploy on Render

- Create a **Web Service** from this GitHub repository.
- Runtime: Node
- Build command: `npm install`
- Start command: `npm start`
- Add environment variable `OPENAI_API_KEY` with your secret OpenAI API key in Render's Environment settings.
- Optional: add `OPENAI_MODEL` with a model available to your API account. The default is `gpt-5.5`.
- Deploy the service.

Never put API keys in GitHub or in the Android app source.

## Endpoints

- `GET /` — service information
- `GET /health` — health check
- `POST /agent` — expects JSON such as `{"message":"Help me plan a mod","context":"","history":[]}` and returns `{"reply":"..."}`

This starter includes a basic in-memory IP request limit. It is suitable for testing, not a complete abuse-prevention system for a large public service.
