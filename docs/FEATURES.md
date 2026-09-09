# Project Brain: capability reference

[Project overview](../README.md) · [Visual walkthrough](SHOWCASE.md)

**Project Brain is DevQA's first module and is under testing and validation.** It presents a Spring Boot repository snapshot inside IntelliJ IDEA, with an overview, a component inventory, and a grouped file browser. This page describes the interface demonstrated in the supplied screenshots and separates it from the wider product roadmap.

DevQAReview is a public product showcase. The production source code is private, and this repository currently provides no public release or installable plugin package.

## Current demonstrated capabilities

| Capability | What the current showcase demonstrates |
| --- | --- |
| IDE integration | A DevQA tool window accessible through **View → Tool Windows → DevQA**. |
| Project context | The current project's name and analysis status appear in the tool window. |
| Repository analysis | An **Analyze Repository** action, an in-progress state, and a completed state with **Analyze Again**. |
| Framework identification | The analyzed example is identified as **Spring Boot** in the result header and project profile. |
| Repository overview | Summary cards and inventories display project-file, Java-type, and component counts. |
| Component inventory | Dedicated views for controllers, services, repositories, entities, DTOs, and all discovered classes. |
| File inventory | A tree groups project files by source category and file type, including resources, configuration, SQL, and documentation. |
| Results workspace | A **DevQA Analysis - HumanResourcesSystem** editor tab contains **Overview**, **Components**, and **Project Files**. |

These demonstrations establish the current user experience. They do not establish a compatibility matrix, exhaustive detection coverage, or performance benchmarks.

## Analysis lifecycle

1. **Open DevQA.** In IntelliJ IDEA, select **View → Tool Windows → DevQA**.
2. **Check the project context.** The tool window displays the current project and a **Ready** status.
3. **Start the analysis.** Select **Analyze Repository**. The captured in-progress state reads **Analyzing repository**, and the action reads **Analyzing…**.
4. **Review the snapshot.** The completed state reads **Analysis complete**. Results are shown in the analysis editor tab.
5. **Request a fresh analysis.** The completed tool window exposes **Analyze Again**.

The screenshots document these interface states; they do not specify analysis duration or automatic refresh behavior. **Analysis complete** describes completion of repository analysis, not passing tests or QA approval.

See the [visual walkthrough](SHOWCASE.md) for the corresponding screens.

## Overview and metrics

The **Overview** tab combines summary cards, a **Project Profile**, and a **Detected Layer Inventory**. The screenshots use **HumanResourcesSystem**, a Spring Boot application, as the analyzed example.

| Metric | Meaning in the demonstrated interface | Example snapshot |
| --- | --- | ---: |
| Project files | Files included in the displayed repository analysis. | 88 |
| Java classes | Discovered Java types reported by the dashboard. | 72 |
| Controllers | Components listed in the Controllers view. | 4 |
| Services | Components listed in the Services view. | 4 |
| Repositories | Persistence components listed in the Repositories view. | 16 |
| Entities | Persistence domain types listed in the Entities view. | 16 |
| DTOs | Types listed in the DTOs view. | 4 |

These values belong to one example snapshot. They are not DevQA's own source-code statistics, quality scores, test-coverage percentages, or expected results for other projects.

The dashboard labels **Java Classes**, **Java Files**, and **All Classes** each show 72 in this capture. The visible Project Files tree separately shows 69 main Java source files and two test Java source files. The screenshots alone do not explain that difference, so these labels should not be treated as interchangeable counting definitions.

## Component inventory

The **Components** tab organizes the detected inventory into six views:

| View | Purpose | Example shown |
| --- | --- | --- |
| Controllers | Review the detected web-entry-point components. | `EmployeeController` |
| Services | Review the detected service components. | `EmployeeService` |
| Repositories | Review the application's persistence repository types. | `CompanyRepository` |
| Entities | Review the detected persistence domain types. | `EmployeeEntity` |
| DTOs | Review the detected data transfer objects. | `EmployersDTO` |
| All Classes | Inspect fully qualified Java type names across the discovered inventory. | `HumanResourcesPackage.Controllers.JobPositionController` |

**Repositories** here refers to application persistence components rather than Git repositories.

The category counts describe the displayed analysis result. The public showcase does not define the exact annotation, naming, inheritance, or package rules used for classification. A type's inclusion or absence in a category should therefore be reviewed in the context of the module's testing status.

### All Classes display

The supplied All Classes screenshot includes fully qualified names and ends with **“… 47 more classes”**. The visible list is abbreviated even though its tab reports 72 classes. Do not interpret the displayed entries as the full inventory or assume that every result is visible in that screen.

The [visual walkthrough](SHOWCASE.md) includes each component view.

## Project Files

The **Project Files** tab presents a tree with two visible grouping levels: source category and file type. In the example capture, it contains:

| Source category | File-type groups shown | Displayed total |
| --- | --- | ---: |
| Main | Java Source: 69 | 69 |
| Test | Java Source: 2; Properties: 1 | 3 |
| Resource | Properties: 1; Sql: 10 | 11 |
| Unknown | Maven: 1; Yaml: 2; Documentation: 1; Other: 1 | 5 |

The **Unknown** bucket is part of the demonstrated grouping. A file can appear there while still having a recognized file type, such as Maven or YAML. Its presence does not by itself indicate an invalid file or failed analysis; it shows that the interface has not assigned the file to one of the other displayed source categories.

The capture demonstrates expandable groups and inventory counts. It does not establish file editing, source navigation, export, or a complete set of supported file formats.

## Current scope and interpretation

Project Brain currently demonstrates repository discovery and structural inspection. Use the snapshot to orient yourself in a codebase and identify areas for closer review.

- **Testing status:** detection accuracy and behavior remain subject to validation.
- **Example-specific evidence:** the screenshots cover one Spring Boot project and one IDE environment.
- **Inventory semantics:** counts and categories are analysis outputs; they do not establish architectural correctness or component health.
- **Abbreviated results:** the All Classes screenshot does not display the full reported inventory.
- **Public availability:** this repository contains documentation and showcase material; no public installation workflow is available yet.

## Product vision and future direction

The wider DevQA vision is to help developers understand software quality before work reaches QA. The existing roadmap describes a planned platform with more than 30 major features across these areas:

| Future area | Intended direction |
| --- | --- |
| Architecture intelligence | Deeper understanding of application structure and architectural relationships. |
| Dependency intelligence | Greater visibility into dependencies and their relationships. |
| Security analysis | Security-focused repository analysis. |
| Code quality analysis | Additional signals for reviewing maintainability and code quality. |
| Testing intelligence | Support for understanding testing needs and test-related quality. |
| AI explanations and recommendations | Explanations and suggested fixes built on project understanding. |
| Project health scoring | A broader view of project health. |
| CI/CD integration | Integration with engineering delivery workflows. |

These are roadmap directions, not capabilities demonstrated by the current Project Brain screenshots. No delivery dates or release commitments are implied.

Return to the [project overview](../README.md) or explore the [visual walkthrough](SHOWCASE.md).
