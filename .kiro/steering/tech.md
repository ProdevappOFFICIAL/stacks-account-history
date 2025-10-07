# Technology Stack

## Framework & Runtime
- **Next.js 15.1.5** - React framework with App Router
- **React 19** - UI library with latest features
- **TypeScript 5** - Type-safe JavaScript development
- **Node.js 20+** - Runtime environment

## Stacks Integration
- **@stacks/connect 7.10.0** - Wallet connection and authentication
- **@stacks/transactions 7.0.2** - Address validation and transaction utilities

## Styling & UI
- **Tailwind CSS 3.4.1** - Utility-first CSS framework
- **Lucide React** - Icon library
- **Inter Font** - Typography via next/font

## Development Tools
- **ESLint 9** - Code linting with Next.js config
- **PostCSS 8** - CSS processing

## Common Commands

### Development
```bash
npm run dev          # Start development server on localhost:3000
npm run build        # Build production bundle
npm run start        # Start production server
npm run lint         # Run ESLint checks
```

### Package Management
```bash
npm install          # Install dependencies
npm ci               # Clean install from lock file
```

## Build Configuration
- Uses Next.js App Router (not Pages Router)
- TypeScript strict mode enabled
- Tailwind configured for app/, components/, and pages/ directories
- ESLint extends Next.js recommended rules