# Identity and Access Management (IAM)

## Overview

Identity and access management covers how user accounts are created, proven, and shared across systems, and how access to resources is controlled. These topics often appear together on the exam, so it helps to see how they connect.

## Access Control Models

Access control models fall into two major groups: discretionary and rule-based.

| Model | Group | Who sets the rules |
|---|---|---|
| **Discretionary access control (DAC)** | Discretionary | The owner of the resource decides who can access it |
| **Mandatory access control (MAC)** | Rule-based | A central authority sets the rules, and users cannot change them |
| **Role-based access control (RBAC)** | Rule-based | Access is tied to the user's role in the organization |
| **Attribute-based access control (ABAC)** | Rule-based | A decision engine evaluates attributes of the request, such as user, resource, and context |

> **Analogy:** DAC is a homeowner deciding who gets a key to their house. MAC is a government building where clearance levels are set centrally. RBAC is an office where managers can see their team's files, but the engineering team cannot see marketing's. ABAC is a security desk that checks several details, such as your role, the time, and your location, before opening a door.

### Discretionary Access Control

Whenever you create a file on your own computer, you can decide who else can read or change it, including making it read only. The owner has the discretion.

### Role-Based Access Control

RBAC is a type of rule-based access control. The rules revolve around roles in the organization. A manager may see what their team has, while the team cannot see the manager's files. Engineering and marketing may not be able to see each other's resources.

### Attribute-Based Access Control

ABAC uses a decision engine that takes in attributes of the access request, such as the user's department, the time of day, the device used, and the sensitivity of the data, then decides whether access is allowed.

> [!IMPORTANT]
> **Exam clue:** Discretionary access is decided by the resource owner. Rule-based models are decided by a set policy. RBAC uses roles, while ABAC uses attributes.

## Account Creation and Identity Proofing

- **Separation of duties:** No single person should create user accounts alone. Requests should come from an authorised department, such as HR or the technology director
- **Identity proofing:** Proving that a person is who they claim to be before an account is issued

> **Analogy:** Opening a bank account requires two people to sign off, and you show ID before the account is activated.

## Federation

Federation lets one
