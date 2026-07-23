# MirrorCommerce AI
# AI Prompting Guide
Version: 1.0

---

# Purpose

This guide provides standardized prompts for AI coding assistants working on MirrorCommerce AI.

The goal is to ensure every AI (Lovable, Codex, Claude Code, Cursor, Gemini, ChatGPT, etc.) follows the same project requirements, architecture, coding standards, and development workflow.

Never begin development without first referencing the PRD and AI Development Rules.

---

# Project Documents

Every AI session must load these documents first.

1. Product Foundation
2. Product Design
3. Technical Design
4. Development Plan
5. AI Development Rules

These documents are the single source of truth.

---

# Standard Context Prompt

Use this at the beginning of every new AI coding session.

---

You are the lead software engineer for MirrorCommerce AI.

MirrorCommerce AI is an AI-powered shopping concierge built for the Perfect Corp. YouCam AI Hackathon.

Before writing code, review the following project documentation:

- Product Foundation
- Product Design
- Technical Design
- Development Plan
- AI Development Rules

Your responsibilities:

- Follow the project architecture exactly.
- Follow the folder structure exactly.
- Use TypeScript.
- Use Next.js 15.
- Use React 19.
- Use Tailwind CSS.
- Use shadcn/ui.
- Use Supabase.
- Use OpenAI.
- Use Perfect Corp. YouCam APIs.

Do not invent additional features.

Do not remove existing functionality.

Do not change the architecture without explanation.

Produce production-quality code.

Always explain major implementation decisions.

---

# Prompt Template: Build New Feature

Build the following feature for MirrorCommerce AI.

Feature:

[Describe Feature]

Requirements:

- Follow the PRD.
- Follow AI Development Rules.
- Reuse existing components.
- Maintain responsive design.
- Handle loading, success and error states.
- Use TypeScript.
- Write clean and modular code.

Before implementation:

Explain your approach.

After implementation:

Summarize what was created.

---

# Prompt Template: Build New Page

Create the following page.

Page Name:

[Page Name]

Requirements:

- Follow Product Design document.
- Follow Technical Design.
- Match project design system.
- Responsive layout.
- Accessibility support.
- Reusable components.
- Proper routing.
- Loading state.
- Error state.

Do not create placeholder architecture that conflicts with the PRD.

---

# Prompt Template: API Integration

Integrate the following API.

API:

[API Name]

Requirements:

- Use Next.js API Routes.
- Never expose secrets.
- Use environment variables.
- Validate requests.
- Handle failures gracefully.
- Return consistent responses.
- Log unexpected errors.
- Use TypeScript interfaces.

Explain:

- Request flow
- Response flow
- Error handling

---

# Prompt Template: UI Improvements

Improve the user interface.

Goals:

- Modern SaaS appearance.
- Better usability.
- Better spacing.
- Better typography.
- Better responsiveness.

Do not redesign the application.

Improve existing design only.

---

# Prompt Template: Bug Fix

Fix the following issue.

Issue:

[Description]

Requirements:

- Identify root cause.
- Explain the issue.
- Implement the smallest safe fix.
- Do not introduce breaking changes.
- Preserve current functionality.
- Update related code if necessary.

Summarize:

- Cause
- Solution
- Files changed

---

# Prompt Template: Refactoring

Refactor the following module.

Goals:

- Improve readability.
- Improve maintainability.
- Reduce duplication.
- Preserve existing behavior.
- Follow AI Development Rules.

Do not rewrite unrelated code.

---

# Prompt Template: Performance Optimization

Optimize the following feature.

Focus on:

- Rendering
- API Calls
- Images
- Lazy Loading
- Bundle Size
- Caching

Measure expected improvements.

---

# Prompt Template: Database Changes

Update the database.

Requirements:

- Maintain relationships.
- Avoid redundant data.
- Use UUID keys.
- Include timestamps.
- Preserve backward compatibility.

Provide:

- Updated schema
- Migration steps
- Impact analysis

---

# Prompt Template: Code Review

Review the current implementation.

Evaluate:

- Architecture
- Performance
- Security
- Accessibility
- Maintainability
- TypeScript quality
- React best practices

Return:

Strengths

Weaknesses

Recommendations

Priority improvements

---

# Prompt Template: Documentation

Document the following module.

Include:

Purpose

Inputs

Outputs

Dependencies

Example usage

Avoid unnecessary explanations.

---

# Prompt Template: Production Readiness Review

Review the project before deployment.

Verify:

- No TypeScript errors
- No lint errors
- Responsive design
- Accessibility
- Security
- API handling
- Environment variables
- Error handling
- Loading states
- Empty states
- Build success

Return a deployment checklist.

---

# Prompt Template: Release Preparation

Prepare the project for release.

Tasks:

- Review documentation.
- Review dependencies.
- Review environment variables.
- Review security.
- Review performance.
- Generate release notes.
- Suggest version number.

---

# AI Collaboration Rules

If another AI previously worked on the project:

Review existing code first.

Avoid duplicate implementations.

Preserve architecture consistency.

Explain any significant changes.

Never overwrite working code without justification.

---

# Session Checklist

At the beginning of every session:

✓ Read project documentation

✓ Understand current objective

✓ Identify affected modules

✓ Explain implementation plan

At the end of every session:

✓ Summarize work completed

✓ List modified files

✓ List remaining tasks

✓ Identify risks or blockers

---

# Prompting Best Practices

Always provide:

- Clear objective
- Scope
- Constraints
- Expected output
- Acceptance criteria

Avoid vague requests such as:

"Improve the app."

Instead use:

"Improve the dashboard layout by enhancing spacing, responsiveness, and accessibility while preserving the existing design system."

---

# Definition of Success

A successful AI session should:

- Produce production-quality code.
- Respect the PRD.
- Follow AI Development Rules.
- Require minimal manual corrections.
- Move the project closer to completion.

---

End of Document

Version 1.0

