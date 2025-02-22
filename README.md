<div align="center">
  <div align="center">
    <img src="./image/logo-devstage.svg" alt="Devstage" width="120">
  </div>
  
  <h1 align="center">DEVSTAGE-API</h1>

  <p align="center">
    <strong>High-performance Event Management API with Real-time Analytics</strong>
  </p>

  <p align="center">
    <img src="https://img.shields.io/github/license/JonatasT/devstage-api?style=flat-square&logo=opensourceinitiative&logoColor=white&color=002b54" alt="license">
    <img src="https://img.shields.io/github/last-commit/JonatasT/devstage-api?style=flat-square&logo=git&logoColor=white&color=002b54" alt="last-commit">
    <img src="https://img.shields.io/github/actions/workflow/status/JonatasT/devstage-api/ci.yml?style=flat-square&logo=githubactions&color=002b54" alt="build status">
  </p>
</div>

<br>

<div align="center">
  <img src="https://img.shields.io/badge/Fastify-000000.svg?style=for-the-badge&logo=Fastify&logoColor=white" alt="Fastify">
  <img src="https://img.shields.io/badge/TypeScript-3178C6.svg?style=for-the-badge&logo=TypeScript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Docker-2496ED.svg?style=for-the-badge&logo=Docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1.svg?style=for-the-badge&logo=PostgreSQL&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Redis-DC382D.svg?style=for-the-badge&logo=Redis&logoColor=white" alt="Redis">
  <img src="https://img.shields.io/badge/View_in-Scalar-2A4AEF?style=for-the-badge&logo=scalar&logoColor=white" alt="Scalar">
</div>

<br>

## 🚀 Features

- **Event Subscription System** - Manage event registrations with email validation
- **Real-time Analytics** - Track invite clicks and participant engagement
- **Leaderboard System** - Dynamic ranking of top participants
- **Unique Invite Links** - Trackable referral system with unique URLs
- **Rate Limiting** - Built-in protection against abuse
- **Redis Caching** - High-performance caching layer for frequent queries

## 📦 Project Structure

```sh
devstage-api/
├── src/
│   ├── routes/          # API endpoint handlers
│   ├── drizzle/         # Database schema and migrations
│   ├── functions/       # Core business logic
│   ├── redis/           # Redis client configuration
│   ├── env.ts           # Environment validation
│   └── server.ts        # Fastify server setup
├── tests/               # Integration/unit tests
├── docker-compose.yml   # Local development stack
├── drizzle.config.ts    # ORM configuration
└── tsup.config.ts       # TypeScript bundler config
```

## ⚡ Quick Start

### Prerequisites
- Node.js 18+
- Docker 20+
- PostgreSQL 15
- Redis 7

### Local Development
1. Clone repository:
   ```bash
   git clone https://github.com/JonatasT/devstage-api
   cd devstage-api
   ```

2. Setup environment:
   ```bash
   cp .env.example .env
   # Update .env with your credentials
   ```

3. Start services:
   ```bash
   docker-compose up -d
   ```

4. Install dependencies:
   ```bash
   npm install
   ```

5. Run migrations:
   ```bash
   npm run db:migrate
   ```

6. Start development server:
   ```bash
   npm run dev
   ```

### Production Deployment
```bash
docker-compose -f docker-compose.prod.yml up --build
```

## 📚 API Documentation

Explore our interactive API documentation powered by Scalar:

[![View in Scalar](https://img.shields.io/badge/View_in-Scalar-2A4AEF?style=for-the-badge&logo=scalar&logoColor=white)](https://www.scalar.com/ecosystem/playground?url=https://raw.githubusercontent.com/JonatasT/devstage-api/main/client.http)

```http
### Subscribe to Event
POST /api/events/subscribe
Content-Type: application/json

{
  "email": "user@example.com",
  "eventId": "EVENT_123"
}

### Get Ranking
GET /api/ranking?limit=10

### Access Invite Link
GET /api/invites/{code}

### Get User Analytics
GET /api/analytics/{userId}
```

## 🧪 Testing
Run the test suite with coverage:
```bash
npm test
# Or with watch mode
npm run test:watch
```

## 🤝 Contributing
We welcome contributions! Please follow these steps:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🙏 Acknowledgments
- Fastify team for the excellent web framework
- Drizzle ORM for type-safe database interactions
- Scalar team for API documentation tools
- Vercel team for deployment infrastructure