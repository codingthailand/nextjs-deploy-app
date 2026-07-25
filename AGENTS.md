<!-- BEGIN:nextjs-agent-rules -->
# This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` before writing any code. Heed deprecation notices.
<!-- END:nextjs-agent-rules -->

## Repo facts

- Next.js **16.2.11** + React 19, plain `create-next-app` layout (App Router under `src/app/`). No tests, no CI, no custom `next.config.ts` options.
- Package manager: **npm** (`package-lock.json` is the lockfile — don't introduce pnpm/yarn).
- Docs for this exact Next.js version ship locally at `node_modules/next/dist/docs/` — prefer them (or Context7) over memory for any API/config question.

## Commands

- `npm run dev` / `npm run build` / `npm start` — standard Next.js.
- `npm run lint` — runs plain `eslint` (flat config in `eslint.config.mjs`, includes `eslint-config-next` core-web-vitals + typescript). `next lint` is removed in Next 16; don't suggest it.
- Typecheck: no script exists — use `npx tsc --noEmit` (`tsconfig.json` is set up for it).

## Conventions

- Tailwind CSS **v4** via `@tailwindcss/postcss` — config is CSS-first in `src/app/globals.css`; there is no `tailwind.config.*` file.
