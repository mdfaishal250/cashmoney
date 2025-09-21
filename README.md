# CASH MONEY - Fintech Multi-Portal Platform

[![CI/CD Pipeline](https://github.com/YOUR_USERNAME/cashmoney-fintech/workflows/CI/CD%20Pipeline/badge.svg)](https://github.com/YOUR_USERNAME/cashmoney-fintech/actions)
[![codecov](https://codecov.io/gh/YOUR_USERNAME/cashmoney-fintech/branch/main/graph/badge.svg)](https://codecov.io/gh/YOUR_USERNAME/cashmoney-fintech)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive fintech multi-portal platform with role-based access control and integrated financial services.

## 🚀 Features

- **Role-Based Multi-Portal System**
  - Admin Portal (Full Control)
  - Whitelabel Portal (Partner Management)
  - B2B Admin Portal (Business Operations)
  - Distributor & Retailer Interfaces

- **Integrated Financial Services**
  - Mobile & D2H Recharge
  - BBPS Bill Payments
  - AEPS Banking Services
  - Domestic Money Transfer
  - Payin/Payout Services
  - Travel Ticketing

- **Security & Compliance**
  - JWT Authentication
  - Role-Based Access Control
  - Encrypted Data Storage
  - Audit Logging

## 🛠 Technology Stack

### Frontend
- React 18 with TypeScript
- Tailwind CSS
- React Router v6
- Chart.js

### Backend
- Node.js with Express
- PostgreSQL Database
- Sequelize ORM
- JWT Authentication

### DevOps
- Docker & Docker Compose
- GitHub Actions CI/CD
- Playwright E2E Testing

## 📋 Prerequisites

- Node.js >= 18.0.0
- PostgreSQL >= 13
- Docker & Docker Compose
- Git

## 🚀 Quick Start

### 1. Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/cashmoney-fintech.git
cd cashmoney-fintech
```

### 2. Environment Setup

Copy the example environment files and update them with your secrets and configuration:

```bash
cp .env.example .env
touch .env.development .env.production
cp .env.development.example .env.development
cp .env.production.example .env.production
```

Edit `.env`, `.env.development`, and `.env.production` with your actual credentials and API keys.

### 3. Install Dependencies

Install all dependencies for the monorepo:

```bash
npm install
```

To install dependencies for individual workspaces:

```bash
npm install -w apps/web
npm install -w apps/api
```

### 4. Database Setup

Make sure PostgreSQL is running and accessible. You can use Docker Compose to start the database service:

```bash
docker-compose up db
```

If you have an `init.sql` file in `./database/`, it will be executed automatically to initialize your database.

Update your `.env` files with the correct `DATABASE_URL` for your environment.

### 5. Start Development

You can start all services using Docker Compose:

```bash
docker-compose up
```

Or, to run the frontend and backend locally without Docker:

```bash
npm run dev
```

This will start both the API and web servers in development mode.

Access the application:
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000

## 🧪 Testing

Run all tests for both frontend and backend:

```bash
npm test
```

To run tests for a specific workspace:

```bash
npm run test -w apps/web
npm run test -w apps/api
```

For end-to-end tests (Playwright):

```bash
npm run test:e2e
```

## 🚀 Deployment

### Production Build

Build the frontend and backend for production:

```bash
npm run build
```

Or build individually:

```bash
npm run build -w apps/web
npm run build -w apps/api
```

### Docker Compose (Production)

Start all services in production mode:

```bash
docker-compose -f docker-compose.yml up -d
```

Make sure your `.env.production` file is configured with production secrets and URLs.

### Docker Deployment

Build and push Docker images for frontend and backend:

```bash
# Build and push frontend image
DOCKER_BUILDKIT=1 docker build -t your-dockerhub-username/cashmoney-frontend:latest ./apps/web

docker push your-dockerhub-username/cashmoney-frontend:latest

# Build and push backend image
DOCKER_BUILDKIT=1 docker build -t your-dockerhub-username/cashmoney-backend:latest ./apps/api

docker push your-dockerhub-username/cashmoney-backend:latest
```

Update your deployment configuration to use these images in your cloud provider or orchestration platform.

## 📖 API Documentation

API documentation is available at `/api/docs` when running the development server.

Import the Postman collection from `docs/postman/` for testing.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support, please open an issue or contact [your-email@domain.com](mailto:your-email@domain.com).
