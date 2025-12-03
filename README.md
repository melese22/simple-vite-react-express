# Simple Vite React Express

<p align="center">
  <img src="./public/template-logo.png" alt="modern-fullstack-template-logo" height="200">
</p>

<p align="center">
    <img src="https://img.shields.io/badge/Vite-646CFF.svg?style=flat-square&logo=Vite&logoColor=white" alt="Vite 6+">
    <img src="https://img.shields.io/badge/React-61DAFB.svg?style=flat-square&logo=React&logoColor=black" alt="React 19">
    <img src="https://img.shields.io/badge/Express-000000.svg?style=flat-square&logo=Express&logoColor=white" alt="Express">
    <img src="https://img.shields.io/badge/postgresql-4169e1.svg?style=flat-square&logo=PostgreSQL&logoColor=white" alt="PostgreSQL">
    <img src="https://img.shields.io/badge/Prisma-2D3748.svg?style=flat-square&logo=Prisma&logoColor=white" alt="Prisma">
    <br>
    <img src="https://img.shields.io/badge/TypeScript-3178C6.svg?style=flat-square&logo=TypeScript&logoColor=white" alt="TypeScript Ready">
    <img src="https://img.shields.io/badge/Material--UI-007FFF.svg?style=flat-square&logo=MUI&logoColor=white" alt="Material-UI">
    <img src="https://img.shields.io/badge/ESLint-4B32C3.svg?style=flat-square&logo=ESLint&logoColor=white" alt="ESLint">
    <img src="https://img.shields.io/badge/Prettier-F7B93E.svg?style=flat-square&logo=Prettier&logoColor=black" alt="Prettier">
    <img src="https://img.shields.io/badge/Nodemon-76D04B.svg?style=flat-square&logo=Nodemon&logoColor=white" alt="Nodemon">
</p>

A full-stack starter with working examples instead of empty files. I built this because I was tired of cloning repos with just authentication and a "Hello World" - this one has actual CRUD operations, relationships, and form handling so you can see how things connect together.

<div align="center">
<img src="screenshots/homepage.png" alt="Homepage" height="400">
</div>

## Quick Start

```bash
# Clone and setup your project
git clone git@github.com:Avinava/simple-vite-react-express.git your-project-name
cd your-project-name

# Install dependencies (npm, yarn, or pnpm)
npm install
# or
yarn install
# or
pnpm install

# Environment setup
cp example.env .env
# Edit .env with your database credentials

# Database initialization
npm run db:setup
# or manually:
# npx prisma migrate dev
# npx prisma generate

# Start development servers
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) and you'll see what I mean. Instead of placeholder content, you get:
- Contact management (create, edit, delete, view details)
- Task tracking with status changes and priorities
- Project organization with member assignments
- Material-UI components that actually do something
- PostgreSQL with foreign keys and relationships working

It's basically a simple CRM to demonstrate how the pieces fit together. Good for learning or as a starting point for something bigger.

## What This Demonstrates

### Actual Working Features
Most starter templates have a login page and then... nothing. Here you can immediately see how CRUD operations work, how forms connect to the backend, how to handle validation errors, and how the database relationships actually function. It's the stuff you usually have to figure out yourself.

### Common Patterns You'll Need
The code shows how to structure a multi-model application: contacts, tasks, and projects with relationships between them. You can see how to handle one-to-many (contact has many tasks) and many-to-many (projects have many contacts) relationships. Plus practical things like status enums, optional fields, and proper foreign keys.

### Full Stack Integration
The frontend and backend actually talk to each other properly. API routes that return consistent response formats, error handling that shows meaningful messages, form validation on both client and server. You can see the complete data flow instead of guessing how pieces connect.

### Development Setup That Works
Everything is configured to work together from the start. Vite for fast frontend builds, Nodemon for backend auto-restart, Prisma for database management, and proper environment handling. No hunting for the right configuration or fighting with build tools.

## Project Structure

```
├── src/
│   ├── client/              # Frontend (React + Vite)
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Route-based page components
│   │   ├── hooks/           # Custom React hooks
│   │   ├── utils/           # Client-side utilities
│   │   └── theme/           # Material-UI theme config
│   │
│   └── server/              # Backend (Express + Node.js)
│       ├── routes/          # API route definitions
│       ├── services/        # Business logic layer
│       ├── middleware/      # Express middleware
│       ├── utils/           # Server utilities
│       └── config/          # Configuration files
│
├── prisma/                  # Database (Prisma ORM)
│   ├── schema.prisma        # Database schema
│   ├── migrations/          # Database migrations
│   └── seed.js              # Database seeding
│
├── docs/                    # Documentation
├── public/                  # Static assets
└── scripts/                 # Build & deployment scripts
```

## Available Scripts

### Development

```bash
npm run dev          # Start both client and server
npm run client       # Start only frontend (Vite)
npm run server       # Start only backend (Nodemon)
npm run preview      # Preview production build
```

### Database

```bash
npm run db:setup     # Initialize database (migrate + generate)
npm run db:migrate   # Run database migrations
npm run db:generate  # Generate Prisma client
npm run db:studio    # Open Prisma Studio
npm run db:reset     # Reset database
npm run db:seed      # Seed database with sample data
```


