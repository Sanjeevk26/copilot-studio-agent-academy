# Lab 04 – Practical Implementation  
## Creating a Publisher and Custom Solution in Copilot Studio

---

## Lab Objective

In this lab, we completed the hands-on implementation of:

- Creating a Solution Publisher  
- Creating a Custom Solution  
- Setting the Solution as Preferred  
- Preparing the environment for enterprise-grade ALM  

This solution will be used to build and manage the IT Helpdesk Agent in future lessons.

---

## Environment Preparation

### Step 1 – Switch to Developer Environment

Before creating the solution:

1. Open Copilot Studio  
2. Select the **Settings (Cog wheel)** in the upper right  
3. Switch from the Default environment to your **Dedicated Developer Environment**

Note: All development work should be done inside a dedicated developer environment — not the Default environment.

---

## 4.1 Create a Solution Publisher

### Step 2 – Open Solution Explorer

1. In Copilot Studio, select the **ellipsis (...)** from the left navigation  
2. Select **Solutions** under the Explore section  
3. Solution Explorer opens  
4. Select **+ New solution**

---

### Step 3 – Create a New Publisher

Inside the New Solution pane:

1. Select **+ New publisher**

Populate the fields as follows:

| Property | Value |
|----------|--------|
| Display name | Contoso Solutions |
| Name | ContosoSolutions |
| Description | Copilot Studio Agent Academy |
| Prefix | cts |
| Choice value prefix | Rounded to nearest thousand (example: 77000) |

Example:

If the default value is `77074`, change it to:

77000


Optional:
- Navigate to the Contact tab and provide contact details (not required for this lab).

2. Select **Save**

Publisher creation complete.

---

## 4.2 Create the Custom Solution

After saving the publisher, you return to the New Solution pane.

### Step 4 – Complete Solution Details

Populate the following:

| Field | Value |
|-------|--------|
| Display name | Contoso Helpdesk Agent |
| Name | ContosoHelpdeskAgent |
| Version | 1.0.0.0 (default) |

Select:

- Set as your preferred solution (checkbox)

Leave **More options** fields blank for this lab.

Select **Create**

---

## Step 5 – Validate Solution Creation

After creation:

- The solution appears in Solution Explorer
- It contains **0 components** (expected)
- It is marked as **Current preferred solution**

This ensures that any new agent created will automatically be added to this solution.

---

## Verification Checklist

Confirm the following:

- [ ] Developer environment selected  
- [ ] Publisher created with prefix `cts`  
- [ ] Choice value prefix rounded correctly  
- [ ] Solution named Contoso Helpdesk Agent  
- [ ] Version is 1.0.0.0  
- [ ] Preferred solution checkbox selected  
- [ ] Solution visible in Solution Explorer  

---

## Why This Matters (Practical Reflection)

By creating a dedicated solution:

- Agent components are isolated from the Default solution
- Deployment becomes structured and repeatable
- Future exports to Test / UAT / Production are simplified
- Naming conventions are controlled via publisher prefix
- ALM best practices are enforced from day one

---

## What Happens Next

When we create or move the IT Helpdesk Agent into this solution:

- All related components (prompts, flows, environment variables) will be packaged together
- The solution can later be exported as Managed
- The solution can be imported into Test or Production environments

---

## Lab Outcome

Publisher Created: Yes  
Custom Solution Created: Yes  
Preferred Solution Set: Yes  
Environment Prepared for ALM: Yes  

Mission Status: Complete

---


