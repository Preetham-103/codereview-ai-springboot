# Product Requirements Document (PRD)

# CodeReview AI for Spring Boot Projects

---

# 1. Product Overview

CodeReview AI is a developer tool that reviews **Java Spring Boot projects** and produces code-quality and architecture feedback.

It allows a developer to upload a Spring Boot codebase, extract structural metadata, run rule-based checks, and receive issue-level review findings. In later phases, it will also use AI to explain issues and suggest improvements.

---

# 2. Problem Statement

Spring Boot developers, especially students and freshers, often do not know whether:

* their controllers are too heavy
* validation is missing
* repository access is placed incorrectly
* exception handling is weak
* service methods are too large
* package/layer organization is inconsistent

Manual review requires time and experienced reviewers. This product aims to automate first-level review of Spring Boot projects.

---

# 3. Target User

## Primary User

A Java/Spring Boot developer who wants to upload a project and receive review feedback before:

* presenting it in interviews
* putting it on GitHub
* improving its code quality
* learning better backend practices

---

# 4. Product Goals

## Primary Goals

1. Accept Spring Boot project input
2. Parse project structure and Java metadata
3. Detect rule-based code-quality issues
4. Store review findings with severity and suggestions
5. Provide review reports via API
6. Add AI-generated issue explanations in later phases

---

# 5. Non-Goals for MVP

The MVP will **not** include:

* full SonarQube-level static analysis
* IDE plugin support
* support for multiple languages
* automatic code fixes committed back to repo
* GitHub PR bot integration
* enterprise team collaboration features

---

# 6. MVP Scope

The MVP must support:

* creating a review project
* uploading a Spring Boot ZIP
* extracting files
* scanning `.java` and key config files
* identifying Spring components
* running 8–10 rule-based checks
* storing issues in MongoDB
* returning review report APIs

---

# 7. Core Modules

## Module 1 — Project Management

Handles project creation, retrieval, and project status.

## Module 2 — Upload & Extraction

Handles ZIP upload, validation, extraction, and file indexing.

## Module 3 — Parsing & Metadata Extraction

Parses Java files, annotations, and project layer information.

## Module 4 — Rule Engine

Runs review rules and generates issues.

## Module 5 — Review Reporting

Returns project review results and summaries.

## Module 6 — AI Explanation Layer

Generates AI explanations and fix suggestions for issues.

## Module 7 — Health Score & Insights

Creates project-level quality scores and summaries.

---

# 8. Success Criteria for MVP

The MVP is successful if:

1. A user can create a review project
2. A Spring Boot ZIP can be uploaded and extracted
3. The system can detect controllers/services/repositories/DTOs/entities
4. The rule engine can produce issues for at least 8 meaningful checks
5. Issues can be retrieved through review APIs

---

# 9. Initial Rule Set

The first version of the rule engine will support:

1. Field injection used
2. Controller directly accesses repository
3. Missing `@Valid`
4. Missing global exception handler
5. Controller contains too much logic
6. Long service methods
7. Hardcoded strings
8. Layer/package mismatch

---

# 10. Development Phases

## Phase 0 — Planning & Documentation

Define scope, docs, backlog, repo, and project board.

## Phase 1 — Backend Skeleton

Set up Spring Boot project, MongoDB, project APIs, and common exception handling.

## Phase 2 — Upload & Extraction

Implement ZIP upload, validation, extraction, and file indexing.

## Phase 3 — Parsing & Metadata Extraction

Read Java metadata and classify project layers.

## Phase 4 — Rule Engine MVP

Implement the initial rule set and issue generation.

## Phase 5 — Review Reporting APIs

Provide issue listing and summary APIs.

## Phase 6 — AI Explanation Layer

Generate AI explanations and fix suggestions for issues.

## Phase 7 — Dashboard / Advanced Features

Add UI, health score, and advanced product features.
