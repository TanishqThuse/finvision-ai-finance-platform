# 🧠 FinVisionAI – AI Finance Platform

A scalable, secure, and intelligent **AI-powered financial management platform** built with **Next.js**, **TypeScript**, and **Supabase**.  
It integrates **Clerk**, **Arcjet**, and **Inngest** to deliver authentication, database management, advanced security, and automated background workflows.

---

## 🚀 Overview

**FinVisionAI** enables seamless financial automation — from user authentication and transaction management to AI-driven analytics — with a clean, modular architecture.

It combines:
- **Next.js (TypeScript)** for a high-performance, SEO-optimized frontend.
- **Supabase + Prisma** for a robust and easily migratable SQL database layer.
- **Clerk** for secure authentication and user management.
- **Arcjet** for security (spam, bot, and attack protection).
- **Inngest** for background workflows, event automation, and job orchestration.

---

## 🔗 Key Integrations

| Tool | Purpose | Link |
|------|----------|------|
| **Clerk** | Authentication (Sign-Up, Login, Sessions) | [Clerk Dashboard](https://go.clerk.com/jxTyzlj) |
| **Inngest** | Serverless background jobs & async workflows | [Inngest Console](https://innge.st/yt-rsc1) |
| **Arcjet** | Security (Spam, Bot, & Attack Protection) | [Arcjet Dashboard](https://launch.arcjet.com/n5oLgHV) |
| **Supabase** | PostgreSQL database hosting | [Supabase Project](https://supabase.com/dashboard/project/vsvulexlnrrtecsrlykv) |
| **Gemini** | AI intelligence & automation | — |

---

## 🏗️ Tech Stack

| Layer | Technology | Purpose |
|--------|-------------|----------|
| **Frontend** | Next.js (TypeScript) | React-based framework with routing, SSR, and SEO optimization |
| **Authentication** | Clerk | Manages user auth, sessions, and OAuth |
| **Database** | Supabase + Prisma (PostgreSQL) | Managed SQL database + ORM for schema and migrations |
| **Security** | Arcjet | Protects against spam, bots, SQL injection, and abuse |
| **Workflows** | Inngest | Handles event-driven background jobs and async tasks |
| **Language** | TypeScript | Strong typing, scalability, and maintainability |

---

## 🧩 Architecture Summary

Frontend (Next.js + Clerk)

↓

Backend API Routes (/api/)

↓

Database Layer (Prisma + Supabase)

↓

Security Layer (Arcjet Middleware)

↓

Background Tasks / Workflows (Inngest)


---

## 🔐 Authentication – Clerk

- Provides **user registration, login, and session management**.  
- Supports **OAuth** and **email/password**.  
- Integrated using `withClerkMiddleware()` and server-side validation.

## Flow: 

User → Clerk verifies → Supabase stores user data → Arcjet validates → Access granted


---

## 🗃️ Database – Supabase + Prisma

- **Supabase** = managed PostgreSQL database.  
- **Prisma** = ORM for:
  - Schema definition (`schema.prisma`)
  - Type-safe queries
  - Easy migrations  
- Allows future migration to MySQL, CockroachDB, etc. with minimal change.

---

## 🛡️ Security Layer – Arcjet

**Arcjet** provides robust application-layer protection.  

### Features:
- 🧠 **Spam Detection** – filters invalid content.  
- 🤖 **Bot Detection** – blocks automated or malicious traffic.  
- 📧 **Email Validation** – ensures valid sign-ups.  
- 🧱 **Attack Protection** – guards critical routes (`/api/login`, `/api/register`, `/api/payment`).  

### Business & SaaS Integration:
Rate limiting lets us:
- Prevent abuse by malicious users.
- Create tiered pricing models (Free → Silver → Gold → Platinum).
- Protect servers from spam transactions and AI scrapers.

---

## ⚙️ Workflow Engine – Inngest

**Inngest** handles all background jobs and event automation.

### Commands:
```bash
npx inngest-cli@latest dev
```

Used for :
  - Sending transactional emails (e.g., budget alerts, reports)
  - Automating recurring transactions
  - Generating daily and weekly balance summaries
  - Handling job retries and scheduling
  - Managing scalable asynchronous workflows

Example workflow :
  trigger: "Budget utilization exceeds 80%"
  action: "Automatically send an email alert via Inngest"

# 🧠 FinVisionAI – AI Finance Platform

overview: |
  FinVisionAI is a secure, scalable, and intelligent AI-powered financial management platform
  built with Next.js, TypeScript, Supabase, Prisma, Clerk, Arcjet, and Inngest.
  It automates workflows, strengthens app security, and streamlines finance operations — all in one system.

---

🚀 Overview:
  - Built using Next.js (TypeScript) for a high-performance, SEO-optimized frontend.
  - Supabase + Prisma serve as the database backbone with easy migrations and type safety.
  - Clerk handles user authentication and session management.
  - Arcjet strengthens security via spam, bot, and attack protection.
  - Inngest powers background job orchestration and AI-driven automation.
  - Shadcn/UI provides clean, modern UI components across the platform.

---

🔗 Key Integrations:
  - Clerk: Authentication (Sign-Up, Login, Session Handling)
  - Supabase: PostgreSQL database + Hosting
  - Prisma: ORM for schema, queries, and migrations
  - Arcjet: Security Middleware (Spam, Bot & Injection Protection)
  - Inngest: Event-driven Background Jobs & Workflows
  - Shadcn/UI: Component library for interface design
  - Gemini: Integrated AI engine for analytics and automation

---

🏗️ Tech Stack:
  Frontend: "Next.js (TypeScript) + Shadcn/UI"
  Auth: "Clerk for authentication and sessions"
  Database: "Supabase + Prisma (PostgreSQL)"
  Security: "Arcjet for anti-spam, bot protection, and request validation"
  Workflows: "Inngest for async tasks and automation"
  Language: "TypeScript"

---

🧩 Architecture Summary:
  - Frontend (Next.js + Clerk)
  - ↓
  - API Routes (/api/)
  - ↓
  - Database (Prisma + Supabase)
  - ↓
  - Security Layer (Arcjet Middleware)
  - ↓
  - Background Jobs (Inngest)

---

🔐 Authentication – Clerk:
  - Provides Sign-Up, Login, OAuth, and Email/Password authentication.
  - Integrates seamlessly using `withClerkMiddleware()` and server validation.
  - Flow:
      "User → Clerk verifies → Supabase stores user → Arcjet validates → Access granted"

---

🗃️ Database – Supabase + Prisma:
  - Supabase offers a managed PostgreSQL instance.
  - Prisma acts as an ORM for schema management and migrations.
  - Enables switching to MySQL, CockroachDB, etc., with minimal changes.
  - `schema.prisma` defines all models and relationships.

---

🛡️ Security Layer – Arcjet:
  Features:
    - Spam Detection
    - Bot & Scripted Traffic Blocking
    - Email Validation
    - Attack Protection for key routes (login, payments, register)
  Business Logic:
    - Prevents abuse and protects resources.
    - Enables rate-limiting for premium pricing tiers (Free → Silver → Gold).
    - Protects against AI scraping and SQL injection.

---

⚙️ Workflow Engine – Inngest:
  Command: "npx inngest-cli@latest dev"
  Used For:
    - Automating recurring transactions.
    - Sending reports or email alerts when budgets cross thresholds.
    - Scheduling periodic summaries (daily/weekly).
    - Handling job retries, queues, and async tasks.
  Example:
    "If budget > 80%, trigger automated email alert through Inngest."

---

🖥️ Frontend – Hero Section:
  Description: >
    The Hero section conveys FinVisionAI’s core value instantly to the visitor.
  Example: |
    “AI-Powered Financial Intelligence for Modern Businesses.”
    Analyze, automate, and scale your financial workflows securely with Supabase, Inngest, and Arcjet.
  Analogy: >
    Think of it like a **movie trailer** — short, captivating, and made to hook users instantly.

---

🧭 Landing Page Structure:
  - Hero: First impression and hook.
  - Features: Key product highlights.
  - Demo: Quick visual preview.
  - Testimonials: User feedback.
  - Pricing: Tiered subscription details.
  - Footer: Contact and quick links.

---

📊 Charts & Visualization:
  - Library: Recharts
  - Purpose: Dynamic data visualization for financial analytics.
  - Description: Enables visual reports and financial performance dashboards.

---

🧠 Demo Notes:
  - Endpoint: "http://localhost:3000/api/seed"
  - Description: Imports ~120 transactions into Supabase for the specified user_id and account_id.

---

🧰 Useful Commands:
  - Start Next.js Dev Server: "npm run dev"
  - Run Inngest Background Engine: "npx inngest-cli@latest dev"

---

⚙️ SEO Optimization (Next.js):
  - Server Components pre-render HTML for SEO.
  - Each component defines `<Metadata>` for keyword indexing.
  - Enhances load speed, crawlability, and search ranking.

---

📜 License:
  Type: "MIT License"
  Description: "This project is open-source and available under the MIT License."

---

👨‍💻 Author:
  Name: "Tanishq Thuse"
  Location: "Pune, India"
  Contact: "GitHub: tanishqthuse"

---

🌟 Acknowledgements:
  - Clerk
  - Inngest
  - Arcjet
  - Supabase
  - Shadcn/UI
  - Google Gemini

