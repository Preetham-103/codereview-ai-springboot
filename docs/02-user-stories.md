# User Stories

# CodeReview AI for Spring Boot Projects

---

# EPIC E1 — Review Project Management

## US-1.1 Create review project

**As a developer**, I want to create a review project so that I can analyze a Spring Boot codebase.

### Acceptance Criteria

* user can create a project with a name
* project receives a unique ID
* project status is initialized

---

## US-1.2 List all review projects

**As a developer**, I want to view all review projects so that I can continue my previous reviews.

### Acceptance Criteria

* API returns all projects
* each project includes name, status, and timestamps

---

## US-1.3 Get project details

**As a developer**, I want to view a project’s details and current review status.

### Acceptance Criteria

* fetch project by ID
* show metadata and current status

---

# EPIC E2 — Upload & Extraction

## US-2.1 Upload Spring Boot ZIP

**As a developer**, I want to upload a Spring Boot ZIP so that the system can analyze it.

### Acceptance Criteria

* ZIP upload endpoint accepts `.zip`
* upload is linked to project ID
* upload status is saved

---

## US-2.2 Validate uploaded ZIP

**As the system**, I want to validate ZIP type and structure before extraction.

### Acceptance Criteria

* reject invalid file types
* reject empty ZIP uploads
* return meaningful validation error

---

## US-2.3 Extract ZIP contents

**As the system**, I want to extract ZIP contents so that project files can be scanned.

### Acceptance Criteria

* ZIP is extracted safely
* extracted files are indexed
* extraction status is updated

---

## US-2.4 Scan extracted project files

**As the system**, I want to scan extracted files and identify relevant project files.

### Acceptance Criteria

* `.java`, `pom.xml`, `application.properties`, and `application.yml` can be identified
* extracted file paths are stored

---

# EPIC E3 — Parsing & Metadata Extraction

## US-3.1 Parse Java file metadata

**As the system**, I want to extract metadata from Java files so that rules can run on structured information.

### Acceptance Criteria

* detect class name
* detect package name
* detect imports
* detect method names

---

## US-3.2 Detect annotations and layer type

**As the system**, I want to detect Spring annotations and infer whether a file is a controller, service, repository, DTO, or entity.

### Acceptance Criteria

* detect class-level annotations
* map file to a logical layer

---

## US-3.3 Save parsed file metadata

**As the system**, I want to store parsed metadata so that review rules can reuse it.

### Acceptance Criteria

* metadata stored with project linkage
* file path and layer are stored

---

# EPIC E4 — Rule Engine MVP

## US-4.1 Run rule engine for uploaded project

**As a developer**, I want the system to run review rules on my project and generate findings.

### Acceptance Criteria

* review can be triggered for a project
* issues are generated and saved

---

## US-4.2 Detect field injection

**As a developer**, I want field injection usage to be flagged so I can follow Spring best practices.

---

## US-4.3 Detect controller to repository direct access

**As a developer**, I want controllers that directly access repositories to be flagged.

---

## US-4.4 Detect missing `@Valid`

**As a developer**, I want endpoints that accept request DTOs without validation to be flagged.

---

## US-4.5 Detect missing global exception handler

**As a developer**, I want projects without centralized exception handling to be flagged.

---

## US-4.6 Detect long service methods

**As a developer**, I want long service methods to be flagged for maintainability concerns.

---

# EPIC E5 — Review Reporting APIs

## US-5.1 Save review issues

**As the system**, I want review findings to be stored so that reports can be generated later.

## US-5.2 Get review results by project

**As a developer**, I want to fetch review results for a project.

## US-5.3 Get project review summary

**As a developer**, I want a project-level summary of issue counts and review health.

---

# EPIC E6 — AI Explanation Layer

## US-6.1 Generate AI explanation for issue

**As a developer**, I want AI to explain what is wrong with the code and why it matters.

## US-6.2 Generate fix suggestion

**As a developer**, I want AI to suggest how to fix an issue.

## US-6.3 Save AI explanation result

**As the system**, I want AI explanations to be stored and linked to issues.

---

# EPIC E7 — Health Score & Insights

## US-7.1 Generate project health score

**As a developer**, I want a project-level score that summarizes code quality.

## US-7.2 Generate architecture summary

**As a developer**, I want a summary of architecture strengths and weaknesses.
