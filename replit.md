# Overview

Dor is a traditional Indian matrimonial application built with modern web technologies. The app focuses on connecting users for marriage while respecting traditional values and cultural sensitivity. It features a React-based frontend with TypeScript, Express.js backend, PostgreSQL database with Drizzle ORM, and integrates Replit authentication system.

The application supports both authenticated users and guest mode functionality, allowing users to explore profiles for a limited time before signing up. The system includes profile creation, partner preferences, matchmaking, messaging, and interest-based matching features.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript
- **Routing**: Wouter for client-side navigation
- **State Management**: TanStack Query (React Query) for server state management
- **UI Components**: Custom component library built with Radix UI primitives and Tailwind CSS
- **Styling**: Tailwind CSS with custom color scheme (saffron/brown theme for Indian aesthetic)
- **Build Tool**: Vite for development and production builds

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM with PostgreSQL
- **Authentication**: Replit's OpenID Connect (OIDC) authentication system
- **Session Management**: Express sessions with PostgreSQL store
- **API Design**: RESTful API with consistent error handling

## Database Design
The database uses PostgreSQL with the following key entities:
- **Users**: Basic user information from Replit auth
- **Profiles**: Detailed matrimonial profiles with personal information
- **Partner Preferences**: User's preferences for potential matches
- **Matches**: Interest exchanges between users
- **Messages**: Chat functionality between matched users
- **Guest Sessions**: Time-limited access for non-registered users
- **Sessions**: Authentication session storage

## Authentication & Authorization
- **Primary Auth**: Replit OIDC integration with automatic user provisioning
- **Guest Mode**: Temporary session-based access with 10-day expiration
- **Session Storage**: PostgreSQL-backed sessions using connect-pg-simple
- **Security**: HTTP-only cookies, CSRF protection, secure session handling

## Key Features Architecture
- **Profile Browsing**: Filtered profile discovery with customizable search parameters
- **Matchmaking System**: Interest-based matching with mutual consent workflow
- **Real-time Messaging**: Chat system between matched users
- **Guest Experience**: Limited-time access to encourage sign-ups
- **Responsive Design**: Mobile-first approach with adaptive layouts

# External Dependencies

## Core Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL client for database connectivity
- **drizzle-orm**: TypeScript-first ORM for database operations
- **drizzle-kit**: Database migration and schema management tools

## Authentication & Session Management
- **openid-client**: OpenID Connect client for Replit authentication
- **passport**: Authentication middleware framework
- **express-session**: Session management for Express
- **connect-pg-simple**: PostgreSQL session store adapter

## Frontend Libraries
- **@tanstack/react-query**: Server state management and caching
- **@radix-ui/react-***: Accessible UI component primitives
- **react-hook-form**: Form state management and validation
- **@hookform/resolvers**: Form validation resolvers
- **zod**: TypeScript-first schema validation
- **wouter**: Minimalist routing library
- **tailwindcss**: Utility-first CSS framework

## Development Tools
- **vite**: Fast build tool and development server
- **typescript**: Static type checking
- **tsx**: TypeScript execution engine
- **esbuild**: Fast JavaScript bundler for production

## UI Components & Styling
- **class-variance-authority**: CSS class composition utility
- **clsx**: Conditional className utility
- **tailwind-merge**: Tailwind CSS class merging
- **lucide-react**: Icon library
- **date-fns**: Date manipulation utilities

## Replit-Specific Integrations
- **@replit/vite-plugin-runtime-error-modal**: Development error overlay
- **@replit/vite-plugin-cartographer**: Replit development tools integration

The application is designed to run seamlessly on Replit's infrastructure while maintaining the flexibility to deploy elsewhere if needed.