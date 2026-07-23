# MirrorCommerce AI

> **Technical Design**  
> **Version:** 1.0  
> **Status:** Planning Complete  
> **Last Updated:** July 2026

---

# Product Requirements Document (PRD)

## Part 3 – Technical Design

This document defines the technical architecture, system modules, database design, API structure, security model, and project folder organization for MirrorCommerce AI.

---

# Table of Contents

1. Technology Stack
2. System Architecture
3. System Modules
4. Database Schema
5. API Architecture
6. Security
7. Project Folder Structure

---

# 1. Technology Stack

The application is built using a modern full-stack architecture designed for scalability, maintainability, and rapid development.

## Frontend

| Technology | Purpose |
|------------|---------|
| Next.js 15 | React Framework |
| React 19 | User Interface |
| TypeScript | Type Safety |
| Tailwind CSS | Styling |
| shadcn/ui | UI Components |
| Framer Motion | Animations |

---

## Backend

| Technology | Purpose |
|------------|---------|
| Next.js API Routes | Backend APIs |
| Server Actions | Server-side Operations |
| Node.js | Runtime Environment |

---

## Database

| Technology | Purpose |
|------------|---------|
| Supabase PostgreSQL | Primary Database |

---

## Authentication

| Technology | Purpose |
|------------|---------|
| Supabase Auth | User Authentication |

---

## Storage

| Technology | Purpose |
|------------|---------|
| Supabase Storage | Image & File Storage |

---

## AI Services

| Technology | Purpose |
|------------|---------|
| OpenAI GPT API | AI Recommendations |
| Perfect Corp. YouCam APIs | Skin Analysis & Virtual Try-On |

---

## Deployment

| Technology | Purpose |
|------------|---------|
| Vercel | Hosting & Deployment |

---

# 2. System Architecture

## High-Level Architecture

```text
                    User
                     │
                     ▼
            Next.js Frontend
                     │
     ┌───────────────┼───────────────┐
     ▼               ▼               ▼
Supabase Auth   Next.js API    Supabase Database
                     │
     ┌───────────────┼───────────────┐
     ▼                               ▼
YouCam APIs                    OpenAI API
     │                               │
     └───────────────┬───────────────┘
                     ▼
        AI Recommendation Engine
                     │
                     ▼
              Dashboard Interface
```

---

## Request Flow

```text
User

↓

Next.js Frontend

↓

API Route

↓

AI Services (YouCam / OpenAI)

↓

Supabase Database

↓

Dashboard Response
```

---

# 3. System Modules

The application is divided into independent modules, each responsible for a specific area of functionality.

---

## Authentication Module

### Responsibilities

- User Registration
- User Login
- Session Management
- User Profile Management

---

## Image Processing Module

### Responsibilities

- Upload Images
- Validate Image Format
- Compress Images
- Send Images to YouCam APIs

---

## Skin Analysis Module

### Responsibilities

- Face Detection
- Skin Analysis
- Skin Metrics
- Skin Score Calculation

---

## AI Recommendation Module

### Responsibilities

- Receive Skin Analysis
- Generate AI Explanations
- Recommend Products
- Explain Recommendations

---

## Virtual Try-On Module

### Responsibilities

- Load Product Catalog
- Send Images to YouCam
- Generate Virtual Preview
- Compare Multiple Products

---

## History Module

### Responsibilities

- Save Analyses
- Save Recommendations
- Retrieve Previous Sessions

---

# 4. Database Schema

The application uses **Supabase PostgreSQL** with relational tables and JSONB for flexible AI response storage.

---

## users

| Field | Type |
|--------|------|
| id | UUID |
| name | Text |
| email | Text |
| avatar | Text |
| created_at | Timestamp |

---

## analyses

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| image_url | Text |
| skin_score | Integer |
| analysis_json | JSONB |
| created_at | Timestamp |

---

## recommendations

| Field | Type |
|--------|------|
| id | UUID |
| analysis_id | UUID |
| ai_response | Text |
| confidence_score | Integer |
| created_at | Timestamp |

