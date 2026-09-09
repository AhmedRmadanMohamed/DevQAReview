# DevQA Showcase Guide

[Back to the product overview](../README.md) · [Feature reference](FEATURES.md)

This guide walks through **Project Brain**, DevQA's first repository intelligence module, using 11 screenshots captured inside IntelliJ IDEA. The sample project is **HumanResourcesSystem**, a Spring Boot application.

The capture documents the current demonstration build under testing and validation. It is a product walkthrough, not an installation guide.

## Tour at a glance

| Step | View | What to inspect |
| --- | --- | --- |
| 1 | [Launch](#1-open-the-devqa-tool-window) | Open the DevQA tool window |
| 2 | [Ready](#2-start-a-repository-analysis) | Confirm the project and start the scan |
| 3 | [Analysis in progress](#3-follow-the-analysis-state) | Observe the current analysis state |
| 4 | [Overview](#4-read-the-dashboard) | Review the repository snapshot |
| 5 | [Components](#5-review-the-component-inventory) | Browse six component and class views |
| 6 | [Project Files](#6-explore-project-files) | Inspect file groups and resource types |

## 1. Open the DevQA tool window

With a Spring Boot project open, select **View → Tool Windows → DevQA**. The screenshot shows the DevQA entry within IntelliJ IDEA's standard Tool Windows menu.

![IntelliJ IDEA menu path View, Tool Windows, DevQA](../assets/screenshots/open-tool-window.png)

## 2. Start a repository analysis

The tool window identifies **HumanResourcesSystem** as the current project. Its status is **Ready**, and the primary action is **Analyze Repository**.

![DevQA tool window with the current project, Ready status, and Analyze Repository action](../assets/screenshots/ready-to-analyze.png)

Select **Analyze Repository** to begin the scan.

## 3. Follow the analysis state

During the scan, the tool window displays **Analyzing repository**, a progress indicator, and an **Analyzing...** action state.

![DevQA repository analysis in progress](../assets/screenshots/analysis-in-progress.png)

After completion, the status changes to **Analysis complete** and the primary action becomes **Analyze Again**. Results appear in the **DevQA Analysis - HumanResourcesSystem** editor tab.

## 4. Read the dashboard

The **Overview** tab presents three complementary sections:

- **Headline metrics:** project files, Java classes, controllers, services, repositories, and entities.
- **Project Profile:** framework identification, Java files, DTOs, and all classes.
- **Detected Layer Inventory:** counts for controllers, services, repositories, entities, and DTOs.

![DevQA Project Brain Overview dashboard for HumanResourcesSystem](../assets/screenshots/dashboard.png)

The **Spring Boot** indicator describes the detected project framework. **Analysis complete** describes scan completion, rather than a passed test suite or a quality certification.

## 5. Review the component inventory

The **Components** tab contains six views. Names and counts below belong to the sample project shown in the captures.

### Controllers

Four detected controllers appear in the inventory: `EmployeeController`, `EmployersController`, `JobPositionController`, and `UsersInformationController`.

![Controller inventory containing four detected controller types](../assets/screenshots/components-controllers.png)

### Services

Four detected services appear: `EmployeeService`, `EmployersService`, `JobPositionService`, and `UsersInformationService`.

![Service inventory containing four detected service types](../assets/screenshots/components-services.png)

### Repositories

The view reports **16 repositories** and displays a scrollable inventory that includes `CompanyRepository`, `DepartmentsRepository`, and `EmployeeRepository`.

In this view, a repository is an application persistence component. It is distinct from the Git repository being analyzed.

![Persistence repository inventory with a reported total of sixteen](../assets/screenshots/components-repositories.png)

### Entities

The view reports **16 entities**. Visible examples include `CitiesEntity`, `EmployeeEntity`, `EmploymentsEntity`, and `TenantEntity`.

![Persistence entity inventory with a reported total of sixteen](../assets/screenshots/components-entities.png)

### DTOs

Four detected DTOs appear: `EmployersDTO`, `JobPositionDTO`, `TenantDTO`, and `UserInformationDTO`.

![Data transfer object inventory containing four detected DTO types](../assets/screenshots/components-dtos.png)

### All Classes

This view presents fully qualified Java type names, making package context visible alongside class names. Its reported total is **72**.

![All Classes inventory showing fully qualified names and an abbreviated remainder](../assets/screenshots/components-all-classes.png)

The screenshot ends with **“… 47 more classes”**. It demonstrates an abbreviated presentation of the inventory, rather than every class name being rendered in the captured list.

## 6. Explore project files

The **Project Files** tab organizes discovered files by source category and then by file type.

![Project Files tree with Main, Test, Resource, and Unknown groups](../assets/screenshots/project-files.png)

| Source category | Displayed total | Visible file-type groups |
| --- | ---: | --- |
| Main | 69 | Java Source (69) |
| Test | 3 | Java Source (2), Properties (1) |
| Resource | 11 | Properties (1), SQL (10) |
| Unknown | 5 | Maven (1), YAML (2), Documentation (1), Other (1) |

**Unknown** is a source-category label. The files beneath it may still have a recognized file type, such as Maven or YAML. The screenshot does not establish why those files were placed in that category.

## Reading the example counts

The dashboard displays **88 project files**, **72 Java classes**, **4 controllers**, **4 services**, **16 repositories**, **16 entities**, and **4 DTOs**.

Use these figures as a record of the captured demonstration:

- **Source groups reconcile to 88 files:** Main (69) + Test (3) + Resource (11) + Unknown (5).
- **Java file totals differ across views:** the dashboard's Project Profile shows Java Files (72), while the Project Files tree shows Java Source (69) under Main and Java Source (2) under Test. That visible total is 71. The screenshots do not explain the difference; the classification behavior remains under validation.
- **Layer totals are component counts:** they should not be added to the All Classes total. They describe detected categories within the analyzed project.
- **Detection is the current focus:** the screenshots show an inventory and analysis workflow, rather than evidence of detection accuracy, test coverage, security scanning, or performance measurements.

For terminology and current scope, see the [feature reference](FEATURES.md).

## Presenting the demonstration

A concise product walkthrough can follow this sequence:

1. Introduce DevQA as Spring Boot repository intelligence inside IntelliJ IDEA.
2. Open the tool window and start the analysis.
3. Use Overview to orient the audience to the project snapshot.
4. Move through the component views to explain the detected layers.
5. Open Project Files to include source, test, configuration, and resource assets.
6. Close with the current testing milestone and the separately labeled [product roadmap](../README.md#roadmap).

[Watch the LinkedIn demo](https://www.linkedin.com/posts/ahmedramadanmohamedsmaha_java-springboot-intellijidea-activity-7503421471629762560-otMz) or return to the [README](../README.md).
