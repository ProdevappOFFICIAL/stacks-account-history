# Project Structure

## Directory Organization

```
├── app/                    # Next.js App Router pages
│   ├── [address]/         # Dynamic route for address pages
│   ├── globals.css        # Global styles
│   ├── layout.tsx         # Root layout component
│   └── page.tsx           # Home page
├── components/            # Reusable React components
├── hooks/                 # Custom React hooks
├── lib/                   # Utility functions and API calls
└── public/               # Static assets
```

## Architecture Patterns

### File Naming Conventions
- **Components**: kebab-case (e.g., `txn-details.tsx`, `txns-list.tsx`)
- **Hooks**: prefix with `use-` (e.g., `use-stacks.ts`)
- **Utilities**: descriptive names (e.g., `stx-utils.ts`, `fetch-address-transactions.ts`)
- **Pages**: Next.js App Router conventions (`page.tsx`, `layout.tsx`)

### Component Organization
- **Client Components**: Use `"use client"` directive for interactivity
- **Server Components**: Default for data fetching and static content
- **Hooks**: Custom hooks in `/hooks` directory for reusable logic
- **Utilities**: Pure functions in `/lib` for business logic

### Import Patterns
- Use `@/` path alias for absolute imports from project root
- Import order: external libraries, then internal modules
- Destructure imports where appropriate

### Styling Conventions
- **Tailwind Classes**: Utility-first approach with responsive design
- **Component Styling**: Inline Tailwind classes, no separate CSS modules
- **Color Scheme**: Dark theme with gray-700 backgrounds, blue/red accent colors
- **Typography**: Inter font family, consistent text sizing

### State Management
- **Local State**: React useState for component-level state
- **Authentication**: Custom useStacks hook with UserSession
- **URL State**: Next.js router for navigation and address parameters

### Data Fetching
- **Server Components**: Direct async/await for initial data
- **Client Components**: Custom hooks for interactive data fetching
- **API Integration**: Stacks blockchain API calls in `/lib` utilities