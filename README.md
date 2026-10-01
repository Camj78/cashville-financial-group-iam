# Cashville Financial Group — Identity & Access Management

> An enterprise-style Identity & Access Management implementation built in Microsoft Entra ID, documenting the design, implementation, validation, and troubleshooting of identity security controls.

## 🏦 Project Overview

Cashville Financial Group (CFG) is a fictional financial services organization used to simulate real-world Identity & Access Management challenges in a Microsoft Entra environment.

Rather than treating each exercise as an isolated lab, this project follows the development of CFG's identity program across multiple implementation phases. Each phase begins with business and security requirements and documents the resulting IAM design, configuration, testing, troubleshooting, and lessons learned.

The objective is to demonstrate practical IAM engineering skills through hands-on implementation rather than certification knowledge alone.

---

## 🎯 IAM Program Objectives

The Cashville Financial Group IAM program is designed to:

- Establish a secure and scalable identity foundation.
- Apply least-privilege access principles.
- Separate standard workforce identities from privileged administrative identities.
- Reduce standing privileged access.
- Establish controlled administrative boundaries.
- Protect emergency administrative access.
- Implement identity lifecycle and access governance controls.
- Validate IAM configurations through testing and evidence.
- Document technical decisions and troubleshooting processes.

---

## 🗺️ Implementation Roadmap

| Phase | Implementation | Status |
|---|---|---|
| **Phase 1** | Identity Design | ✅ Complete |
| **Phase 2** | Coming Next | 🟡 In Progress |
| **Phase 3** | Planned | ⚪ Planned |
| **Phase 4** | Planned | ⚪ Planned |
| **Phase 5** | Planned | ⚪ Planned |

---

## 🧩 Phase 1 — Identity Design

Phase 1 establishes the foundational identity and privileged-access model for Cashville Financial Group.

The implementation includes:

- Workforce identity design
- Separation of workforce and privileged administrative identities
- Emergency access accounts
- Microsoft Entra administrative roles
- Administrative Units
- Scoped administration
- Least-privilege role design
- Microsoft Entra Privileged Identity Management (PIM)
- Privileged-access validation
- Microsoft Graph troubleshooting and validation

### Key Security Principles

**Least Privilege**  
Administrative permissions are limited to the access and scope required to perform the assigned responsibility.

**Privileged Identity Separation**  
Administrative activity is separated from normal workforce activity to reduce exposure of privileged credentials.

**Administrative Scoping**  
Administrative Units are used to constrain identity administration to defined organizational boundaries.

**Just-in-Time Privileged Access**  
Privileged Identity Management is incorporated into the administrative model to reduce persistent privileged access.

**Emergency Access**  
Dedicated emergency-access identities provide a recovery path for critical administrative scenarios.

➡️ **[View the complete Phase 1 implementation](./phase-1-identity-design/README.md)**

---

## 🛠️ Technologies & Platforms

- Microsoft Entra ID
- Microsoft Entra Privileged Identity Management (PIM)
- Microsoft Graph
- Microsoft Azure
- Microsoft 365

---

## 🔐 IAM Concepts Demonstrated

`Identity Administration` • `RBAC` • `Least Privilege` • `Privileged Access` • `Administrative Units` • `PIM` • `Emergency Access` • `Identity Governance` • `Microsoft Graph` • `Zero Trust`

---

## 📸 Documentation Approach

Each implementation phase contains supporting technical evidence including:

- Architecture and design decisions
- Configuration screenshots
- Security rationale
- Testing and validation
- Troubleshooting investigations
- Final-state evidence
- Lessons learned

Sensitive information is removed or sanitized before publication.

---

## 👤 About This Project

This project is part of my hands-on development in Identity & Access Management and Microsoft Entra ID.

The environment is designed to translate IAM concepts into practical implementation experience while developing the technical reasoning required for IAM Analyst and IAM Engineer responsibilities.

> **Note:** Cashville Financial Group is a fictional organization created solely for this IAM lab environment. No production company identities or systems are represented in this repository.
