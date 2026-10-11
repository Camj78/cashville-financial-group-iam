# Case study — CFG Identity Lifecycle Management

## Business problem

A simulated financial services company needs access to follow a worker's job responsibilities while avoiding stale permissions during transfers and controlling access promptly during offboarding.

## My implementation

In Microsoft Entra ID, I configured dynamic security group rules and group-based enterprise application assignment. I then validated three cases: a new Finance employee (Jonathan Jones), a Finance-to-Marketing transfer (Sarah Mitchell), and contractor offboarding (David Coleman).

## Outcomes demonstrated

**Joiner:** Jonathan's Finance / CFG / Employee attributes qualified him for the Finance group; he inherited the Finance Portal assignment. The included screenshots document Jonathan’s identity attributes, dynamic group membership, and inherited app assignment.

**Mover:** Sarah's changed department was reflected in dynamic group membership, and the inherited Finance Portal assignment disappeared. This helps reduce privilege creep from stale department-based assignments.

**Leaver:** David's account was disabled and his Entra sign-in sessions were revoked. Audit records showed the account-enabled flag changing and the refresh-token validity timestamp updating. David had no pre-existing app or group assignments in the captured baseline, so entitlement removal was not demonstrated.

## Controls and trade-offs

- Attribute-driven membership scales better than manually maintaining department memberships, but depends on correct identity data.
- Group-based app assignment avoids repetitive per-user app assignments.
- Sensitive exceptions should be managed separately from broad departmental groups.
- Session revocation is not the same as terminating all downstream application sessions.

## What I would extend in a production setting

Integrate a trusted HR source; establish approval and exception workflows; use supported application provisioning where available; test access and session behavior end-to-end; and measure offboarding completion against documented policy.

## Tools and skills

Microsoft Entra ID, dynamic security groups, enterprise applications, identity attributes, JML lifecycle management, least privilege, access verification, audit logs.
