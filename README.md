# Cashville Financial Group — Identity & Access Management Portfolio

**Microsoft Entra ID | Identity Governance | Privileged Access | Joiner–Mover–Leaver (JML) | Least Privilege**

> **Independent hands-on portfolio lab.** Cashville Financial Group (CFG) is a simulated financial-services organization. The environment, people, and workflows are lab scenarios, not a production client deployment.

## Project overview

I designed and tested identity and access management controls in Microsoft Entra ID, documenting not just configuration steps but security decisions, validation results, audit evidence, troubleshooting, and technical limitations.

The project progresses from a **secure identity and privileged-administration foundation** (Phase 1) to **workforce identity lifecycle and access changes** (Phase 2).

## Architecture at a glance

```text
                Cashville Financial Group (simulated)
                               |
                        Microsoft Entra ID
                               |
           +-------------------+--------------------+
           |                                        |
    Phase 1: Identity Design               Phase 2: Lifecycle
           |                                        |
    Workforce / Admin separation             Identity attributes
    Emergency-access accounts                       |
    Administrative Unit scope                 Dynamic security groups
    PIM-eligible admin access                        |
    Validation & cleanup                     Group-based app assignment
                                                    |
                                         Joiner / Mover / Leaver tests
                                         Account disable + audit logs
```

## Completed lab phases

| Phase | Focus | Evidence and documentation |
|---|---|---|
| **01 — Identity Design** | Workforce/privileged identity separation, emergency access, Administrative Units, scoped Entra roles, PIM eligibility, troubleshooting, privilege cleanup | [Phase 1 README](phase-1-identity-design/README.md) |
| **02 — Identity Lifecycle Management** | Joiner, mover, leaver; dynamic security groups; inherited enterprise app assignment; account disablement, session revocation and audit validation | [Phase 2 README](phase-2-identity-lifecycle/README.md) · [Evidence index](phase-2-identity-lifecycle/EVIDENCE_INDEX.md) · [Case study](phase-2-identity-lifecycle/PORTFOLIO_CASE_STUDY.md) |

## Selected technical outcomes

**Phase 1 — secure identity administration**
- Separated normal workforce and privileged administrator identities.
- Established emergency-access accounts and scoped regional administration with an Administrative Unit.
- Tested PIM-eligible role access, investigated configuration issues, and cleaned up temporary privilege and Graph write permissions.

**Phase 2 — access follows identity lifecycle**
- **Joiner:** Created a Finance identity and verified dynamic Finance group membership and group-inherited CFG Finance Portal assignment.
- **Mover:** Changed a Finance employee to Marketing and verified the Finance group-derived app assignment disappeared.
- **Leaver:** Disabled a contractor account, revoked Entra sign-in sessions, and examined audit evidence.

## Security and engineering principles

- **Least privilege:** Grant only the permissions appropriate to identity, role, and scope.
- **Attribute quality:** Dynamic membership is only as reliable as its source attributes.
- **Separation of concerns:** Entra group-derived assignments are not the same as downstream application account provisioning.
- **Layered offboarding:** Disabling an account and revoking Entra sessions do not guarantee that all independent application sessions end immediately.
- **Evidence-driven validation:** Capture before/after states and audit logs, and document limitations instead of claiming controls that were not tested.

## Repository structure

```text
cashville-financial-group-iam/
├── README.md
├── phase-1-identity-design/
│   ├── README.md
│   ├── architecture/
│   ├── evidence/
│   └── troubleshooting/
└── phase-2-identity-lifecycle/
    ├── README.md
    ├── EVIDENCE_INDEX.md
    ├── PORTFOLIO_CASE_STUDY.md
    ├── PUBLISHING_GUIDE.md
    └── screenshots/   (26 evidence captures)
```

## Scope and transparency

This is a cloud-only educational lab, not a production deployment. Phase 2 does **not** demonstrate HRIS-driven automated account creation, SCIM downstream deprovisioning, real Finance Portal sign-in enforcement, or application-side session termination. See each phase's README for the specific implementation and evidence.

**For recruiters and hiring managers:** Start with the [Phase 2 case study](phase-2-identity-lifecycle/PORTFOLIO_CASE_STUDY.md), then follow the [Phase 2 evidence index](phase-2-identity-lifecycle/EVIDENCE_INDEX.md) or explore the [Phase 1 design](phase-1-identity-design/README.md).
