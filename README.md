# PulseDesk

> A multi-tenant SaaS Help Desk platform built for the Forge2 AI Engineering Hackathon using Hermes (Product Owner) and OpenClaw (Software Engineer).

---

## Overview

PulseDesk is a hosted customer support platform that enables multiple organizations (tenants) to manage customer support tickets securely and independently.

The application demonstrates an AI-native software engineering workflow where Hermes plans and manages the project while OpenClaw implements features through iterative sprints.

---

## Features

### MUST Features

- Multi-tenancy (organization-based data isolation)
- Laravel Sanctum Authentication
- Role-based access control
  - Admin
  - Agent
  - Customer
- Ticket Management
  - Create
  - Update
  - Assign
  - Resolve
  - Close
- Ticket Conversations
  - Public Replies
  - Internal Notes
- Search & Filtering
- REST API
- React Frontend
- Seeded Demo Data

### SHOULD Features

- SLA Policies
- Assignment Queues
- Activity Logs
- Dashboard Metrics
- Notifications

### STRETCH Features

- Customer Portal
- CSAT Ratings
- Ticket Merge
- Bulk Actions
- CSV Export

---

# Technology Stack

## Backend

- Laravel
- PHP
- Sanctum Authentication
- MySQL

## Frontend

- React
- Vite
- Axios

## AI Agents

- Hermes Agent
- OpenClaw

## AI Model Provider

- EastRouter
- Model: GLM-5.1

---

# Architecture

```
React Frontend
        │
        ▼
Laravel REST API
        │
        ▼
Authentication (Sanctum)
        │
        ▼
Business Logic
        │
        ▼
MySQL Database
```

Every tenant's data is isolated using the `organization_id` field.

---

# Project Structure

```
app/
database/
routes/
resources/
tests/

sprints/
    sprint-00.md
    sprint-01.md
    sprint-02.md

evidence/
    screenshots/
    slack/
    prs/
    ci/

.github/
```

---

# AI Engineering Workflow

## Hermes

Responsibilities

- Sprint Planning
- Product Backlog
- Issue Creation
- Task Assignment
- Acceptance Criteria

## OpenClaw

Responsibilities

- Feature Implementation
- Code Generation
- Testing
- Pull Requests
- Progress Updates

## Human

Responsibilities

- Review
- Approval
- Merge
- Final Validation

---

# Sprint Workflow

```
Hermes
      │
      ▼
Sprint Planning
      │
      ▼
Issue Assignment
      │
      ▼
OpenClaw Implementation
      │
      ▼
Pull Request
      │
      ▼
CI Validation
      │
      ▼
Human Review
      │
      ▼
Merge
```

---

# Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/PulseDesk.git
```

Install dependencies

```bash
composer install
npm install
```

Copy environment

```bash
cp .env.example .env
```

Generate application key

```bash
php artisan key:generate
```

Run migrations

```bash
php artisan migrate --seed
```

Run backend

```bash
php artisan serve
```

Run frontend

```bash
npm run dev
```

---

# Demo Accounts

## Admin

```
admin@pulsedesk.test
password
```

## Agent

```
agent1@pulsedesk.test
password
```

## Customer

```
customer1@pulsedesk.test
password
```

---

# Security

- Organization-based data isolation
- Role-based authorization
- Laravel Sanctum authentication
- Environment variables for secrets
- No API keys committed to the repository

---

# Testing

Run backend tests

```bash
php artisan test
```

Run frontend

```bash
npm run test
```

---

# Hackathon Deliverables

- Multi-tenant SaaS Application
- REST API
- React Frontend
- Sprint Documentation
- GitHub Pull Requests
- CI/CD Pipeline
- AI Agent Collaboration
- Human Review Process

---

# Team Workflow

Hermes served as the Product Owner, responsible for planning, backlog management, sprint creation, and issue assignment.

OpenClaw acted as the Software Engineer, implementing features, generating code, preparing pull requests, and reporting progress.

The human developer reviewed all changes, approved pull requests, validated functionality, and managed the final integration.

---

# License

MIT License

---

Built for the **Forge2 AI Engineering Hackathon** using **Hermes**, **OpenClaw**, **EastRouter**, **Laravel**, and **React**.
