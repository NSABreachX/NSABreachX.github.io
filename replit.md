# EuroBot Virtual Economy System

## Overview

EuroBot is a comprehensive virtual economy system inspired by Discord bots, built as a full-stack web application. The system provides users with a complete virtual economy experience including currency management, banking operations, job systems, gambling games, a marketplace, and administrative tools. Users can earn virtual euros through daily rewards and various jobs, spend money in a virtual shop, play games like gambling and blackjack, and manage their finances through a banking system.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite for development and build tooling
- **UI Library**: Shadcn/ui components with Radix UI primitives for accessibility
- **Styling**: Tailwind CSS with custom Discord-inspired design system and color scheme
- **State Management**: TanStack Query for server state management and caching
- **Routing**: Wouter for client-side routing
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Session Management**: Express sessions with PostgreSQL store for persistence
- **Authentication**: Replit OpenID Connect (OIDC) authentication system
- **API Design**: RESTful API endpoints with JSON request/response format

### Database Schema Design
- **Users Table**: Core user data with balance, bank amount, job tracking, and daily reward timestamps
- **Shop Items**: Virtual marketplace with products, descriptions, and pricing
- **Transactions**: Complete financial history tracking for all money movements
- **Purchases**: User purchase history with status tracking (pending, completed, cancelled)
- **Game History**: Records of gambling and gaming activities with outcomes
- **Sessions**: Required for Replit authentication persistence

### Authentication & Authorization
- **Provider**: Replit OIDC for seamless integration with the platform
- **Session Storage**: PostgreSQL-backed sessions with 7-day expiration
- **Route Protection**: Middleware-based authentication checks on all protected endpoints
- **User Management**: Automatic user creation on first login with default starting balance

### Virtual Economy Systems
- **Banking**: Deposit/withdrawal system between wallet and bank accounts
- **Daily Rewards**: Time-gated daily currency claims with persistence checking
- **Job System**: Multiple job types with cooldown periods and variable earnings
- **Gaming**: Gambling with multipliers and blackjack with standard rules
- **Marketplace**: Shop system with admin-managed inventory and purchase requests
- **Transfers**: Peer-to-peer currency transfers between users

## External Dependencies

### Database
- **Neon PostgreSQL**: Serverless PostgreSQL database with connection pooling
- **Connection**: Uses @neondatabase/serverless with WebSocket constructor override

### Authentication
- **Replit OIDC**: OpenID Connect integration for user authentication
- **Session Store**: connect-pg-simple for PostgreSQL session persistence

### UI Components
- **Radix UI**: Comprehensive set of accessible React components
- **Lucide React**: Icon library for consistent iconography
- **Font Awesome**: Additional icons for Discord-style interface elements

### Development Tools
- **Vite**: Fast development server and build tool with React plugin
- **TypeScript**: Type safety across frontend and backend
- **ESBuild**: Production bundling for server-side code
- **Replit Plugins**: Development environment integration and error handling