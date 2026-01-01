<!--
Sync Impact Report:
- Version change: [CONSTITUTION_VERSION] → 1.0.0
- List of modified principles:
  - [PRINCIPLE_1_NAME] → I. Spec-Driven Development
  - [PRINCIPLE_2_NAME] → II. Simplicity
  - [PRINCIPLE_3_NAME] → III. In-Memory Storage
  - [PRINCIPLE_4_NAME] → IV. Code Quality
  - [PRINCIPLE_5_NAME] → V. Technical Stack & Standards
  - [PRINCIPLE_6_NAME] → VI. Architecture & Validation
- Added sections:
  - Constraints
  - Success Criteria
- Removed sections: None
- Templates requiring updates:
  - .specify/templates/plan-template.md (✅ updated conceptually via constitution)
  - .specify/templates/spec-template.md (✅ updated conceptually via constitution)
  - .specify/templates/tasks-template.md (✅ updated conceptually via constitution)
- Follow-up TODOs:
  - RATIFICATION_DATE set to today (2026-01-01) as this is Phase 1 adoption.
-->

# In-Memory Python Todo Console Application Constitution

## Core Principles

### I. Spec-Driven Development
Implementation MUST strictly follow the specifications defined in the `specs/` folder. No code should be written
without a corresponding specification and plan that has been reviewed.

### II. Simplicity
Focus on a clean, functional Command Line Interface (CLI) without unnecessary complexity. The first solution
to a problem MUST be the simplest one that satisfies the requirements.

### III. In-Memory Storage
For Phase 1, the application MUST NOT use external databases or files for persistence. Data MUST persist
only while the application is running.

### IV. Code Quality
Code MUST be PEP 8 compliant, modular, and easy to extend for future phases. Every function SHOULD have
docstrings explaining its purpose.

### V. Technical Stack & Standards
- Language: Python 3.13+
- Dependency Management: `uv`
- Development Framework: Spec-Kit Plus

### VI. Architecture & Validation
There MUST be a clear separation between business logic (CRUD operations) and the CLI interface.
All user inputs, especially IDs, MUST be validated to prevent application crashes.

## Constraints

- Scope: Only implement Phase 1 features (In-Memory Python App). Do NOT add Next.js or FastAPI yet.
- Environment: Must run seamlessly within a WSL/Ubuntu environment.
- Tooling: Use `uv` for all package management and running scripts.

## Success Criteria

- Application starts and displays a menu (Add, List, Complete, Delete, Exit).
- User can add a task and see it immediately in the list.
- "Complete" and "Delete" actions work correctly using Task IDs.
- Zero errors when running the final Python script.

## Governance

- The Constitution supersedes all other project practices.
- Amendments MUST be documented with a version bump and approved by the project architect.
- All code reviews MUST verify compliance with these principles.

**Version**: 1.0.0 | **Ratified**: 2026-01-01 | **Last Amended**: 2026-01-01
