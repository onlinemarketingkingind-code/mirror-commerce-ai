# MirrorCommerce AI
## AI Development Rules
Version: 1.0

---

# Purpose

This document defines the engineering standards, coding principles, architecture rules, and development workflow for MirrorCommerce AI.

Every AI coding assistant (Lovable, Codex, Cursor, Claude, Gemini, ChatGPT, etc.) must follow these rules before generating or modifying any code.

These rules override assumptions and default behaviors whenever possible.

---

# Project Vision

MirrorCommerce AI is an AI-powered shopping concierge that combines:

- Perfect Corp. YouCam APIs
- OpenAI
- Next.js
- Supabase

to deliver intelligent shopping experiences through:

- AI Skin Analysis
- Virtual Try-On
- Personalized Recommendations
- User Dashboard
- Analysis History

Every implementation decision should support this vision.

---

# Development Principles

The project must prioritize:

- Clean Architecture
- Scalability
- Maintainability
- Performance
- Security
- Reusable Components
- Accessibility
- Production Readiness

Never generate prototype-quality code unless explicitly requested.

---

# Technology Stack

Frontend

- Next.js 15
- React 19
- TypeScript
- Tailwind CSS
- shadcn/ui
- Framer Motion

Backend

- Next.js API Routes
- Server Actions

Database

- Supabase PostgreSQL

Authentication

- Supabase Auth

Storage

- Supabase Storage

Deployment

- Vercel

AI

- OpenAI API
- Perfect Corp. YouCam APIs

Do not replace any technology without approval.

---

# Coding Standards

Always use:

TypeScript

Never use plain JavaScript.

Always

- Strict typing
- Functional components
- Async/Await
- Modular architecture
- Reusable code

Avoid

- Any
- Duplicate logic
- Large monolithic components
- Hardcoded values

---

# Component Rules

Every component must have one responsibility.

Good Example

Button

UploadCard

SkinScoreCard

RecommendationCard

HistoryTable

Avoid

DashboardComponentThatDoesEverything

Components should remain reusable.

---

# Folder Rules

Follow this structure.

app/

components/

lib/

hooks/

services/

types/

public/

styles/

docs/

Do not create random folders.

---

# UI Guidelines

Design should be:

Clean

Minimal

Modern SaaS

Responsive

Professional

Use:

- Tailwind CSS
- shadcn/ui

Avoid unnecessary animations.

Only use Framer Motion where it improves user experience.

---

# Responsive Design

Support:

Desktop

Tablet

Mobile

Every page should work properly on all screen sizes.

---

# API Rules

Never call external APIs directly from the client.

Always

Client

↓

API Route

↓

External API

↓

Return Response

API keys must never be exposed.

---

# Security Rules

Never expose:

OpenAI API Key

YouCam Secret

Supabase Service Key

Always use environment variables.

Validate every request.

Sanitize all user input.

Use secure authentication.

---

# Database Rules

Use Supabase.

Never duplicate user data.

Prefer relational design.

Store complex API responses as JSONB.

Use UUID primary keys.

Use timestamps on every table.

---

# Image Handling

Before sending to YouCam:

Validate image

Check file size

Compress if necessary

Reject unsupported formats

Never store unnecessary user images permanently.

---

# Error Handling

Every API call must handle:

Loading

Success

Failure

Timeout

Retry

Display friendly error messages.

Never expose technical stack traces to users.

---

# Logging

Use structured logging.

Log:

API failures

Authentication errors

Unexpected exceptions

Do not log:

Passwords

Secrets

Tokens

Personal information

---

# Performance

Optimize:

Images

API calls

Rendering

Lazy loading

Caching

Avoid unnecessary re-renders.

---

# Accessibility

Support:

Keyboard navigation

Proper labels

ARIA attributes

Color contrast

Screen readers

Accessibility is required.

---

# Documentation

Every major module should include:

Purpose

Inputs

Outputs

Dependencies

Complex logic should be documented.

Avoid unnecessary comments.

Write self-explanatory code.

---

# Git Workflow

Small commits.

Meaningful commit messages.

Examples

feat(authentication): add Supabase login

fix(upload): resolve image validation issue

refactor(api): improve recommendation endpoint

Avoid:

update

changes

fix bug

---

# Testing

Before completing any feature verify:

No TypeScript errors

No console errors

Responsive

Accessible

API working

Error handling working

---

# AI Behavior Rules

Never delete existing functionality unless instructed.

Never rename files unnecessarily.

Never reorganize folders without approval.

Never introduce breaking changes.

Always preserve backward compatibility.

Always explain architectural decisions.

When uncertain:

Ask instead of assuming.

---

# Code Quality Checklist

Before considering any task complete:

- Builds successfully
- TypeScript passes
- No lint errors
- Responsive
- Accessible
- Reusable components
- Secure
- Environment variables used
- API errors handled
- Loading states implemented
- Empty states implemented
- Documentation updated

---

# Definition of Done

A feature is complete only when:

✓ Code compiles

✓ UI matches requirements

✓ API works

✓ Database updated

✓ Error handling exists

✓ Responsive

✓ Accessible

✓ Clean code

✓ Production ready

---

# Future AI Instructions

Every AI assistant working on MirrorCommerce AI must:

Read:

1. Product Foundation

2. Product Design

3. Technical Design

4. Development Plan

5. AI Development Rules

before writing or modifying code.

Never skip this step.

---

End of Document
Version 1.0

