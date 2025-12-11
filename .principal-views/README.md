# Supabase Architecture Canvas - Color Coded

## 🎨 Node Color Legend

| Color | Category | Components |
|-------|----------|------------|
| 🟢 **Green** | Applications | Studio, Marketing Site, Documentation, CMS, Design System, UI Library |
| 🟡 **Yellow** | Core Packages | Postgres Meta, Common, API Types, UI Components, UI Patterns |
| 🟠 **Orange** | Tools | AI Commands, Generator |
| 🔵 **Blue** | Infrastructure | Shared Data, Config, TS Config, ESLint Config |
| 🟣 **Purple** | External Services | PostgreSQL, Auth, Storage, Realtime, Edge Functions |

## 🔗 Edge Color & Style Legend

| Style | Color | Relationship Type | Description |
|-------|--------|------------------|-------------|
| **Solid Line** | 🟢 Green | Uses | Direct dependencies and service usage |
| **Dashed Line** | 🟡 Yellow | Imports | Code imports and module dependencies |
| **Dotted Line** | 🔵 Blue | Uses | Data usage and configuration |
| **Animated Line** | 🟡 Yellow | Communicates | API calls and real-time communication |
| **Solid Line** | 🟣 Purple | Extends | Inheritance and extension relationships |

## 📊 Architecture Overview

The color-coded architecture provides immediate visual understanding of:

### **Application Layer (Green)**
- User-facing applications and interfaces
- Studio: Main dashboard for project management
- Marketing Site, Documentation, CMS: Content and documentation
- Design System, UI Library: User interface components

### **Core Layer (Yellow)**
- Essential packages and libraries
- Postgres Meta: Database management layer
- Common, API Types: Shared utilities and type definitions
- UI Components, UI Patterns: Reusable interface elements

### **Tools Layer (Orange)**
- Development and automation tools
- AI Commands: AI-powered development assistance
- Generator: Code generation utilities

### **Infrastructure Layer (Blue)**
- Configuration and build tools
- Shared Data: Common configuration data
- Config, TS Config, ESLint Config: Build and development setup

### **External Services (Purple)**
- Third-party and platform services
- PostgreSQL: Primary database
- Auth, Storage, Realtime, Edge Functions: Core platform services

## 🔄 Key Relationships

- **Green solid lines**: Studio depends on core packages and external services
- **Yellow dashed lines**: Applications import shared utilities and UI components
- **Purple solid lines**: UI components extend base libraries
- **Yellow animated lines**: Real-time API communication between Studio and external services
- **Blue dotted lines**: Tools and infrastructure use shared configuration data

## 📁 Files Generated

- `.vgc/library.yaml` - Component definitions with colors
- `.vgc/architecture.canvas` - Canvas configuration with color coding
- `.vgc/architecture-viewer.html` - Interactive visual viewer

Open `architecture-viewer.html` in a browser to see the fully color-coded architecture diagram!