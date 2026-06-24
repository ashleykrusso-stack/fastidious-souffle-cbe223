[README.md](https://github.com/user-attachments/files/29297044/README.md)
# Levy Banquet Ops

AI-powered banquet operations platform for Levy Restaurants at LACC.
Upload BEO PDFs → auto-generate prep sheets, menu tags, staffing schedules, and ops plans.

## Deploy in 2 minutes

### Netlify drag & drop
1. `npm run build` → drag `dist/` to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Set env vars in Site Settings → Environment Variables

### GitHub + Netlify/Vercel (recommended)
1. Push to GitHub → import in Netlify or Vercel
2. Set env vars → deploy

## Environment Variables

Copy `.env.example` to `.env`:

```
VITE_ANTHROPIC_API_KEY=sk-ant-your-key-here

# Optional Supabase (for persistence + auth)
# VITE_SUPABASE_URL=https://your-project.supabase.co
# VITE_SUPABASE_ANON_KEY=eyJ...
```

Without Supabase: demo mode with sample LACC data. AI works with key set.

## Local Dev

```bash
npm install
cp .env.example .env
npm run dev
```

## Supabase (production)

```bash
supabase secrets set ANTHROPIC_API_KEY=sk-ant-...
supabase functions deploy ai
```

## Stack
React 18 · Vite · Tailwind CSS · React Router · Claude claude-sonnet-4-6 · Supabase (optional)
