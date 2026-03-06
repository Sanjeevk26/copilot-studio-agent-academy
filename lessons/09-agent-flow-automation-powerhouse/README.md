Folder name:
lessons/09-agent-flow-automation-powerhouse

File name:
lessons/09-agent-flow-automation-powerhouse/README.md

# Lesson 09 – Add an Agent Flow to Your Topic for Automation

## Overview

In this lesson, we move from conversational responses to real automation by introducing agent flows in Copilot Studio. While the agent can already answer questions, retrieve knowledge, and guide users through structured topics, agent flows allow it to perform actions in connected systems in a reliable and repeatable way.

This lesson focuses on the purpose of agent flows, how they differ from Power Automate cloud flows, what makes them powerful, and how they support end-to-end automation scenarios such as device request handling.

By the end of this lesson, the agent is no longer limited to conversation. It becomes capable of executing business actions such as retrieving records, sending notifications, and supporting approvals through workflow automation.

---

## Objectives

In this mission, you will learn:

- What agent flows are and how they differ from Power Automate cloud flows
- The features that make agent flows powerful, including AI actions and natural language authoring
- How the agent flow designer works
- How expressions are used for dynamic data handling
- How agent flows support end-to-end automation scenarios in Copilot Studio

---

## What Is an Agent Flow?

An agent flow is a structured workflow that an agent can execute to automate tasks and connect with systems or services.

Agent flows are deterministic, which means they follow the same defined path each time for the same inputs. This makes them predictable and reliable for business processes.

In simple terms:

- Agents decide and converse
- Agent flows execute and automate

Agent flows help the agent do things, not just say things. They can send notifications, retrieve records, update systems, and perform other business actions as part of the conversation experience.

---

## Agent Flows vs Power Automate Cloud Flows

Although both are used for automation, they are designed for different purposes.

### Agent Flows in Copilot Studio

Used for:

- Automation inside agents
- Task execution triggered by user conversations
- AI-assisted workflow creation directly inside Copilot Studio

Advantages:

- Built directly in Copilot Studio
- Suitable for conversational scenarios
- No separate Power Automate license required for use within Copilot Studio usage model
- Closely tied to agent logic and topics

Limitations:

- Cannot be shared, copied, or co-owned like traditional cloud flows
- Visible and usable only within Copilot Studio
- Some event-trigger management may still require the Power Automate maker portal

### Power Automate Cloud Flows

Used for:

- General-purpose automation across apps and services
- Workflows outside agent experiences
- Team-wide reusable automation

Advantages:

- Large connector ecosystem
- Shareable and manageable across teams
- Useful beyond Copilot Studio

Requirements:

- Requires Power Automate licensing

### Summary

Use agent flows when you want to automate actions inside an agent conversation and keep the logic within Copilot Studio.

Use Power Automate cloud flows when you want broader workflow automation across systems outside the agent experience.

---

## Why Use Agent Flows?

Agent flows are valuable because they are:

### Reliable
They behave the same way every time for the same conditions.

### Predictable
You know exactly what sequence of actions will run.

### Rule-based
They follow the logic you configure.

Additional benefits include:

- Automation of repetitive processes
- Integration with business systems
- Tight connection to agent conversations
- Reusability across scenarios
- No-code and low-code authoring options
- Centralized design, testing, and deployment in Copilot Studio

---

## How Agent Flows Enhance an Agent

Agent flows allow an agent to move from information delivery to action execution.

For example, instead of only telling a user how to request a device, the agent can:

- Capture request details
- Retrieve data from SharePoint
- Notify the manager by email
- Confirm the request back to the user

This makes the agent operational, not just conversational.

A useful way to think about it is:

- Agents are the smart decision-makers
- Agent flows are the reliable executors

---

## Key Features of Agent Flows

### Natural Language Authoring

You can describe what the flow should do in plain language, and Copilot helps generate the structure.

This lowers the barrier to building automations and speeds up development.

### AI Actions

Agent flows can use AI-driven capabilities such as:

