# Medusa Monorepo

A pnpm monorepo with Turbo for a Medusa backend and Next.js storefront.

## Structure

```
apps/
  backend/     # Medusa backend application
  storefront/  # Next.js storefront
```

## Prerequisites

- Node.js >= 20
- pnpm >= 9

## Getting Started

### Install Dependencies

```bash
pnpm install
```

### Development

Run all apps in development mode:

```bash
pnpm dev
```

Run specific app:

```bash
pnpm --filter backend dev
pnpm --filter storefront dev
```

### Build

Build all apps:

```bash
pnpm build
```

Build specific app:

```bash
pnpm --filter backend build
pnpm --filter storefront build
```

### Start Production

```bash
pnpm start
```

## Turbo

This monorepo uses [Turbo](https://turbo.build/) for:

- Fast, incremental builds
- Smart caching
- Parallel task execution
- Pipeline orchestration

### Turbo Commands

```bash
# Run dev with turbo
turbo dev

# Build with turbo (with caching)
turbo build

# Clear turbo cache
turbo clean
```

## pnpm Workspace

This monorepo uses pnpm workspaces. Key commands:

```bash
# Add dependency to specific workspace
pnpm --filter backend add <package>
pnpm --filter storefront add <package>

# Add dev dependency
pnpm --filter backend add -D <package>

# Run command in all workspaces
pnpm -r <command>

# Update dependencies
pnpm update -r
```

## Environment Variables

Each app manages its own environment variables. See individual app README files for details.

## Learn More

- [Medusa Documentation](https://docs.medusajs.com)
- [Next.js Documentation](https://nextjs.org/docs)
- [Turbo Documentation](https://turbo.build/repo/docs)
- [pnpm Workspaces](https://pnpm.io/workspaces)
