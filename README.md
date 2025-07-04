# Supabase‑only LINE GPT Bot

Serverless Python bot for LINE, deployed on Vercel.
Uses:
- OpenAI GPT for chat
- Supabase (Postgres + pgvector) as knowledge base

## Structure
- `api/line_bot.py`  – Serverless Function entry
- `requirements.txt` – Python deps

## Deployment
1. Push to GitHub.
2. In Vercel, import repo. Environment variables:

```
OPENAI_API_KEY=sk-…
SUPABASE_URL=https://xxx.supabase.co
SUPABASE_KEY=service-role-key
LINE_CHANNEL_ACCESS_TOKEN=…
LINE_CHANNEL_SECRET=…
```

3. Set Webhook URL in LINE console:

```
https://PROJECT.vercel.app/api/line_bot/callback
```
