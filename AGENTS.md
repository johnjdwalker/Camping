# AGENTS.md

## Project Overview

This is a full-stack web application built with React, Express, and TypeScript. The project uses modern web development tools and follows a monorepo structure with both frontend and backend code.

## Tech Stack

### Frontend
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter
- **Styling**: Tailwind CSS 4.x with custom animations
- **UI Components**: Radix UI primitives with shadcn/ui
- **State Management**: TanStack Query (React Query)
- **Forms**: React Hook Form with Zod validation
- **Build Tool**: Vite

### Backend
- **Runtime**: Node.js with Express
- **Database**: PostgreSQL (Neon serverless)
- **ORM**: Drizzle ORM
- **Authentication**: Passport.js (local strategy, OpenID)
- **Session Management**: Express Session with connect-pg-simple
- **Payment Processing**: Stripe

### Development Tools
- **Language**: TypeScript 5.6
- **Package Manager**: npm
- **Build**: Vite (frontend), esbuild (backend)
- **Type Checking**: tsc

## Project Structure

```
/workspace/NickSmithSheriffR-20250612T210958Z-1-001/NickSmithSheriffR/
├── server/          # Backend Express application
├── client/          # Frontend React application (likely in src/)
├── components.json  # shadcn/ui component configuration
├── drizzle.config.ts # Database configuration
├── package.json     # Dependencies and scripts
├── tsconfig.json    # TypeScript configuration
├── vite.config.ts   # Vite build configuration
└── tailwind.config.ts # Tailwind CSS configuration
```

## Key Commands

### Development
```bash
npm run dev          # Start development server (backend with tsx)
```

### Build
```bash
npm run build        # Build both frontend (Vite) and backend (esbuild)
npm run start        # Run production build
```

### Type Checking & Database
```bash
npm run check        # TypeScript type checking
npm run db:push      # Push database schema changes with Drizzle
```

## Development Guidelines

### When Making Changes

1. **Frontend Changes**
   - React components are likely in a `client/` or `src/` directory
   - Use existing shadcn/ui components from Radix UI
   - Follow React Hook Form + Zod pattern for forms
   - Use TanStack Query for data fetching
   - Maintain TypeScript strict typing

2. **Backend Changes**
   - Server code is in `server/` directory
   - Use Drizzle ORM for database operations
   - Follow Express middleware patterns
   - Maintain authentication flow with Passport.js
   - Handle errors properly with error middleware

3. **Database Changes**
   - Update schema files used by Drizzle
   - Run `npm run db:push` to apply changes
   - Use Drizzle migrations for production

4. **Styling**
   - Use Tailwind CSS utility classes
   - Follow shadcn/ui design patterns
   - Leverage tailwindcss-animate for animations
   - Check `tailwind.config.ts` for custom theme settings

### Testing Changes

1. Run `npm run check` to verify TypeScript types
2. Test in development mode with `npm run dev`
3. Build the project with `npm run build` to ensure production builds work
4. Check both frontend and backend functionality

### Common Patterns

- **API Routes**: Express routes in server/
- **Database Queries**: Drizzle ORM with type-safe queries
- **Form Validation**: Zod schemas with drizzle-zod integration
- **Authentication**: Passport.js strategies with session management
- **UI Components**: Radix UI primitives wrapped with Tailwind styling

## Environment Setup

This project likely requires:
- Environment variables for database connection (Neon)
- Stripe API keys for payment processing
- Session secrets for authentication
- OpenID client credentials if using OAuth

Check for `.env` or `.env.example` files for required environment variables.

## Git Workflow

- Development branch: `cursor/agents-markdown-file-1807`
- Commit changes with clear, descriptive messages
- Push changes regularly to track progress
- Keep commits focused on single logical changes

## Notes for AI Agents

1. **Always read before modifying** - Use Read tool to understand current implementation
2. **Maintain consistency** - Follow existing patterns in the codebase
3. **Type safety** - Preserve TypeScript types and Zod schemas
4. **Database schema** - Be careful with schema changes, use migrations
5. **Dependencies** - Don't modify package.json versions without good reason
6. **UI/UX** - Maintain the existing design system and component patterns

## Additional Resources

- [React Documentation](https://react.dev)
- [Drizzle ORM Docs](https://orm.drizzle.team)
- [Shadcn UI](https://ui.shadcn.com)
- [Tailwind CSS](https://tailwindcss.com)
- [TanStack Query](https://tanstack.com/query)
- [Express.js](https://expressjs.com)

---

*This file is designed to help AI agents understand and work effectively with this codebase. Update it as the project evolves.*
