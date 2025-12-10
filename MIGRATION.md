# Migration Guide

## Directory Structure Changes

The Supabase monorepo has been reorganized for better clarity and maintainability. Here are the key changes:

### Applications
- `apps/studio` → `platform/studio`
- `apps/cms` → `tools/cms`
- `apps/design-system` → `tools/design-system`
- `apps/ui-library` → `tools/ui-library`
- `apps/www` → `docs/www`
- `apps/docs` → `docs/reference`

### Packages
- `packages/pg-meta` → `packages/core/pg-meta`
- `packages/ai-commands` → `packages/shared/ai-commands`
- `packages/common` → `packages/shared/common`
- `packages/config` → `packages/shared/config`
- `packages/api-types` → `packages/shared/api-types`
- `packages/eslint-config-supabase` → `packages/integrations/eslint-config-supabase`

### Examples
- `examples/slack-clone` → `examples/starters/slack-clone`
- `examples/todo-list` → `examples/starters/todo-list`
- `examples/user-management` → `examples/starters/user-management`
- `examples/auth` → `examples/integrations/auth`
- `examples/ai` → `examples/integrations/ai`
- `examples/caching` → `examples/integrations/caching`

### Infrastructure
- `e2e/` → `infrastructure/testing/e2e/`
- `scripts/` → `internal/scripts/`
- `.github/` → `infrastructure/github/`
- `docker/` → `infrastructure/docker/`
- `supa-mdx-lint/` → `internal/linting/supa-mdx-lint/`

## Updated Commands

### Development
- `pnpm dev:studio-local` now uses `./platform/studio`
- `pnpm e2e` now uses `./infrastructure/testing/studio`

### Build
- All build commands remain the same but now use the new paths

### Formatting
- Prettier now checks all directories: `{platform,tools,docs,packages,blocks,examples,infrastructure}`

## Import Path Updates

If you have any imports referencing the old paths, update them:

```typescript
// Before
import { something } from '@supabase/studio'

// After (if needed)
import { something } from '@supabase/platform/studio'
```

Most internal imports should continue to work as the package names haven't changed, only their locations.

## CI/CD Updates

Make sure to update any CI/CD pipelines that reference the old directory paths.