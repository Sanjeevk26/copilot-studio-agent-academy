# Lesson 02 – Copilot Studio Fundamentals

## Overview

This lesson documents my understanding of how Microsoft Copilot Studio works and how intelligent agents are structured within the platform. The focus is on understanding when to use Copilot Studio, what agents are, and the four core building blocks that every Copilot Studio agent is composed of: Knowledge, Tools, Topics, and Instructions.

Understanding these components is required before creating any custom agent.

---

## What Is Copilot Studio

Copilot Studio is a low-code platform used to build custom AI agents that can answer questions, retrieve information, and perform actions across enterprise systems.

Unlike general-purpose assistants, agents built in Copilot Studio are designed for specific business scenarios. They can be embedded into existing tools such as Microsoft Teams, Microsoft 365 Copilot, or external web applications.

Key characteristics of Copilot Studio include:

- Low-code, visual agent authoring  
- Native integration with Microsoft 365 and Power Platform  
- Support for conversational and event-driven scenarios  
- Built-in orchestration using large language models  

---

## What Are Agents in Copilot Studio

An agent is a specialized AI assistant created to perform defined tasks within a given scope.

Compared to a generic chatbot, a Copilot Studio agent:

- Uses organization-specific data such as policies, documents, and databases  
- Maintains conversational context across interactions  
- Can perform real-world actions such as sending messages, updating records, or triggering workflows  
- Operates within constraints and rules defined by the agent creator  

Agents are built by assembling predefined components rather than writing code from scratch.

---

## When and Why to Use Copilot Studio

While Microsoft 365 Copilot provides general AI assistance across Office applications, Copilot Studio is used when custom behavior or orchestration is required.

Common scenarios where a custom agent is appropriate include:

### Multiple Knowledge Sources

When answers must be grounded in data beyond default Microsoft 365 context, such as multiple SharePoint sites, internal documentation repositories, or external knowledge bases.

### Workflow Automation

When a user request requires multiple coordinated steps, such as collecting input, updating records, notifying stakeholders, or calling external systems.

### Embedded, Contextual Experiences

When guidance or automation must occur directly inside tools like Microsoft Teams rather than as a separate application.

---

## Core Building Blocks of an Agent

Every Copilot Studio agent is composed of four fundamental components:

1. Knowledge  
2. Tools (Actions)  
3. Topics  
4. Instructions  

These components are orchestrated together by the Copilot Studio AI runtime.

---

## Knowledge

Knowledge defines what information the agent can use to answer questions and maintain context.

### Custom Instructions and Context

Each agent includes a description of its purpose and behavior. This establishes:

- The role of the agent  
- The domain it operates in  
- How it should interpret and respond to user input  

The agent also maintains conversational context, allowing it to reference earlier parts of the conversation.

### Knowledge Sources (Grounding Data)

Agents can be connected to structured and unstructured data sources, such as:

- SharePoint document libraries  
- Internal documentation  
- Wikis  
- Databases  

When a question is asked, the agent retrieves relevant excerpts from these sources and grounds its response in that data. Agents can also be restricted to respond only using connected knowledge sources to prevent unsupported answers.

---

## Tools (Actions)

Tools, also referred to as actions, define what the agent can do beyond generating text.

Examples of actions include:

- Sending emails or Teams messages  
- Creating or updating calendar events  
- Writing to SharePoint lists or Dataverse tables  
- Triggering Power Automate flows  
- Calling REST APIs  

Actions are defined with inputs and outputs and can be chained together to form multi-step workflows.

---

## Topics

Topics define how an agent recognizes user intent and decides which conversational or action flow to execute.

Each topic includes a description of what it handles. Copilot Studio uses this description to match user intent even when phrasing varies.

Once a topic is selected, the agent follows the defined steps, which may include asking questions, retrieving knowledge, calling actions, and returning results.

---

## Instructions

Instructions define the global rules that govern agent behavior.

They typically specify:

- Role and persona  
- Tone and response style  
- Formatting or length constraints  
- Rules for unknown or restricted information  
- Memory and context boundaries  

Instructions apply consistently across all topics and actions.

---

## End-to-End Example: Service Desk Agent Using All Four Components

This example illustrates how Knowledge, Tools, Topics, and Instructions work together in a single agent.

### Scenario

A Service Desk agent in Microsoft Teams helps employees submit IT support tickets.

### Knowledge

- Connected to a SharePoint site containing:
  - IT policies
  - Common troubleshooting guides
  - Support escalation procedures
- The agent is instructed to answer questions only using this data.

### Topic

- Topic name: `Submit IT Ticket`
- Topic description:
  - Handles requests related to reporting technical issues and submitting support tickets.
- The agent matches this topic when a user says:
  - “My laptop is not connecting to Wi-Fi”
  - “I need help with my new device”

### Tools (Actions)

- Action 1: Create item in SharePoint List  
  - Inputs: Issue description, priority, user name  
- Action 2: Send Teams message  
  - Notifies the IT support channel with ticket details  

### Instructions

- Agent role: Internal IT support assistant  
- Tone: Professional and concise  
- Rules:
  - Ask clarifying questions if issue details are incomplete  
  - Confirm ticket creation before ending the conversation  
  - Do not provide troubleshooting steps beyond documented policies  

### How the Flow Executes

1. User describes an issue in Teams  
2. Agent matches the request to the `Submit IT Ticket` topic  
3. Instructions guide the agent to collect required details  
4. Knowledge is used to validate issue category and priority  
5. Tools are executed to create the ticket and notify IT  
6. Agent confirms successful submission to the user  

This example demonstrates how all four components are required to move from understanding intent to executing a real business process.

---

## How the Components Work Together

At runtime, Copilot Studio orchestrates the components as follows:

1. User input is matched to the most relevant topic  
2. Instructions determine tone, rules, and response behavior  
3. Knowledge sources are queried to ground responses  
4. Tools are executed to perform actions when required  
5. The agent responds using retrieved data and action results  

This orchestration is dynamic and adapts to conversation context and execution outcomes.

---

## Summary

From this lesson, the following understanding is established:

- Copilot Studio enables custom, task-focused AI agents  
- Agents are composed of Knowledge, Tools, Topics, and Instructions  
- Knowledge provides grounding and context  
- Tools enable execution  
- Topics drive intent recognition and flow selection  
- Instructions enforce consistency and boundaries  
- The orchestrator coordinates all components at runtime  

These fundamentals are required before building any functional agent.

---

## Next Steps

The next lesson focuses on creating a declarative agent for Microsoft 365 Copilot, including defining instructions and grounding the agent in knowledge sources.
