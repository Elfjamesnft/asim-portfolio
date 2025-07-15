# Project Structure

## Overview
This document outlines the complete structure of the Asim Shaikh AI Portfolio application, a full-stack TypeScript web application built with React and Express.js.

## Root Directory
```
asim-shaikh-ai-portfolio/
├── client/                    # Frontend React application
├── server/                    # Backend Express application  
├── shared/                    # Shared types and schemas
├── dist/                      # Production build output
├── attached_assets/           # User-uploaded assets
├── node_modules/              # Dependencies
├── package.json               # Project configuration
├── package-lock.json          # Dependency lock file
├── tsconfig.json             # TypeScript configuration
├── vite.config.ts            # Vite build configuration
├── tailwind.config.ts        # Tailwind CSS configuration
├── postcss.config.js         # PostCSS configuration
├── drizzle.config.ts         # Database configuration
├── components.json           # Shadcn/ui configuration
├── .env.example              # Environment variables template
├── .gitignore                # Git ignore rules
├── README.md                 # Main documentation
├── DEPLOYMENT.md             # Deployment instructions
├── CONTRIBUTING.md           # Contribution guidelines
├── PROJECT_STRUCTURE.md      # This file
└── replit.md                 # Replit-specific documentation
```

## Client Directory (`/client`)
Frontend React application with modern tooling and UI components.

```
client/
├── src/
│   ├── components/           # Reusable UI components
│   │   ├── sections/         # Page sections
│   │   │   ├── hero.tsx      # Hero section component
│   │   │   ├── about.tsx     # About section component
│   │   │   ├── projects.tsx  # Projects showcase
│   │   │   ├── technology.tsx # Technology stack
│   │   │   ├── partnership.tsx # Partnership section
│   │   │   ├── contact.tsx   # Contact form
│   │   │   └── footer.tsx    # Footer component
│   │   └── ui/               # Shadcn/ui components
│   │       ├── button.tsx    # Button component
│   │       ├── card.tsx      # Card component
│   │       ├── form.tsx      # Form components
│   │       ├── input.tsx     # Input component
│   │       ├── textarea.tsx  # Textarea component
│   │       ├── toast.tsx     # Toast notifications
│   │       ├── toaster.tsx   # Toast container
│   │       ├── navigation.tsx # Navigation component
│   │       ├── feature-card.tsx # Feature card component
│   │       ├── project-card.tsx # Project card component
│   │       └── [30+ other UI components]
│   ├── hooks/                # Custom React hooks
│   │   ├── use-mobile.tsx    # Mobile detection hook
│   │   └── use-toast.ts      # Toast notification hook
│   ├── lib/                  # Utility functions
│   │   ├── utils.ts          # General utilities
│   │   └── queryClient.ts    # React Query configuration
│   ├── pages/                # Page components
│   │   ├── home.tsx          # Home page
│   │   └── not-found.tsx     # 404 page
│   ├── App.tsx               # Main app component with routing
│   ├── main.tsx              # Application entry point
│   └── index.css             # Global styles and themes
├── index.html                # HTML template
└── public/                   # Static assets (if needed)
```

## Server Directory (`/server`)
Backend Express.js application with TypeScript and database integration.

```
server/
├── index.ts                  # Server entry point
├── routes.ts                 # API route handlers
├── storage.ts                # Database operations and interfaces
└── vite.ts                   # Vite integration for development
```

### Key Server Files

**`index.ts`** - Express server setup with:
- Middleware configuration
- Session management
- Error handling
- Port configuration

**`routes.ts`** - API endpoints:
- `POST /api/contact` - Contact form submissions
- `GET /api/contact` - Retrieve contact submissions
- Static file serving in production

**`storage.ts`** - Database layer:
- `IStorage` interface for database operations
- `MemStorage` implementation for in-memory storage
- PostgreSQL integration ready

**`vite.ts`** - Development server integration:
- Hot module replacement
- Static file serving
- Development middleware

## Shared Directory (`/shared`)
Common TypeScript types and database schemas used by both frontend and backend.

```
shared/
└── schema.ts                 # Database schemas and types
    ├── User schema          # User data structure
    ├── ContactSubmission    # Contact form data
    └── Zod validation schemas
```

## Database Schema
Using Drizzle ORM with PostgreSQL:

### Tables
- **users** - User accounts (prepared for future use)
- **contact_submissions** - Partnership inquiry submissions

### Types
- `User` / `InsertUser` - User data types
- `ContactSubmission` / `InsertContactSubmission` - Contact form types

## Build Output (`/dist`)
Production build artifacts:

```
dist/
├── public/                   # Built frontend assets
│   ├── index.html           # Entry HTML
│   ├── assets/              # CSS, JS, and other assets
│   └── [additional static files]
└── index.js                 # Bundled server code
```

## Configuration Files

### TypeScript Configuration (`tsconfig.json`)
- Strict type checking enabled
- Path aliases configured (`@/`, `@shared/`)
- Modern ES modules support

### Vite Configuration (`vite.config.ts`)
- React plugin setup
- Path aliases configuration
- Development server settings
- Build optimization

### Tailwind Configuration (`tailwind.config.ts`)
- Custom color scheme
- Dark mode support
- Component integration
- Animation utilities

### Database Configuration (`drizzle.config.ts`)
- PostgreSQL connection
- Migration settings
- Schema management

## Development Workflow

### Development Mode
1. `npm run dev` starts:
   - Express server on port 5000
   - Vite dev server with HMR
   - TypeScript compilation
   - Hot reloading for both frontend and backend

### Production Build
1. `npm run build` creates:
   - Frontend build in `dist/public/`
   - Backend bundle in `dist/index.js`
   - Optimized assets and code splitting

### Database Management
- `npm run db:push` - Push schema changes
- Drizzle Kit for migrations
- PostgreSQL with Neon DB support

## Key Features

### Frontend Features
- **Responsive Design** - Mobile-first approach
- **Dark Theme** - Black/charcoal grey color scheme
- **3D Effects** - Card hover animations and depth
- **Glass Morphism** - Modern UI with backdrop blur
- **Smooth Animations** - Framer Motion integration
- **Type Safety** - Full TypeScript coverage

### Backend Features
- **RESTful API** - Clean endpoint structure
- **Database Integration** - PostgreSQL with Drizzle ORM
- **Session Management** - Express sessions
- **Error Handling** - Comprehensive error middleware
- **Type Safety** - Shared types with frontend

### Performance Optimizations
- **Code Splitting** - Automatic route-based splitting
- **Tree Shaking** - Unused code elimination
- **CSS Purging** - Tailwind CSS optimization
- **Bundle Optimization** - Vite production builds

## Security Considerations
- Environment variable protection
- SQL injection prevention (Drizzle ORM)
- XSS protection
- Session security
- Input validation with Zod

## Deployment Ready
- Docker containerization support
- Environment configuration
- Production build optimization
- Database migration support
- Static asset serving

This structure provides a solid foundation for a modern, scalable web application with excellent developer experience and production readiness.