- Reading and extracting information from documents
- Summarizing content
- Making recommendations

### Generative Actions

These allow more flexible handling of changing situations and inputs.

### Integration Actions

Agent flows can connect to systems such as:

- Outlook
- Microsoft Teams
- SharePoint
- Salesforce
- ServiceNow
- Other applications through built-in or custom connectors

### Human in the Loop

Flows can include approvals or review steps when human confirmation is required.

---

## How Agent Flows Work

An agent flow generally has two main parts:

### Trigger

The event that starts the flow.

Examples:

- A user invoking the flow from a topic
- A scheduled event
- A system event
- An automation trigger inside the agent

### Actions

The steps performed after the trigger.

Examples:

- Send an email
- Retrieve SharePoint items
- Create or update records
- Call an API
- Route for approval

---

## How to Create an Agent Flow

There are two common approaches:

### Natural Language

Describe the flow in plain language and let Copilot create the initial structure.

### Designer Canvas

Use the visual flow designer to add, configure, and connect actions manually.

---

## What Is the Agent Flow Designer?

The agent flow designer is the visual interface in Copilot Studio used to build and manage flows.

It provides:

### Visual Canvas
A diagram-like view of the flow structure.

### Add and Remove Actions
You can insert actions using the plus button and remove actions through the menu.

### Parameter Configuration
Each action can be configured using static values, dynamic content, or expressions.

### Version History
Every save creates a version that can later be reviewed or restored.

### Flow Checker
Used to detect errors before publishing.

### Publish and Test
Once valid, the flow can be published and tested.

---

## Expressions in Agent Flows

Expressions are formulas used to manipulate and evaluate data inside a flow.

They help with:

- Formatting values
- Combining fields
- Making decisions
- Handling null or fallback values
- Counting items
- Generating timestamps and identifiers

Functions in agent flows are similar to Excel functions. Instead of referencing worksheet cells, they work with outputs from triggers and actions.

---

## Commonly Used Functions

### Text Functions

- `concat()` joins text values
- `toLower()` converts text to lowercase
- `toUpper()` converts text to uppercase
- `substring()` extracts part of a string
- `trim()` removes extra spaces

### Math Functions

- `add()`
- `sub()`
- `mul()`
- `div()`

### Date and Time Functions

- `utcNow()`
- `addDays()`
- `addHours()`
- `formatDateTime()`

### Logical Functions

- `if()`
- `equals()`
- `and()`
- `or()`
- `not()`

### Utility Functions

- `coalesce()`
- `guid()`
- `length()`

These functions make flows smarter, more flexible, and more dynamic.

---

## Best Practices

When building agent flows:

### Start Simple
Begin with a small automation and extend it gradually.

### Use Clear Action Names
Rename actions so their purpose is obvious.

Example:
Instead of `Update item`, use `Update device status`.

### Check Errors Early
Use Flow Checker regularly.

### Test Thoroughly
A published flow is not necessarily a correct flow. Validate expected outcomes.

### Use Version History
Save often so you can restore earlier versions if needed.

### Use Parameters and Expressions Carefully
Prefer dynamic behavior where useful, but keep formulas readable and maintainable.

### Delete Unused Actions
Remove experimental or unnecessary actions to keep the flow clean.

---

## Example Scenario for This Lesson

In the device request process, an agent flow can be used to support an end-to-end automation such as:

1. Capture the selected device from the adaptive card
2. Retrieve device details from SharePoint
3. Send a notification email to the appropriate manager
4. Confirm the request submission to the employee

This turns the topic into a complete business process instead of only a conversational experience.

---

## Key Takeaway

Agent flows are what turn a Copilot Studio agent into an automation-enabled assistant. They provide structure, predictability, and system connectivity so the agent can do meaningful work inside the conversation.

The combination of topics, adaptive cards, and agent flows makes it possible to create guided, interactive, and action-oriented business experiences.

---

## Next Step

The next practical implementation should focus on adding an actual agent flow to the device request topic so the request can be processed automatically after the user submits the adaptive card.
