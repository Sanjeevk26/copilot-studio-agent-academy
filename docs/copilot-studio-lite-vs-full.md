# When to Use Copilot Studio Lite vs Copilot Studio Full

This section documents when to use Copilot Studio Lite (Agent Builder in Microsoft 365 Copilot) versus Copilot Studio Full, based on scope, complexity, and enterprise requirements.

Both options create declarative agents that extend Microsoft 365 Copilot, but they are intended for different levels of customization and control.

---

## Copilot Studio Lite (Agent Builder in Microsoft 365 Copilot)

### What It Is

Copilot Studio Lite is the in-product agent builder experience available directly inside Microsoft 365 Copilot. It is designed for quick customization using natural language without requiring access to the full Copilot Studio environment.

It prioritizes speed and simplicity over extensibility.

---

### When to Use Copilot Studio Lite

Use Copilot Studio Lite when:

- You need a lightweight, personal or team-level agent
- The agent only needs Microsoft 365 data (SharePoint, Outlook, Teams)
- No external system integration is required
- The agent is read-oriented rather than action-heavy
- Publishing only to Microsoft 365 Copilot is sufficient
- You want minimal setup and governance overhead

---

### Example Scenarios for Copilot Studio Lite

#### Example 1: Personal Productivity Assistant

A knowledge worker creates an agent to help with daily tasks such as:

- Summarizing recent emails
- Answering questions from personal OneDrive files
- Finding information in Teams chats

No automation, external systems, or shared ownership is required.

---

#### Example 2: Team Knowledge Helper

A small team creates an agent that:

- Answers questions from a single SharePoint site
- Helps locate documents
- Summarizes meeting notes from Teams chats

The agent is used informally by the team and does not perform actions such as ticket creation or record updates.

---

### Limitations of Copilot Studio Lite

- Limited knowledge sources (primarily Microsoft 365 data)
- No access to Power Platform connectors
- No REST API or external system integration
- Limited permission and ownership controls
- Cannot be published to Microsoft Teams
- Not suitable for enterprise automation scenarios

---

## Copilot Studio Full

### What It Is

Copilot Studio Full is the standalone, low-code platform for building production-grade declarative agents. It provides advanced orchestration, tooling, enterprise integration, and deployment options.

It is designed for shared, governed, and extensible agents.

---

### When to Use Copilot Studio Full

Use Copilot Studio Full when:

- The agent supports a business process or operational workflow
- Enterprise knowledge beyond basic Microsoft 365 context is required
- The agent must perform actions (not just answer questions)
- Integration with external systems is required
- Multiple owners or editors are needed
- The agent must be deployed to Microsoft Teams
- Governance, security, and scalability matter

---

### Example Scenarios for Copilot Studio Full

#### Example 1: IT Helpdesk Agent (B2E)

An internal IT agent that:

- Retrieves troubleshooting steps from SharePoint
- Creates tickets in ServiceNow via a connector
- Updates a SharePoint or Dataverse ticket log
- Notifies IT staff in Microsoft Teams
- Is shared and maintained by multiple administrators

This scenario requires tools, workflows, enterprise knowledge, and shared ownership.

---

#### Example 2: HR Policy and Benefits Agent

An HR agent that:

- Answers policy questions using SharePoint and Dataverse
- Enforces response rules (e.g., no legal advice)
- Submits leave requests through Power Automate
- Sends confirmation emails and Teams messages
- Is published to Microsoft Teams for employee access

This goes beyond simple retrieval and requires orchestration and governance.

---

#### Example 3: Finance or Operations Agent

An agent that:

- Pulls data from Dynamics 365 or SAP
- Performs calculations or summarization using AI prompts
- Writes results back to Dataverse
- Triggers approval workflows
- Is restricted by role-based access

This requires advanced connectors, actions, and permission control.

---

## Decision Summary

| Requirement | Copilot Studio Lite | Copilot Studio Full |
|------------|-------------------|---------------------|
| Quick, personal customization | Yes | Yes |
| Enterprise-grade automation | No | Yes |
| External system integration | No | Yes |
| Power Platform connectors | No | Yes |
| REST API / custom connectors | No | Yes |
| Microsoft Teams deployment | No | Yes |
| Multiple editors | No | Yes |
| Governance and scalability | Limited | Full |

---

## Practical Rule of Thumb

- Use **Copilot Studio Lite** when the agent is:
  - Simple
  - Informational
  - Personal or small-team focused

- Use **Copilot Studio Full** when the agent is:
  - Operational
  - Action-oriented
  - Integrated with enterprise systems
  - Shared across users or departments

If an agent starts in Copilot Studio Lite and later requires automation, integrations, or governance, it is a strong signal that it should be rebuilt or extended using Copilot Studio Full.

---

## Notes

Both tools create declarative agents, but they serve different stages of maturity. Copilot Studio Lite is optimized for speed and experimentation, while Copilot Studio Full is optimized for production and scale.
