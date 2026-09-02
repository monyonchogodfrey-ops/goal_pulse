# Goal Pulse Predictions — Football Analysis

A production-oriented Next.js 16 + Supabase starter for a football-analysis site under the Goal Pulse Predictions brand.

## What is included

- Public responsive website
- Match fixtures and results
- Editorial football predictions with confidence, goals/BTTS views and result tracking
- Football analysis articles
- Search by team/league
- Secure Supabase email/password authentication
- Admin dashboard
- Admin-controlled match and article publishing
- PostgreSQL schema with Row Level Security
- Custom SVG Goal Pulse logo
- Dynamic article pages with SEO metadata
- `robots.txt` and dynamic `sitemap.xml`
- Mobile-first dark/green visual design

## Important

This project is intentionally an **analysis/information site**. It does not implement betting, wagering, payment, odds, or gambling features.

## Setup

1. Install Node.js 20+.
2. Create a Supabase project.
3. In Supabase SQL Editor, run `supabase/schema.sql` (this includes the predictions system).
4. Create your first user in Supabase Authentication.
5. Copy that user's UUID and run:
   `update public.profiles set role='admin' where id='YOUR_UUID';`
6. Copy `.env.example` to `.env.local`.
7. Put your Supabase URL, publishable key, and public site URL in `.env.local`.
8. Run:
   `npm install`
   `npm run dev`
9. Open `http://localhost:3000`.
10. Go to `/login` and sign in.

## Deploy

The project is ready to deploy on a modern Next.js host such as Vercel or another Node-compatible platform. Add the same environment variables in the hosting dashboard and set `NEXT_PUBLIC_SITE_URL` to your real HTTPS domain.

## Google Search

Next.js provides metadata, a sitemap and robots file in this project. Google recommends crawlable links, descriptive page titles/descriptions, a sitemap, accessible text content and Search Console for monitoring. Submit your production sitemap at:
`https://YOUR-DOMAIN.com/sitemap.xml`

Google does not guarantee indexing or rankings.

## Security

- Never put a Supabase service-role key in browser code or `NEXT_PUBLIC_*`.
- Keep the admin route protected by Supabase Auth and the database protected by RLS.
- Use HTTPS in production.
- Turn on appropriate email confirmation and password policies in Supabase.
- Review Supabase Auth and RLS policies before launch.

## Brand

The logo is an original SVG mark included in `components/Logo.tsx`. Replace or refine it there if you want a different visual identity.
