# Project Context

**Project Name:** MirrorCommerce AI

**Tagline:** Your Personal AI Shopping Concierge

---

## Purpose

This document serves as the primary context for developers and AI coding assistants working on MirrorCommerce AI.

Before implementing any feature, read this document along with the documentation in the `/docs` directory to understand the project's goals, architecture, development standards, and current progress.

This file is the single source of truth for project context.

---

# Project Overview

MirrorCommerce AI is an AI-powered shopping assistant built for the **Perfect Corp. YouCam AI Hackathon**.

The platform combines:

- Perfect Corp. YouCam APIs
- OpenAI
- Supabase
- Next.js
- React
- TypeScript

to create an intelligent shopping experience that helps users discover products through AI Skin Analysis, Virtual Try-On, and personalized recommendations.

The primary objective is to demonstrate how AI, computer vision, and generative intelligence can improve online shopping while maintaining a scalable, production-ready architecture.

---

# Project Goals

## Business Goals

- Build an AI-powered shopping experience using Perfect Corp. YouCam APIs and OpenAI.
- Deliver a polished, production-ready application for the Perfect Corp. YouCam AI Hackathon.
- Demonstrate a scalable architecture suitable for future commercial development.

## Technical Goals

- Build a modern full-stack application using Next.js 15 and React 19.
- Implement secure authentication and data storage with Supabase.
- Integrate Perfect Corp. YouCam APIs for AI Skin Analysis and Virtual Try-On.
- Use OpenAI to generate intelligent product recommendations.
- Deploy the application on Vercel with a production-ready workflow.

## User Goals

- Help users discover products that match their needs.
- Simplify the online shopping experience using AI.
- Deliver fast, intuitive and personalised recommendations.

---

# AI Development Guidelines

Every AI coding assistant (Lovable, Codex, Claude Code, Cursor, ChatGPT, Gemini, etc.) must follow these rules when working on this project.

## General Rules

- Read this document before generating or modifying code.
- Review the relevant documentation inside the `/docs` directory.
- Never change the project architecture without updating the documentation.
- Follow the project's coding standards and naming conventions.
- Keep the codebase clean, modular and maintainable.
- Avoid unnecessary dependencies.
- Prefer reusable components over duplicated code.

## Documentation Rules

- Update documentation whenever a major architectural or functional change is made.
- Keep the documentation consistent with the implementation.
- Archive obsolete documentation instead of deleting it.

## Security Rules

- Never hardcode API keys or secrets.
- Use environment variables for all sensitive configuration.
- Validate all user input.
- Follow secure authentication and authorization practices.

## Code Quality Rules

- Write readable and self-documenting code.
- Use TypeScript wherever possible.
- Prefer composition over duplication.
- Keep functions focused on a single responsibility.
- Test new features before marking them as complete.

  ---

# Project Structure

```
mirror-commerce-ai/
│
├── README.md
├── PROJECT_CONTEXT.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── .gitignore
│
├── docs/
│   ├── README.md
│   ├── CHANGELOG.md
│   ├── assets/
│   ├── archive/
│   ├── 01-Product-Foundation.md
│   ├── 02-Product-Design.md
│   ├── 03-Technical-Design.md
│   ├── 04-Development-Roadmap.md
│   ├── 05-AI-Development-Rules.md
│   ├── 06-Prompting-Guide.md
│   └── 07-Project-Progress.md
│
├── app/
├── components/
├── lib/
├── public/
├── styles/
└── supabase/
```

## Documentation Reading Order

AI coding assistants should read the documentation in the following order:

1. PROJECT_CONTEXT.md
2. docs/01-Product-Foundation.md
3. docs/02-Product-Design.md
4. docs/03-Technical-Design.md
5. docs/04-Development-Roadmap.md
6. docs/05-AI-Development-Rules.md
7. docs/06-Prompting-Guide.md
8. docs/07-Project-Progress.md
