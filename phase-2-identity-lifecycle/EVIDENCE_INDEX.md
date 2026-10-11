# Phase 2 — Evidence Index

**Scope:** 26 screenshots supporting Joiner–Mover–Leaver (JML) tests in a simulated Microsoft Entra ID environment. Descriptions explain the intended evidence shown by each named capture; they do not imply end-to-end application provisioning or production operation.

| Evidence | What it demonstrates |
|---|---|
| [CFG-Phase2-David-Contractor-Identity-Attributes.png](screenshots/CFG-Phase2-David-Contractor-Identity-Attributes.png) | David's Finance / Apex Consulting / Contractor identity attributes; baseline for testing employee-only group exclusion. |
| [CFG-Phase2-David-Leaver-Account-Disabled-Audit.png](screenshots/CFG-Phase2-David-Leaver-Account-Disabled-Audit.png) | Audit detail documenting the account-enabled property changing from true to false. |
| [CFG-Phase2-David-Leaver-Account-Disabled.png](screenshots/CFG-Phase2-David-Leaver-Account-Disabled.png) | David's user account after administrative sign-in disablement. |
| [CFG-Phase2-David-Leaver-Applications-Before.png](screenshots/CFG-Phase2-David-Leaver-Applications-Before.png) | David's application assignments view before offboarding; no assignments shown. |
| [CFG-Phase2-David-Leaver-Before-Disable.png](screenshots/CFG-Phase2-David-Leaver-Before-Disable.png) | David's enabled-account baseline before the offboarding action. |
| [CFG-Phase2-David-Leaver-Groups-Before.png](screenshots/CFG-Phase2-David-Leaver-Groups-Before.png) | David's group membership view before offboarding; baseline for exclusion verification. |
| [CFG-Phase2-David-Leaver-Session-Revocation-Audit-Activity.png](screenshots/CFG-Phase2-David-Leaver-Session-Revocation-Audit-Activity.png) | Audit activity entry for the administrative session-revocation operation. |
| [CFG-Phase2-David-Leaver-Sessions-Revoked-Audit.png](screenshots/CFG-Phase2-David-Leaver-Sessions-Revoked-Audit.png) | Audit details showing the refresh-token validity timestamp update after revocation. |
| [CFG-Phase2-David-Leaver-Sessions-Revoked.png](screenshots/CFG-Phase2-David-Leaver-Sessions-Revoked.png) | Entra user interface state following the revoke-sessions action; does not prove termination of independent app sessions. |
| [CFG-Phase2-Dynamic-Rule-CompanyName-Workaround.png](screenshots/CFG-Phase2-Dynamic-Rule-CompanyName-Workaround.png) | Troubleshooting evidence for use of companyName as an identity attribute in the dynamic membership rule. |
| [CFG-Phase2-Dynamic-Rule-EmployeeType-Unsupported.png](screenshots/CFG-Phase2-Dynamic-Rule-EmployeeType-Unsupported.png) | Troubleshooting evidence of the employeeType rule limitation encountered in the lab. |
| [CFG-Phase2-Finance-Dynamic-Group-Rule.png](screenshots/CFG-Phase2-Finance-Dynamic-Group-Rule.png) | Finance dynamic group membership rule configuration; documents the employee-only eligibility criteria used in the lab. |
| [CFG-Phase2-Finance-Portal-Assignment-Required.png](screenshots/CFG-Phase2-Finance-Portal-Assignment-Required.png) | CFG Finance Portal enterprise application setting requiring assignment. |
| [CFG-Phase2-Finance-Portal-Group-Assignment.png](screenshots/CFG-Phase2-Finance-Portal-Group-Assignment.png) | CFG Finance Employees security group assigned to the CFG Finance Portal enterprise application. |
| [CFG-Phase2-Joiner-Jonathan-Dynamic-Group-Membership.png](screenshots/CFG-Phase2-Joiner-Jonathan-Dynamic-Group-Membership.png) | Jonathan's membership in CFG Finance Employees after dynamic rule evaluation. |
| [CFG-Phase2-Joiner-Jonathan-Identity-Attributes.png](screenshots/CFG-Phase2-Joiner-Jonathan-Identity-Attributes.png) | Jonathan's joiner identity record showing Finance department, CFG company, employee type, title, and employee ID. |
| [CFG-Phase2-Joiner-Jonathan-Inherited-App-Assignment.png](screenshots/CFG-Phase2-Joiner-Jonathan-Inherited-App-Assignment.png) | Jonathan's CFG Finance Portal assignment inherited through Finance group membership. |
| [CFG-Phase2-Marketing-Dynamic-Membership-Validated.png](screenshots/CFG-Phase2-Marketing-Dynamic-Membership-Validated.png) | Validation of the Marketing dynamic group membership configuration or evaluation. |
| [CFG-Phase2-Sarah-Finance-Group-Removal.png](screenshots/CFG-Phase2-Sarah-Finance-Group-Removal.png) | Sarah no longer appears in the Finance group after the mover attribute change. |
| [CFG-Phase2-Sarah-Finance-Identity-Attributes-Updated.png](screenshots/CFG-Phase2-Sarah-Finance-Identity-Attributes-Updated.png) | Intermediate updated identity attributes during Sarah's mover workflow. |
| [CFG-Phase2-Sarah-Finance-Identity-Attributes.png](screenshots/CFG-Phase2-Sarah-Finance-Identity-Attributes.png) | Sarah's original Finance identity attributes before the department transfer. |
| [CFG-Phase2-Sarah-Finance-Membership-Restored.png](screenshots/CFG-Phase2-Sarah-Finance-Membership-Restored.png) | Finance group membership restored during the mover scenario validation/reset. |
| [CFG-Phase2-Sarah-Finance-Portal-Assignment-Removed.png](screenshots/CFG-Phase2-Sarah-Finance-Portal-Assignment-Removed.png) | Sarah's Finance Portal group-derived application assignment no longer appears after Finance membership removal. |
| [CFG-Phase2-Sarah-Inherited-Finance-Portal-Assignment.png](screenshots/CFG-Phase2-Sarah-Inherited-Finance-Portal-Assignment.png) | Sarah's original inherited Finance Portal application assignment while eligible through Finance membership. |
| [CFG-Phase2-Sarah-Marketing-Membership-Final.png](screenshots/CFG-Phase2-Sarah-Marketing-Membership-Final.png) | Sarah's final Marketing group membership after transfer. |
| [CFG-Phase2-Sarah-Marketing-Mover-Attributes.png](screenshots/CFG-Phase2-Sarah-Marketing-Mover-Attributes.png) | Sarah's identity attributes reflecting her Finance-to-Marketing transfer. |

