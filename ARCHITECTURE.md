# Supabase Architecture Organization

## Overview
This document outlines the reorganized Supabase monorepo structure for better clarity and maintainability.

## New Directory Structure

```
supabase/
├── platform/                    # Core platform applications
│   ├── studio/                  # Main dashboard application
│   ├── api/                     # Platform API services
│   └── admin/                   # Internal admin tools
│
├── tools/                       # Development and design tools
│   ├── design-system/           # UI component library
│   ├── ui-library/              # Public UI components
│   └── cms/                     # Content management system
│
├── docs/                        # Documentation sites
│   ├── reference/               # API reference docs
│   ├── guides/                  # User guides and tutorials
│   └── www/                     # Marketing website
│
├── packages/                    # Shared libraries and utilities
│   ├── core/                    # Core platform packages
│   │   ├── auth-js/
│   │   ├── realtime-js/
│   │   └── postgrest-js/
│   ├── shared/                  # Shared utilities
│   │   ├── common/
│   │   ├── config/
│   │   └── types/
│   └── integrations/            # Third-party integrations
│       └── sentry/
│
├── examples/                    # Example applications and templates
│   ├── starters/                # Quick start templates
│   ├── integrations/            # Integration examples
│   └── tutorials/               # Tutorial code
│
├── blocks/                      # Reusable UI blocks (Vue, etc.)
│   └── vue/
│
├── internal/                    # Internal tools and scripts
│   ├── scripts/
│   ├── generators/
│   └── linting/
│
└── infrastructure/              # DevOps and deployment
    ├── docker/
    ├── github/
    └── testing/
        └── e2e/
```

## Key Improvements

### 1. Clear Separation of Concerns
- **Platform/**: Core production applications
- **Tools/**: Development and design utilities
- **Docs/**: All documentation sites
- **Packages/**: Shared libraries organized by purpose

### 2. Logical Package Grouping
- **Core/**: Essential platform packages (auth, realtime, etc.)
- **Shared/**: Common utilities and configurations
- **Integrations/**: Third-party service integrations

### 3. Better Examples Organization
- **Starters/**: Quick start templates
- **Integrations/**: Service integration examples
- **Tutorials/**: Step-by-step tutorial code

### 4. Internal vs External
- **Internal/**: Internal development tools
- **Infrastructure/**: DevOps and deployment configurations

## Migration Plan

### Phase 1: Create New Structure
1. Create new top-level directories
2. Move existing directories to new locations
3. Update workspace configuration

### Phase 2: Update Configurations
1. Update package.json scripts
2. Update pnpm-workspace.yaml
3. Update turbo.json configuration
4. Update import paths

### Phase 3: Testing and Validation
1. Run full test suite
2. Validate all builds
3. Update CI/CD pipelines

## Benefits

1. **Improved Navigation**: Easier to find relevant code
2. **Better Onboarding**: New contributors can understand structure faster
3. **Clearer Dependencies**: More obvious package relationships
4. **Scalable Structure**: Better organization for future growth
5. **Reduced Cognitive Load**: Clearer mental model of the codebase