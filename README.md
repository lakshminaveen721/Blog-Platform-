# 📝 Blog Platform Backend

A secure and scalable backend for a blogging platform using Node.js, Express, PostgreSQL, Redis, and JWT.

## Features
- User registration & login
- JWT-based authentication
- Create, view, and delete blog posts
- PostgreSQL + Redis integration
- Docker & Heroku ready

## How to Run

### Option 1: Local Development
1. Create `.env` file with:
```
DATABASE_URL=postgres://user:password@localhost:5432/blogdb
JWT_SECRET=supersecret
```

2. Install dependencies and start server:
```bash
npm install
npm start
```

3. Setup PostgreSQL using `schema.sql`

### Option 2: Docker
```bash
docker-compose up --build
```

### Option 3: Heroku
```bash
heroku create
heroku addons:create heroku-postgresql:hobby-dev
git push heroku master
```

## API Endpoints
| Method | Endpoint         | Description           |
|--------|------------------|-----------------------|
| POST   | /api/auth/register | Register a new user |
| POST   | /api/auth/login    | Login and get token |
| GET    | /api/posts         | Get all posts       |
| POST   | /api/posts         | Create a post (auth)|
| DELETE | /api/posts/:id     | Delete own post     |