## How to interpret the evidence

- **Joiner:** Administratively created identity → dynamic group evaluation → inherited enterprise app assignment. No HRIS-triggered user provisioning is claimed.
- **Mover:** Attribute update → dynamic group reevaluation → removal of the group-derived Finance Portal assignment. This is not proof of downstream account deletion or application session termination.
- **Leaver:** Contractor exclusion baseline, manual account disablement, manual Entra session revocation, and corresponding audit entries. David had no pre-existing group or app entitlement to remove.
- **Troubleshooting:** Rule-design screenshots capture the attribute and expression limitations encountered; validate production rules against supported Entra properties before reuse.

## Publication and privacy checklist

- [x] All 26 screenshot filenames inventoried in `screenshots/`
- [x] README image references match inventoried filenames
- [x] Phase 2 linked from repository root README
- [ ] **Privacy clearance pending:** inspect the actual pixels of all 26 images, including header account names, UPNs, domains, object IDs, tenant IDs, audit actors, timestamps, and IP addresses. Redact personal or security-sensitive data as appropriate.
- [ ] Check rendered screenshots after any redactions are committed
- [ ] Confirm the repository's public visibility and intended sharing audience

**Privacy note:** The presence of fictional test-user names does not guarantee that the signed-in administrator account or tenant metadata is fictional. Do not treat this index as a privacy approval.
