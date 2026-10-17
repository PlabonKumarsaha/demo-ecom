# Luxury Ecom

Next.js (App Router, TypeScript) scaffold with Tailwind CSS, Drizzle ORM, Neon Postgres, and Better Auth wired up. No ecommerce features, full auth flows, UI, payments, or deployment are implemented yet.

## Setup

1. Install dependencies:

   ```bash
   npm install
   ```

2. Copy the env example and fill in your Neon connection string and auth secret:

   ```bash
   cp .env.example .env
   ```

3. Push the auth schema to your Neon database:

   ```bash
   npm run db:push
   ```

4. Run the dev server:

   ```bash
   npm run dev
   ```

## Structure

- `src/app` — App Router pages and the Better Auth API route (`/api/auth/[...all]`).
- `src/db` — Drizzle client (`index.ts`) and schema (`schema.ts`, currently just the tables Better Auth requires).
- `src/lib/auth.ts` — Better Auth server instance (drizzle adapter).
- `src/lib/auth-client.ts` — Better Auth React client.
- `drizzle.config.ts` — Drizzle Kit config for migrations against Neon.
# demo-ecom
