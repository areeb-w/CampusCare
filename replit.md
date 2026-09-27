# CampusCare

CampusCare connects student wellbeing, points-based canteen payments, family support, and nurse triage in one campus companion.

## Run & Operate

- `pnpm --filter @workspace/api-server run dev` — run the API server (port 5000)
- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from the OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- Required env: `DATABASE_URL` — Postgres connection string

## Stack

- pnpm workspaces, Node.js 24, TypeScript 5.9
- API: Express 5
- DB: PostgreSQL + Drizzle ORM
- Validation: Zod (`zod/v4`), `drizzle-zod`
- API codegen: Orval (from OpenAPI spec)
- Build: esbuild (CJS bundle)

## Where things live

- `artifacts/campuscare/src/App.tsx` — single-page prototype and local demo state for student, parent, and nurse roles
- `artifacts/campuscare/src/index.css` — CampusCare visual theme, responsive layout, and motion tokens
- `artifacts/api-server` — shared API server scaffold; the first CampusCare build is intentionally frontend-only
- `artifacts/mockup-sandbox` — reusable mockup preview surface

## Architecture decisions

- The first build is local-state-first so the complete student / parent / nurse demo is usable without account setup or seeded data.
- Health signals are framed as triage and early-support prompts; the product does not present them as medical diagnoses.
- The same demo state powers wallet activity, canteen transactions, symptom check-ins, voucher actions, and nurse visibility so cross-role behavior is easy to demonstrate.

## Product

- Student Today view with points balance, nutrition suggestion, wellbeing signal, recent activity, and checkup voucher
- Canteen menu with glycemic index, nutrition, allergen metadata, points prices, and allergen-safe indicators
- Editable student health passport with blood group, allergies, medications, emergency contact, and symptom check-in
- Parent view for points top-ups and academic micro-scholarship history
- Nurse dashboard with risk queue, student records, transaction/food-pattern context, and voucher issuing or use

## User preferences

No additional preferences recorded.

## Gotchas

- The UI demo uses local state and resets on refresh; persistence and real authentication are intentionally deferred for a later iteration.
- Keep care language supportive and triage-oriented rather than diagnostic.

## Pointers

- See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details
