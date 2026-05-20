# CLAUDE.md

## Stack

- HTML/CSS/JS prototypes (static sites, no frameworks unless specified)
- Vercel and Netlify for deploys
- Supabase for backend (Postgres, Auth, Edge Functions, Storage)
- n8n for automation workflows

## Conventions

- Ship working code. No placeholder comments, no TODO stubs, no "coming soon" sections.
- Inline styles or single CSS file for prototypes. No build tools unless asked.
- Use semantic HTML. Keep markup clean.
- SQL migrations go in `/supabase/migrations/` with timestamp prefixes.
- Edge functions go in `/supabase/functions/`.

## Deploy

- Vercel: static output in project root or `/public`. No framework config unless needed.
- Netlify: same. Use `netlify.toml` only when redirects or headers are required.

## Supabase

- Use the Supabase MCP tools for SQL execution, migrations, and edge function deploys.
- Always use Row Level Security on new tables.
- Prefer `timestamptz` over `timestamp`.

## Style

- Terse responses. No summaries of what just happened.
- Don't explain obvious code. Don't add comments unless the why is non-obvious.
- Ask before creating new directories or restructuring.
