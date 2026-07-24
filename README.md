# 🧪 Prisma Project Learning

A backend learning project built with **Express**, **Prisma ORM**, and **PostgreSQL**, focused on practicing schema design, relations, transactions, authentication, and RESTful API patterns.

**📦 Repository:** [github.com/Saddam2508/prisma_project_learning](https://github.com/Saddam2508/prisma_project_learning)

---

## 📖 About

This is a hands-on learning repository built to strengthen backend development skills using **Prisma ORM** with a **PostgreSQL** database. It explores core backend concepts including:

- Designing relational schemas (Users, Posts, Comments, Subscriptions)
- Prisma queries — `findMany`, `include`, `aggregate`, `$transaction`
- JWT-based authentication and password hashing
- RESTful API design using Express
- Query features like search, filtering, sorting, and pagination

---

## 🧰 Tech Stack

| Category | Technology |
|---|---|
| Runtime | Node.js |
| Language | TypeScript |
| Framework | Express 5 |
| ORM | Prisma 7 (`@prisma/client`, `@prisma/adapter-pg`) |
| Database | PostgreSQL (`pg`) |
| Authentication | JWT (`jsonwebtoken`), `bcryptjs` for password hashing |
| Middleware | `cors`, `cookie-parser` |
| Dev Tooling | `tsx` (TypeScript execution & watch mode) |
| HTTP Status Codes | `http-status` |

---

## 📁 Project Structure

```
prisma_project_learning/
├── prisma/
│   ├── schema.prisma       # Database schema definition
│   └── generated/           # Generated Prisma Client
├── src/
│   ├── server.ts             # App entry point
│   ├── lib/
│   │   └── prisma.ts          # Prisma Client instance
│   └── modules/               # Feature-based modules (e.g., post, user)
│       └── post/
│           ├── post.service.ts
│           ├── post.controller.ts
│           ├── post.route.ts
│           └── post.interface.ts
├── prisma.config.ts         # Prisma configuration
├── tsconfig.json
└── package.json
```

> Note: Exact folder contents may evolve as the project grows — refer to the repository for the latest structure.

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ installed
- A running PostgreSQL database instance

### Installation

```bash
git clone https://github.com/Saddam2508/prisma_project_learning.git
cd prisma_project_learning
npm install
```

### Environment Variables

Create a `.env` file in the root directory:

```
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE_NAME"
JWT_SECRET="your_jwt_secret_here"
```

### Generate Prisma Client

```bash
npx prisma generate
```

### Run Database Migrations

```bash
npx prisma migrate dev
```

### Run the Development Server

```bash
npm run dev
```

This starts the server using `tsx watch`, so it automatically restarts on file changes.

### Production Build & Start

```bash
npm run build
npm start
```

---

## 🗄️ Explore the Database

To visually browse and edit your database using Prisma Studio:

```bash
npx prisma studio
```

---

## 🔑 Key Concepts Practiced

- **Relational schema design** — modeling one-to-many and many-to-many relationships (e.g., Users → Posts → Comments)
- **Transactions** — using `prisma.$transaction()` for atomic operations, such as incrementing view counts alongside fetching a post
- **Aggregations** — using `count()`, `aggregate()`, and `Promise.all()` for building dashboard-style statistics
- **Dynamic filtering & search** — building flexible `WHERE` clauses with `AND`/`OR` conditions based on query parameters
- **Pagination & sorting** — implementing `skip`/`take` based pagination with dynamic `orderBy`
- **Authentication** — password hashing with `bcryptjs` and stateless auth using JWT

---

## 📄 License

ISC

---

## 👤 Author

**Md Saddam Hossain**
GitHub: [@Saddam2508](https://github.com/Saddam2508)
