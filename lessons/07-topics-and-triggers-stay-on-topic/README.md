# README.md

# Lesson 07 – Topics and Triggers (Stay on Topic)

## Overview

This lesson explains how Topics and Triggers help a Copilot Studio agent respond with precision. While a generative agent can answer broadly using instructions and knowledge sources, Topics allow you to build structured conversation flows for specific intents such as informational questions, task completion, and troubleshooting.

With Topics and Triggers, the agent can:

- Recognize user intent
- Route conversations with logic
- Gather and store variables
- Trigger tools and connectors
- Perform actions based on user input

This lesson focuses on both the conceptual structure of topics and the practical implementation of a custom topic that connects to SharePoint data.

---

## Objectives

In this mission, you will learn:

- What topics are and how they create structured conversations
- The anatomy of a topic: trigger phrases and conversation nodes
- The most common node types and when to use them
- How to use Power Fx for dynamic logic in topics
- How to create a custom topic from scratch
- How to connect a topic to SharePoint data using a connector tool
- How to test and validate topic execution

---

## What Is a Topic?

A topic is a structured conversation flow that helps your agent handle a specific user request. Each topic is designed to respond to an identifiable intent and then guide the user through a controlled set of steps.

A topic can be thought of as a mini-workflow inside your agent.

---

## Purpose of Topics

Topics are usually designed for one of these purposes:

### Informational
Used when users want information.

Examples:
- What is …?
- When will …?
- Why …?
- Can you tell me …?

### Task Completion
Used when users want the agent to perform an action.

Examples:
- I want to …
- How do I …?
- I need to …

### Troubleshooting
Used when users want help resolving issues.

Examples:
- Something isn’t working …
- I’m seeing an error message …
- This is unexpected …

Topics can also handle ambiguous queries such as “I need help,” by asking clarifying questions first.

---

## Why Topics Are Useful

Topics help you:

- Organize your agent’s behaviors
- Provide consistent and repeatable user experiences
- Reduce ambiguity in responses
- Add logic and branching to conversations
- Connect tools to specific scenarios cleanly

---

## Types of Topics

### System Topics
Built-in topics that handle common events such as:

- Starting a conversation
- Ending a conversation
- Error handling
- Authentication prompts
- Escalation to a human agent

### Custom Topics
Topics you build to handle business-specific tasks, such as:

- Device requests
- Leave requests
- Policy lookup
- Troubleshooting flows

---

## Anatomy of a Topic

A topic typically consists of:

### Trigger Phrases
What users might say to start the topic.

Examples:
- “I need a new device”
- “Show me available laptops”
- “Can I request a device?”

### Conversation Nodes
The steps the agent follows after the trigger.

Nodes represent actions such as:

- Sending a message
- Asking a question
- Setting variables
- Branching using conditions
- Running tools (connectors, flows, prompts)
- Redirecting to other topics
- Using generative answers within the flow

---

## Node Types (Conceptual Summary)

### Send a message
Used when the agent needs to communicate information.

### Ask a question
Used to collect user input and store it into variables.

### Ask with adaptive card
Used when a structured form-like UI is needed.

### Add a condition
Used for if/else branching logic.

### Variable management
Used to store, clear, or transform values.

### Topic management
Used to redirect, end, or transfer conversations.

### Add a tool
Used to run connectors, flows, prompts, APIs, MCP servers, or other tools.

### Generative answers node
Used for dynamic AI responses grounded in knowledge sources.

### HTTP request node
Used to call REST APIs and store responses.

### Send an event
Used for non-message actions sent to the client or channel.

---

## Power Fx in Topics

Power Fx is an Excel-like low-code language used to add logic inside topics.

Common uses:

- Format and transform values
- Build dynamic filter queries
- Create branching logic
- Set variable values using computed expressions

Examples:
- If(score > 80, "Pass", "Fail")
- Text(DateValue, "dd/mm/yyyy")

---

## Designing Topics (Practical Method)

A reliable method to design topics:

1. Identify user needs (questions, tasks, issues)
2. Group scenarios (informational, task, troubleshooting)
3. Map the conversation flow (short, focused)
4. Handle single-turn and multi-turn paths
5. Use AI for unexpected questions (generative answers and conversational boosting)
6. Test using realistic prompts and iterate
7. Avoid duplicating content already available on websites; prioritize frequent user needs

---

## What This Lesson Implements (Lab Summary)

The lab creates a custom topic called:

Available devices

It enables employees to ask for available devices by type (Laptop, Desktop, Smartphone) and retrieves matching results from a SharePoint list using the SharePoint connector and a Power Fx filter query.

It also updates agent instructions so the agent can invoke the topic when users ask about devices.

Proceed to the lab file to implement the topic.
