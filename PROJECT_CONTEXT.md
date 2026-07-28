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

to create an intelligent shopping experience that helps users discover products through AI Skin Analysis, Virtual Try-On, and personalised product recommendations.

The primary objective is to demonstrate how AI, computer vision and generative intelligence can improve online shopping while maintaining a scalable, production-ready architecture.

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
- Deploy the application on Vercel using a production-ready workflow.

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
- Follow secure authentication and authorisation practices.

## Code Quality Rules

- Write readable and self-documenting code.
- Use TypeScript wherever possible.
- Prefer composition over duplication.
- Keep functions focused on a single responsibility.
- Test new features before marking them as complete.

---

# Project Structure

```text
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

Every AI coding assistant should read the documentation in the following order:

1. `PROJECT_CONTEXT.md`
2. `docs/01-Product-Foundation.md`
3. `docs/02-Product-Design.md`
4. `docs/03-Technical-Design.md`
5. `docs/04-Development-Roadmap.md`
6. `docs/05-AI-Development-Rules.md`
7. `docs/06-Prompting-Guide.md`
8. `docs/07-Project-Progress.md`

---

# Current Development Status

## Completed

- Project planning
- Product documentation
- Technical documentation
- Development roadmap
- AI development guidelines
- Git repository setup
- Repository documentation
- README
- PROJECT_CONTEXT
- .gitignore

## In Progress

- Next.js project initialisation
- Project setup
- Core application architecture

## Upcoming Milestones

- Authentication
- Dashboard
- AI Skin Analysis
- Virtual Try-On
- AI Recommendation Engine
- Database integration
- Testing
- Deployment
- Hackathon submission

---

# AI Assistant Workflow

Before generating or modifying code, every AI coding assistant should follow this workflow:

1. Read `PROJECT_CONTEXT.md`.
2. Review the relevant documentation inside the `/docs` directory.
3. Understand the current development status.
4. Follow the AI Development Guidelines.
5. Implement only the requested feature.
6. Keep the implementation modular and maintainable.
7. Update documentation whenever architecture or functionality changes.
8. Update `docs/07-Project-Progress.md` after completing significant work.

The objective is to keep every AI coding session consistent, maintainable and aligned with the project's vision, architecture and long-term goals.

---

# Definition of Success

MirrorCommerce AI is considered successful when:

- The application is fully functional and production-ready.
- AI Skin Analysis is successfully integrated.
- Virtual Try-On works correctly using Perfect Corp. APIs.
- OpenAI provides accurate and useful product recommendations.
- The application is deployed successfully on Vercel.
- The documentation remains synchronised with the implementation.
- Every AI coding assistant can understand the project by reading this document and the documentation in `/docs`.
