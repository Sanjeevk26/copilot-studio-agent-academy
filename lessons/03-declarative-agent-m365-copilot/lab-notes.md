# Lesson 03 – Deploy a Declarative Agent for Microsoft 365 Copilot

## Overview

This document records the complete implementation of Lesson 03, covering conceptual understanding, hands-on lab execution, validation, and issue resolution while building a declarative agent using Microsoft Copilot Studio.

The agent created extends Microsoft 365 Copilot with custom instructions and prompt-based tooling and is published to both Microsoft 365 Copilot and Microsoft Teams.

---

## Objectives

- Understand what declarative agents are and how they extend Microsoft 365 Copilot
- Compare Copilot Studio Lite and Copilot Studio Full for declarative agent creation
- Create a declarative agent using the conversational creation experience
- Add an AI prompt as a tool and invoke it via instructions
- Publish and test the agent in Microsoft 365 Copilot and Microsoft Teams
- Validate agent execution using developer mode
- Identify and resolve deployment and permission issues

---

## Declarative Agents in Microsoft 365 Copilot

Declarative agents are tailored extensions of Microsoft 365 Copilot designed to support specific business processes. They operate based on defined instructions, enterprise knowledge access, and tools that enable extended capabilities beyond generic Copilot interactions.

Declarative agents allow organizations to create customized, governed AI experiences aligned with internal workflows.

---

## Copilot Studio Lite vs Copilot Studio Full

Copilot Studio Lite (Agent Builder in Microsoft 365 Copilot) enables rapid creation of simple, conversational declarative agents using Microsoft 365 data with minimal setup.

Copilot Studio Full provides advanced extensibility and control, including enterprise knowledge integration, workflow automation, external system connectivity, and deployment to Microsoft Teams.

Copilot Studio Full is used when agents require automation, external integrations, governance, or shared ownership.

---

## Business-to-Employee (B2E) Use Case

The lab implements a Business-to-Employee IT Helpdesk agent to assist employees with device, network, and system issues.

The agent is designed to:
- Answer IT-related questions
- Provide step-by-step troubleshooting guidance
- Maintain a professional, empathetic tone
- Be accessible from Microsoft 365 Copilot and Microsoft Teams

---

## Prerequisites

- Access to a Copilot Studio environment
- Permissions to create and publish agents
- Microsoft Teams enabled in the tenant
- Microsoft 365 Copilot license for testing agent usage

---

## Step-by-Step Implementation

### 1. Create a Declarative Agent

- Navigated to https://copilotstudio.microsoft.com
- Selected the appropriate environment
- Selected Agents
- Chose Copilot for Microsoft 365
- Selected Add agent

This launched the conversational creation experience.

---

### 2. Define Initial Agent Instructions

Entered the following description to define the agent role and behavior:

You are a highly skilled and experienced IT professional specializing in a wide range of computer systems, networking, and cybersecurity. You are able to diagnose and solve technical issues, explain solutions in a clear and understandable manner for users of all technical levels, and provide guidance on best practices. You should be concise and informative, using step-by-step instructions with bullet points when appropriate. Your goal is to help the user understand the problem and how to resolve it effectively.

Accepted the suggested agent name and later renamed it to:

Contoso Tech Support Pro

---

### 3. Refine Agent Instructions

Updated instructions to enforce:

- Concise responses
- Bullet-point formatting
- Empathetic tone
- Feedback request after solutions

Concise and Informative:
- Use bullet points for clarity
- Provide a brief summary

User-Friendly Communication:
- Show empathy
- Encourage users

Interactive:
- Ask for feedback after providing a solution

---

### 4. Test Base Agent Behavior

- Used starter prompts in the test pane
- Verified adherence to formatting, tone, and feedback guidance

---

### 5. Create an AI Prompt Tool

- Navigated to Tools
- Selected Add tool
- Chose New tool
- Selected Prompt
- Named the prompt:

IT Expert

---

### 6. Configure the Prompt

Manually entered the following prompt instructions:

I want you to act as an IT Expert. I will provide you with all the information needed about my technical problems, and your role is to solve my problem. You should use your computer science, network infrastructure, and IT security knowledge to solve my problem. Using intelligent, simple, and understandable language for people of all levels in your answers will be helpful. It is helpful to explain your solutions step by step and with bullet points. Try to avoid too many technical details, but use them when necessary. I want you to reply with the solution, not write any explanations. My problem is [Problem]

Configured input parameter:
- Name: problem input
- Sample value: My laptop gets an error with a blue screen

Tested and saved the prompt, then added it to the agent.

---

### 7. Invoke the Prompt via Agent Instructions

Updated agent instructions:

- When a user asks questions about their device, run the "IT Expert" prompt.
- Use the user's question as the problem input for the prompt.

Saved changes.

---

### 8. Test Prompt Invocation

Tested with the query:

Can you help me, my laptop is encountering a blue screen

Verified the prompt was invoked and the response followed the defined structure.

---

### 9. Publish the Agent

- Selected Publish
- Enabled channels:
  - Microsoft 365 Copilot
  - Microsoft Teams
- Updated publishing metadata
- Completed publishing

---

### 10. Validate in Microsoft 365 Copilot

- Opened the agent via shared link
- Added the agent
- Tested using starter prompts
- Granted permission for prompt invocation

---

### 11. Debug Using Developer Mode

Enabled developer mode:

-developer on

Reviewed Agent Debug Info to confirm:
- Prompt selection
- Prompt execution

Disabled developer mode:

-developer off

---

### 12. Validate in Microsoft Teams

- Located the agent under Apps
- Pinned the agent
- Tested the same IT issue scenario
- Verified consistent behavior

---

## Issue Encountered: Permission Error in Microsoft Teams

### Error Message

Permissions needed.
Ask your IT admin to add agent to this team/chat/meeting.

---

## Resolution

The issue was caused by a Microsoft Teams app policy restriction.

### Fix Applied

In the Microsoft Teams Admin Center:
- Navigated to Apps
- Selected App setup policies
- Edited the relevant policy
- Enabled Upload custom apps

After enabling this setting, the agent became accessible in Microsoft Teams and Microsoft 365 Copilot without errors.

---

## Key Learnings

- Declarative agents can be created end-to-end using natural language
- Prompts act as tools and must be explicitly invoked via instructions
- Developer mode is essential for validating agent orchestration
- Publishing to Teams depends on tenant-level app setup policies
- App setup policies can block access even when publishing succeeds

---


Creating a Solution for Your Agent
