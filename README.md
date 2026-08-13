# JAngular CLI

> Enterprise-grade full-stack scaffolding for Angular + Spring Boot applications

[![npm version](https://img.shields.io/npm/v/jangular-cli.svg)](https://www.npmjs.com/package/jangular-cli)
[![npm downloads](https://img.shields.io/npm/dm/jangular-cli.svg)](https://www.npmjs.com/package/jangular-cli)
[![license](https://img.shields.io/npm/l/jangular-cli.svg)](https://github.com/nathangtg/jangular-cli/blob/master/LICENSE.txt)

Rapidly bootstrap production-ready full-stack applications with Angular 17+ frontend and Spring Boot 3 (Java 21) backend. Includes JWT authentication, multi-database support, Docker integration, and enterprise security out of the box.

## Features

- 🚀 **Quick Setup** - Generate complete full-stack projects in minutes
- 🔐 **Built-in Auth** - JWT authentication with refresh tokens and session management
- 🗄️ **Multi-Database** - Support for MySQL, PostgreSQL, and MSSQL
- 🐳 **Docker Ready** - Pre-configured containerization with docker-compose
- 🎨 **Modern Stack** - Angular 17+ with standalone components and Tailwind CSS
- ☕ **Spring Boot 3** - Java 21 with Spring Security and Flyway migrations
- 📊 **User Management** - Complete admin dashboard with role-based access control

## Installation

```bash
npm install -g jangular-cli
```

## Quick Start

```bash
# Create a new project
jangular init my-app

# Navigate to project
cd my-app

# Install dependencies
npm run install:all

# Start development servers
npm run start:backend    # Spring Boot on :8080
npm run start:frontend   # Angular on :4200
```

Visit `http://localhost:4200` to see your application.

## Requirements

- Node.js ≥ 18
- Java ≥ 21
- Maven 3.x
- Docker (optional)

Check if your system meets requirements:

```bash
npx jangular --test
```

## CLI Commands

### Initialize Project

```bash
jangular init <project-name> [options]

Options:
  -g, --group-id <groupId>      Java group ID (default: com.example)
  -a, --artifact-id <id>        Java artifact ID (default: backend)
```

### Docker Management

```bash
jangular docker
```

Interactive menu to manage Docker services, view logs, and check health status.

### Build Project

```bash
jangular build [options]

Options:
  -b, --backend    Build backend only
  -f, --frontend   Build frontend only
  -p, --prod       Production build
```

### Run Tests

```bash
jangular test [options]

Options:
  -b, --backend    Test backend only
  -f, --frontend   Test frontend only
```

## Project Structure

```
my-app/
├── backend/              # Spring Boot application
│   ├── src/
│   ├── pom.xml
│   └── Dockerfile
├── frontend/             # Angular application
│   ├── src/
│   ├── package.json
│   └── Dockerfile
├── docker-compose.yml    # Container orchestration
└── package.json          # Root scripts
```

## What's Included

### Backend (Spring Boot)
- JWT authentication & authorization
- User management with CRUD operations
- Role-based access control (RBAC)
- Account lockout and password policies
- Session tracking and login history
- Flyway database migrations
- Global exception handling
- RESTful API architecture

### Frontend (Angular)
- Standalone components architecture
- Pre-built auth UI (login, register, reset password)
- User management dashboard
- HTTP interceptors for token handling
- Route guards for protected pages
- Reactive forms with validation
- Tailwind CSS styling
- Responsive design

### DevOps
- Multi-container Docker setup
- Development and production profiles
- Database GUI tools (phpMyAdmin/pgAdmin)
- Health check endpoints
- Volume persistence configuration

## Documentation

Full documentation available at **[jangular.nathangtg.com](https://jangular.nathangtg.com)**

- [Getting Started Guide](https://jangular.nathangtg.com/getting-started)
- [CLI Commands](https://jangular.nathangtg.com/commands)
- [Backend Guide](https://jangular.nathangtg.com/backend)
- [Frontend Guide](https://jangular.nathangtg.com/frontend)
- [Docker Deployment](https://jangular.nathangtg.com/docker)
