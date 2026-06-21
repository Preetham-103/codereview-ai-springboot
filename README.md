# CodeReview AI for Spring Boot Projects

## Overview

CodeReview AI is a backend-focused developer tool that reviews **Java Spring Boot projects** and provides structured feedback on code quality, architecture, and best-practice violations.

The platform allows a developer to upload a Spring Boot project, parse its codebase, run rule-based checks, and generate review findings such as:

* field injection usage
* missing request validation
* repository access from controllers
* long service methods
* missing global exception handling
* package/layer mismatches

In later phases, the platform will also use AI to explain issues, suggest fixes, and provide project-level quality summaries.

---

## Problem Statement

Spring Boot developers, especially students and early-career backend engineers, often build projects without knowing:

* whether their layering is clean
* whether Spring Boot best practices are followed
* whether validation and exception handling are implemented correctly
* whether controllers and services are well-structured
* whether maintainability issues exist before deployment or interviews

Manual review takes time and usually requires an experienced reviewer.

**CodeReview AI** aims to automate this process for Spring Boot projects by combining:

1. project parsing
2. rule-based analysis
3. AI-assisted explanations

---

## Core Goals

* Accept a Spring Boot project ZIP as input
* Parse Java classes and Spring annotations
* Detect backend code quality issues
* Generate review findings with severity and suggestions
* Provide a project-level review summary
* Add AI-generated explanations and fix recommendations

---

## MVP Scope

The first version of the project will support:

* creating a review project
* uploading a Spring Boot ZIP
* extracting and scanning project files
* detecting controllers, services, repositories, DTOs, and entities
* running 8–10 rule-based review checks
* storing issues and exposing them via APIs

---

## Planned Rule Checks (Initial)

* Field injection used instead of constructor injection
* Controller directly accessing repository
* Missing `@Valid` on request DTOs
* Missing global exception handling
* Controller containing too much business logic
* Long service methods
* Hardcoded strings in service/controller logic
* Package/layer mismatch

---

## Tech Stack

### Backend

* Java
* Spring Boot
* Spring Web
* Spring Data MongoDB
* Lombok
* Maven

### Database

* MongoDB

### Future AI Layer

* LLM integration for issue explanations and fix suggestions

---

## Project Structure

```text
codereview-ai-springboot/
├── README.md
├── docs/
│   ├── 01-prd.md
│   ├── 02-user-stories.md
│   ├── 03-architecture.md
│   ├── 04-db-schema.md
│   ├── 05-api-spec.md
│   ├── 06-sprint-plan.md
│   ├── 07-rule-catalog.md
│   └── 08-ai-prompts.md
└── backend/
```

---

## Current Development Phases

1. Planning & Documentation
2. Backend Skeleton
3. Upload & Extraction
4. Parsing & Metadata Extraction
5. Rule Engine MVP
6. Review Reporting APIs
7. AI Explanation Layer
8. Dashboard / Advanced Features

---

## Status

Project planning and backlog setup in progress.
