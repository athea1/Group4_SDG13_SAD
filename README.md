# Group4_SDG13_SAD

# CarbonTrack: SOAST Students Carbon Footprint Monitoring System

![SDG 13: Climate Action](https://img.shields.io/badge/SDG-13_Climate_Action-28B463?style=for-the-badge&logo=unicef)
![Methodology: Agile SDLC](https://img.shields.io/badge/Methodology-Agile_SDLC-0052CC?style=for-the-badge)
![Architecture: 3-Tier](https://img.shields.io/badge/Architecture-3--Tier-FF9900?style=for-the-badge)

## Project Title and SDG Goal
**Project Title:** CarbonTrack: SOAST Students Carbon Footprint Monitoring System  
**Sustainable Development Goal:** SDG 13 (Climate Action) - Taking urgent action to combat climate change and its impacts through institutional data monitoring and awareness.

### The Problem Statement
Currently, the NTC School of Arts, Sciences, & Technology (SOAST) department relies on a manual and highly fragmented process to monitor the environmental footprint of its student body. Data collection for sustainability metrics (such as travel distance, campus electricity usage, and waste volume) is tedious, prone to typographical errors, and lacks a proper verification mechanism. 

Furthermore, this manual approach creates severe operational bottlenecks for Program Heads who need to validate the submissions, and it significantly delays the NTC Management in generating accurate, aggregated data for official institutional sustainability campaigns. Without a centralized system, maintaining data integrity and enforcing the Data Privacy Act (DPA) during data collection remains a significant challenge.

---

## Project Description
**CarbonTrack** is a centralized, secure, and web-based digital platform specifically designed to automate the logging, calculation, and validation of the SOAST department's environmental metrics. 

The system provides a seamless workflow divided into three core modules: 
1. **Student Dashboard:** Enables students to input raw numerical metrics and instantly outputs their computed Carbon Footprint Score ($CO_2e$) alongside automated "Eco-Tips" for behavioral change.
2. **Program Head Dashboard:** Serves as a strict validation chokepoint, allowing department heads to review, approve, or reject student logs to maintain data integrity.
3. **Management Dashboard:** Automatically aggregates "Approved Data Only" to generate filterable Official Sustainability Reports for the NTC Administration.

### Overview and Justification of the Architecture Used
The CarbonTrack system is engineered using a robust **3-Tier Architecture** to guarantee maximum security, scalability, and maintainability. This architectural choice is justified by the following implementations:

* **Tier 1: Presentation Layer (Client-Side):** This layer handles the user interfaces for three distinct roles (Students, Program Heads, Management) via standard web browsers. It is decoupled from the backend to ensure a responsive, lightweight, and intuitive UI/UX without exposing raw database structures.
* **Tier 2: Application Layer (Middleware & Business Logic):** Acting as the "brain" of the system, this layer processes all encrypted requests. It houses the *Authentication Controller* (for Role-Based Access Control and DPA compliance), the *Carbon Calculation Engine* (for complex math formulations), and the *Validation Workflow Logic*. This prevents the client side from directly manipulating footprint calculations or bypassing approval protocols. 
* **Tier 3: Data Layer (Backend Storage):** A highly structured Relational Database Management System (RDBMS) is utilized to strictly enforce data schemas. This layer exclusively receives verified commit logs from the Application layer, ensuring that all `tbl_carbon_logs` and `tbl_users` remain centralized, secure, and highly available for reporting queries.

---

## Contributors
The system analysis, architectural modeling, and documentation of the CarbonTrack system were collaboratively developed by the following team members (BSIT - 2.3):

| Name | Role / Assigned Contribution | GitHub Profile |
| :--- | :--- | :--- |
| **Athea Glaise Tarnate** | Lead System Analyst / Module: Authentication & Student Dashboard | [@athea1](https://github.com/athea1) |
| **Prince Wesley Dela Pasion**| Software Architect / Module: System Infrastructure & DFDs | [@westdp17](https://github.com/westdp17) | 
| **Brix Charles Caparon** | Database Designer / Module: Logical ERD & Data Architecture | [@424005722-Brix](https://github.com/424005722-Brix)) |
| **Eucel Penarubia** | UI/UX Designer / Module: Wireframing & Core User Journey | [@username](https://github.com/) |
| **Christian Camano** | QA Specialist / Module: Validation Plan & Requirements Traceability | [@Kisatsune](https://github.com/Kisatsune) |
| **Quelly De Los Santos** | Technical Writer / Module: Feasibility Analysis & Documentation | [@elly006](https://github.com/elly006) |

