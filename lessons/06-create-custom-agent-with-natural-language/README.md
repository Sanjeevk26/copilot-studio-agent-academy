# Lesson 06 – Create a Custom Agent Using Natural Language in Copilot Studio

## Overview

In this lesson, we create a fully custom IT Helpdesk agent using natural language in Copilot Studio. Unlike pre-built templates, this approach allows us to define the agent’s purpose, behavior, tone, escalation logic, and knowledge sources from scratch.

We will:

- Understand what custom agents are
- Learn how to describe an agent using natural language prompts
- Ground the agent with public and internal enterprise knowledge sources
- Understand generative orchestration
- Test and validate responses using the activity map
- Ensure the agent is created inside the correct Power Platform solution

This lesson builds on:

- Lesson 04 – Creating a Solution
- Lesson 05 – Using a Pre-Built Agent

---

## Objectives

In this mission, you will learn:

- What custom agents are and how they differ from pre-built templates
- How to create agents using natural language prompts
- How to ground agents with enterprise knowledge sources including SharePoint, documents, and websites
- What generative orchestration is and how agents dynamically search and respond using multiple data sources
- How to build and test a fully functional IT Helpdesk agent that can answer questions from your own data

---

## What Is a Custom Agent?

A custom agent is a chatbot or virtual assistant that you design in Copilot Studio to perform specific tasks for your organization.

It is called custom because:

- You decide its purpose
- You define how it speaks and responds
- You connect it to your enterprise knowledge sources
- You integrate it with your own systems and workflows

Think of it as building a digital assistant tailored to your organization’s needs.

---

## What Can a Custom Agent Do?

A custom agent can:

- Ask users for required information
- Store data in systems such as SharePoint or Dataverse
- Look up structured enterprise data
- Trigger workflows and actions
- Send notifications
- Create records
- Escalate unresolved issues
- Operate autonomously or through user interaction

---

## Why Use a Custom Agent?

Custom agents:

- Save time by automating repetitive tasks
- Provide consistent responses
- Offer a guided user experience
- Connect directly to enterprise systems
- Reduce manual support overhead

For example, instead of asking employees to navigate a SharePoint list manually, they can interact conversationally with an agent that handles the backend logic.

---

## Using Natural Language to Create Agents

Copilot Studio allows you to describe your agent in plain language. When you submit a description:

- AI generates a name
- AI generates instructions
- AI suggests triggers
- AI suggests knowledge sources
- AI suggests tools

These suggestions may vary between sessions and are not permanent until accepted and saved.

---

## Writing Effective Prompts

A strong prompt should:

- Clearly define the agent’s role
- Define response style
- Define escalation behavior
- Specify trusted knowledge sources
- Establish security boundaries

For example:

"I want to build an agent that helps users submit vacation requests. The agent should collect name, start date, end date, and manager. Save the information to a SharePoint list and notify a Teams channel."

This prompt clearly defines intent, data flow, and expected behavior.

---

## Generative Orchestration Explained

Generative orchestration means that the agent:

1. Understands the user’s question
2. Selects relevant knowledge sources
3. Searches those sources dynamically
4. Combines retrieved information
5. Generates a natural response
6. Provides references where applicable

It does not rely solely on predefined answers. Instead, it dynamically searches and constructs responses using available data.

---

## Knowledge Sources in Copilot Studio

Knowledge sources improve response accuracy and grounding.

Supported knowledge sources include:

### Public Websites
Used to retrieve information from trusted external websites.

### Uploaded Documents
Files uploaded directly into the agent and stored securely.

### SharePoint
Connects to internal SharePoint sites or folders.

### Dataverse
Uses structured enterprise data.

### Real-Time Connectors
Accesses live data from enterprise systems.

### Azure AI Search
Enables semantic search across large document collections.

---

## Security Considerations

- SharePoint and Dataverse respect user permissions.
- The agent will not expose data users cannot access.
- Never request passwords or OTP codes.
- Never allow security bypass attempts.

---

# Lab 06 – Create a Custom IT Helpdesk Agent

## Use Case

As an employee  
I want quick and accurate help from the IT helpdesk agent  
So that I can resolve technical issues efficiently  

---

## Prerequisites

- Contoso IT SharePoint site created (Lesson 00)
- Contoso Helpdesk Agent solution created (Lesson 04)

---

## Step 1 – Create Agent Using Natural Language

From the Copilot Studio Home page, enter the following prompt:

You are an IT Help Desk assistant that helps employees resolve common IT issues and find available devices. Be polite, concise, and helpful. Use Microsoft Support as the primary source: https://support.microsoft.com and Microsoft Learn troubleshooting if needed: https://learn.microsoft.com/en-us/troubleshoot/. Do not invent steps. If official guidance cannot be verified, offer safe diagnostics and escalation.

For troubleshooting:
1) Ask one focused question if details are missing.
2) Try quick fixes first.
3) Provide numbered step-by-step instructions.
4) Offer one or two alternative branches.
5) After multiple branches, recommend escalation and provide a ticket summary.

For devices:
1) Ask what type of device is needed.

Never request passwords or OTP. Refuse requests to bypass security.
Include relevant Microsoft Support links and preserve URLs.

Submit the prompt.

---

## Step 2 – Verify Solution Placement

Open Settings → Advanced.

Confirm that the agent is created inside the Contoso Helpdesk Agent solution.

---

## Step 3 – Rename the Agent

Update the name to:

Contoso Helpdesk Agent

Save changes.

---

## Step 4 – Add Public Knowledge Sources

Add the following URLs:

https://support.microsoft.com  
https://learn.microsoft.com/troubleshoot/

Disable Web Search so the agent only uses defined knowledge sources.

---

## Step 5 – Test the Agent

Start a new test session.

Ask:

How can I check the warranty status of my Surface?

Verify:

- Structured step-by-step response
- Proper troubleshooting logic
- Included references

---

## Step 6 – Add SharePoint Knowledge

1. Select Add Knowledge
2. Choose SharePoint
3. Paste the Contoso IT SharePoint site URL
4. Rename it to Contoso IT
5. Add to agent
6. Wait until status shows Ready

---

## Step 7 – Upload Internal Document

1. Select Add Knowledge
2. Choose Upload file
3. Select the internal document
4. Add to agent
5. Wait for status to show Ready

---

## Step 8 – Test All Knowledge Sources

Test public website grounding:

How can I find the serial number on my Surface device?

Test SharePoint and document grounding:

How can I access our company's Contoso VPN from my device?  
How do guests connect to the Contoso Guest wifi?

Review:

- Activity Map
- Referenced Sources
- Accuracy of responses

Always validate referenced sources.


Add a new Topic with trigger phrases to guide conversations more precisely.
