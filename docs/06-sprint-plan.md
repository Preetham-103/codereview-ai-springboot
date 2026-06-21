# Sprint Plan

# CodeReview AI for Spring Boot Projects

---

# Sprint 1 — Backend Skeleton

## Goal

Set up the Spring Boot project and implement review project management APIs.

## Stories

* US-1.1 Create review project
* US-1.2 List all review projects
* US-1.3 Get project details

## Deliverables

* Spring Boot app initialized
* MongoDB connected
* Project model created
* Create/list/get project APIs working
* Global exception handling added

---

# Sprint 2 — Upload & Extraction

## Goal

Allow a user to upload a Spring Boot ZIP and extract it.

## Stories

* US-2.1 Upload Spring Boot ZIP
* US-2.2 Validate uploaded ZIP
* US-2.3 Extract ZIP contents
* US-2.4 Scan extracted project files

## Deliverables

* upload endpoint
* ZIP validation
* extraction service
* file indexing

---

# Sprint 3 — Parsing & Metadata Extraction

## Goal

Parse Java metadata and classify files.

## Stories

* US-3.1 Parse Java file metadata
* US-3.2 Detect annotations and layer type
* US-3.3 Save parsed file metadata

## Deliverables

* metadata extraction
* layer detection
* metadata persistence

---

# Sprint 4 — Rule Engine MVP

## Goal

Implement the first rule engine checks.

## Stories

* US-4.1 Run rule engine for uploaded project
* US-4.2 Detect field injection
* US-4.3 Detect controller to repository direct access
* US-4.4 Detect missing `@Valid`
* US-4.5 Detect missing global exception handler
* US-4.6 Detect long service methods

## Deliverables

* rule interface
* rule engine flow
* issue generation and storage

---

# Sprint 5 — Review Reporting APIs

## Goal

Return review results and summary APIs.

## Stories

* US-5.1 Save review issues
* US-5.2 Get review results by project
* US-5.3 Get project review summary

## Deliverables

* issue retrieval API
* project review summary API

---

# Sprint 6 — AI Explanation Layer

## Goal

Generate AI explanations for rule violations.

## Stories

* US-6.1 Generate AI explanation for issue
* US-6.2 Generate fix suggestion
* US-6.3 Save AI explanation result

## Deliverables

* AI prompt flow
* issue explanation API
* AI explanation persistence
