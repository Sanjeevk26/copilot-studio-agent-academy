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

