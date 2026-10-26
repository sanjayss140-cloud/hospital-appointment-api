# Hospital Appointment API

A complete Node.js + Prisma CRUD module for the hospital appointment domain.

## Tech Stack
- Node.js (ES Modules)
- TypeScript
- Prisma ORM 7.10.0 with PostgreSQL & `@prisma/adapter-pg`
- `tsx` runner

## Features
- Introspected and cleaned Prisma schema matching Prisma conventions (`PascalCase` models, `camelCase` fields, `@map` and `@@map`).
- Complete CRUD operations for `Patient`, `Doctor`, and `Appointment` models.
- Relational queries with `connect` and nested `include`.
- Database seeding with `prisma db seed`.
- Full end-to-end test verification script (`src/test.ts`).

## Running the Project
1. Configure database connection in `.env`:
   ```env
   DATABASE_URL="postgresql://<user>:<password>@localhost:5432/hospital_api?schema=public"
   ```
2. Generate Prisma client:
   ```bash
   npx prisma generate
   ```
3. Seed test data:
   ```bash
   npx prisma db seed
   ```
4. Run verification tests:
   ```bash
   npx tsx src/test.ts
   ```