---

## virtual_tryons

| Field | Type |
|--------|------|
| id | UUID |
| analysis_id | UUID |
| product_name | Text |
| preview_image | Text |
| created_at | Timestamp |

---

## products

| Field | Type |
|--------|------|
| id | UUID |
| brand | Text |
| category | Text |
| product_name | Text |
| image | Text |
| metadata | JSONB |

---

## user_preferences

| Field | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| skin_type | Text |
| preferred_brand | Text |
| budget | Integer |

---

# 5. API Architecture

## External APIs

### 1. YouCam Skin Analysis API

**Purpose**

Analyze uploaded selfies to generate skin insights.

**Request**

- Image
- User ID

**Response**

- Skin Score
- Skin Type
- Skin Metrics
- Confidence Score

---

### 2. YouCam Virtual Try-On API

**Purpose**

Generate AI-powered virtual product previews.

**Request**

- User Image
- Selected Product

**Response**

- Preview Image
- Rendering Metadata

---

### 3. OpenAI API

**Purpose**

Generate personalized product recommendations.

**Input**

- Skin Analysis
- User Preferences
- Product Database

**Output**

- AI Recommendation
- Product Explanation
- Care Tips

---

## Internal API Routes

| Route | Purpose |
|---------|----------|
| `/api/auth` | Authentication |
| `/api/upload` | Image Upload |
| `/api/analyze` | Skin Analysis |
| `/api/recommend` | AI Recommendations |
| `/api/tryon` | Virtual Try-On |
| `/api/history` | Analysis History |
| `/api/profile` | User Profile |

---

# 6. Security

Security is built into every layer of the application.

---

## Authentication Security

- Supabase Authentication
- JWT Sessions
- Secure Cookies

---

## API Security

- Environment Variables
- Server-side API Calls
- Rate Limiting
- Input Validation

---

## File Upload Security

- Image Type Validation
- File Size Limits
- Secure Storage
- Malware Protection *(Future Enhancement)*

---

## Data Privacy

- User data encrypted
- HTTPS only
- Secure API communication
- No permanent storage of biometric data
- Users can permanently delete their analysis history

---

# 7. Project Folder Structure

```text
mirrorcommerce-ai/
│
├── app/
│   ├── (auth)/
│   ├── dashboard/
│   ├── analysis/
│   ├── try-on/
│   ├── history/
│   ├── profile/
│   └── api/
│
├── components/
│   ├── layout/
│   ├── dashboard/
│   ├── upload/
│   ├── analysis/
│   ├── recommendations/
│   ├── tryon/
│   ├── ui/
│   └── shared/
│
├── lib/
│   ├── openai/
│   ├── youcam/
│   ├── supabase/
│   ├── auth/
│   └── utils/
│
├── hooks/
├── services/
├── types/
├── public/
├── styles/
├── docs/
│
└── README.md
```

---

# Technical Design Principles

MirrorCommerce AI is designed around the following engineering principles:

- **Modular Architecture** – Independent and reusable modules.
- **API-First Design** – Backend services exposed through structured APIs.
- **Scalable Infrastructure** – Built for future feature expansion.
- **Security by Default** – Authentication, validation, and encryption at every layer.
- **AI-Centric Workflow** – YouCam and OpenAI integrations drive the user experience.
- **Maintainability** – Clean folder structure and strongly typed codebase.

---

# Success Criteria

The Technical Design phase will be considered complete when:

- Technology stack is finalized.
- System architecture is documented.
- Core modules are defined.
- Database schema is approved.
- API structure is documented.
- Security requirements are established.
- Folder structure is standardized.

---

# Related Documentation

Continue reading the remaining project documentation in the following order:

1. **04-Development-Roadmap.md**
2. **05-AI-Development-Rules.md**
3. **06-Prompting-Guide.md**
4. **07-Project-Progress.md**

---

**End of Document**

**MirrorCommerce AI – Technical Design**  
**Version 1.0**

