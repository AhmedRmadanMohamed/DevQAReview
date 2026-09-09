<div align="center">

# DevQA

**IntelliJ IDEA Plugin for Spring Boot Project Intelligence & Pre-QA Analysis**

DevQA helps Spring Boot developers understand their repositories, surface project structure, and build stronger software quality awareness directly inside IntelliJ IDEA.

[Watch the Demo on LinkedIn](https://www.linkedin.com/posts/ahmedramadanmohamedsmaha_java-springboot-intellijidea-activity-7503421471629762560-otMz)

</div>

---

## About DevQA

DevQA is a long-term developer tooling project built around a roadmap of **30+ major features** focused on project intelligence, architecture understanding, software quality analysis, testing, developer productivity, and pre-QA engineering workflows.

The project is being developed as an IntelliJ IDEA plugin so analysis and quality insights stay close to the developer workflow instead of living in a separate external tool.

> **Current status:** Feature 1 — **Project Brain** has reached its first implementation milestone and is currently under testing, validation, and production hardening.

## Project Brain

Project Brain is the foundation for the rest of DevQA. It is designed to build an initial understanding of a Spring Boot repository and provide a reusable project model for future DevQA capabilities.

Current capabilities include:

- Scanning and understanding project structure
- Discovering and classifying project files
- Analyzing Java source code and Spring components
- Identifying application layers and component roles
- Detecting configuration, resource, build, SQL, and documentation assets
- Presenting repository analysis through an interactive IntelliJ IDEA dashboard
- Providing repository-level inventory and project metrics

## Current Demo Snapshot

The current Project Brain milestone can analyze a Spring Boot repository and present information such as:

- Project files
- Java classes
- Controllers
- Services
- Repositories
- Entities
- DTOs
- Project file groups and source locations

The screenshots in this repository show DevQA analyzing a sample **HumanResourcesSystem** Spring Boot project.

## Roadmap — 30 Major Features

### System Foundation
1. **Project Brain** — Under Testing
2. Code Understanding Engine — Planned
3. Business Brain — Planned

### Intent Assurance
4. Requirement Understanding — Planned
5. Business Confirmation Engine — Planned
6. Requirement Gap Detection — Planned

### System Intelligence
7. Change Impact Analysis — Planned
8. Dependency Intelligence — Planned
9. Architecture Intelligence — Planned
10. API Intelligence — Planned
11. Database Intelligence — Planned
12. JPA / Hibernate Analyzer — Planned
13. SQL Intelligence — Planned

### Engineering Assurance
14. Security Analyzer — Planned
15. Code Quality Analyzer — Planned
16. Testing Intelligence — Planned
17. QA Scenario Generator — Planned
18. Automated Test Generator — Planned
19. Performance Analyzer — Planned
20. Concurrency Analyzer — Planned
21. Transaction Intelligence — Planned
22. Microservices Intelligence — Planned
23. Observability Intelligence — Planned

### AI & Enterprise
24. AI Explanation Engine — Planned
25. AI Fix Recommendation — Planned
26. Project Health Score — Planned
27. Reports & Dashboard — Planned
28. Enterprise Management — Planned
29. CI/CD & Git Integration — Planned
30. DevQA Platform Ecosystem — Planned

## Technology Direction

DevQA is currently built around:

- **Kotlin**
- **IntelliJ Platform SDK**
- **IntelliJ PSI / code analysis APIs**
- **Swing / IntelliJ UI components**
- **Spring Boot project analysis**

The architecture is being designed with clear feature boundaries so additional analysis engines can be added without turning the plugin into a tightly coupled codebase.

## Demo

A working demo of the current Project Brain milestone is available here:

**LinkedIn Demo:**  
https://www.linkedin.com/posts/ahmedramadanmohamedsmaha_java-springboot-intellijidea-activity-7503421471629762560-otMz

## Source Code Availability

This repository is a **public product showcase** for DevQA.

The DevQA source code is currently maintained in a private repository and is **not distributed through this showcase repository**. Screenshots, product information, roadmap material, and demonstrations are provided here to document development progress and present the project publicly.

## Development Status

DevQA is actively under development.

The current focus is validating and hardening the first Project Brain milestone before continuing with the next major roadmap capability.

---

<div align="center">

**DevQA — Understand • Analyze • Validate**

</div>
