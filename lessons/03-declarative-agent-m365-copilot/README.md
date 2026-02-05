# Lesson 03 – Deploy a Declarative Agent for Microsoft 365 Copilot

## Status

In progress.  
This lesson documents my understanding of declarative agents and the capabilities of Microsoft Copilot Studio before completing the hands-on lab.

---

## Overview

This lesson focuses on deploying a declarative agent that extends Microsoft 365 Copilot with custom instructions, tools, and enterprise knowledge. Declarative agents are embedded directly into Microsoft 365 Copilot and can also be published to Microsoft Teams.

The goal of this lesson is to understand what declarative agents are, why Microsoft Copilot Studio is used to build them, and how Copilot Studio full differs from Copilot Studio lite.

---

## What Is a Declarative Agent

A declarative agent is a customized extension of Microsoft 365 Copilot designed to support a specific business process or use case.

Unlike general-purpose Copilot experiences, a declarative agent:

- Operates with a defined set of instructions that shape its behavior
- Can be grounded in enterprise data such as SharePoint or Dataverse
- Can invoke tools and connectors to perform actions
- Extends Microsoft 365 Copilot without requiring custom application development

Declarative agents allow organizations to tailor Copilot behavior to internal workflows and domain-specific requirements.

---

## Why Use Microsoft Copilot Studio for Declarative Agents

Declarative agents can be created using two different experiences:

- Copilot Studio lite (Agent Builder in Microsoft 365 Copilot)
- Copilot Studio full

While Copilot Studio lite allows quick customization, Copilot Studio full provides significantly more control, extensibility, and deployment options.

Microsoft Copilot Studio is used when declarative agents require:

- Advanced enterprise knowledge grounding
- Integration with external systems
- More sophisticated tooling and orchestration
- Broader deployment and permission management

---

## Copilot Studio Lite vs Copilot Studio Full

The following summarizes the key differences relevant to declarative agents.

### Knowledge Sources

Copilot Studio lite supports:
- Web content
- SharePoint
- Microsoft Teams chats
- Outlook emails
- Copilot connectors

Copilot Studio full supports:
- Web search via Bing
- SharePoint
- Dataverse
- Dynamics 365
- Copilot connectors

---

### Tools and Extensibility

Copilot Studio lite provides:
- Code interpreter
- Image generation

Copilot Studio full provides:
- Over 1400 Power Platform connectors
- Custom connectors
- Prompt-based tools
- REST API integration
- Model Context Protocol servers
- Computer use capabilities

---

### Publishing and Permissions

Copilot Studio lite:
- Publishes only to Microsoft 365 Copilot
- Users have viewer-only access

Copilot Studio full:
- Publishes to Microsoft 365 Copilot and Microsoft Teams
- Supports editor and viewer roles
- Enables shared ownership to reduce dependency on a single owner

---

## Capabilities of Declarative Agents in Copilot Studio

Declarative agents built using Copilot Studio full enable deeper customization across multiple dimensions.

### Instructions and Behavior

- Detailed instructions define agent role, scope, and tone
- Instructions can reference tools and capabilities using natural language
- Behavior can be constrained to specific rules or policies

---

### Enterprise Knowledge Access

Declarative agents can access enterprise data while respecting user permissions, including:

- SharePoint content
- Dataverse tables
- Dynamics 365 records
- Microsoft 365 Copilot connectors enabled by administrators

This enables responses that are grounded in authoritative internal sources.

---

### Advanced Tooling

Declarative agents can integrate with external services using:

- Power Platform connectors (e.g., ServiceNow, Salesforce, SAP)
- Custom connectors
- REST APIs
- Model Context Protocol servers

Agents can also use AI prompts as tools to analyze or transform text, documents, images, or structured data.

---

### Model Selection

AI prompts used as tools support:

- Multiple chat model tiers (Basic, Standard, Premium)
- Bring-your-own models via Microsoft Foundry
- Model grounding to control reasoning and output quality

---

### Deployment Options

Declarative agents built in Copilot Studio can be:

- Published to Microsoft 365 Copilot
- Published to Microsoft Teams for higher user adoption
- Shared with configurable user permissions

---

## Business-to-Employee (B2E) Use Case

This lesson introduces a Business-to-Employee (B2E) scenario as the primary use case.

B2E refers to services and interactions provided by an organization directly to its employees. In the context of declarative agents, B2E scenarios often include:

- IT helpdesk support
- HR policy assistance
- Internal service requests
- Employee onboarding guidance

Declarative agents are well-suited for B2E scenarios because they combine enterprise knowledge, automation, and in-context user experiences.

---

