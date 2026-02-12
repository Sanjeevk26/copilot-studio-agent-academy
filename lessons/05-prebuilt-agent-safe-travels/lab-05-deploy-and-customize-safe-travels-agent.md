# Lab 05 – Deploy and Customize the Safe Travels Agent

---

## Lab Objective

In this lab, we will:

1. Launch Copilot Studio  
2. Deploy the Safe Travels agent template  
3. Enable generative AI  
4. Add a public knowledge source  
5. Test the agent  
6. Publish the agent  

---

## Prerequisites

- Copilot Studio enabled in your tenant
- Access to your Developer Environment
- Appropriate permissions to create agents

If Copilot Studio is not visible, revisit your environment setup.

---

## 5.1 Launch Copilot Studio

1. Navigate to:  
   https://copilotstudio.microsoft.com  

2. Sign in using your Microsoft 365 work or school account  

3. Ensure you are in your **Developer Environment**

---

## 5.2 Choose the Safe Travels Template

1. From the homepage, select **+ Create an agent**
2. Scroll to **Start with an agent template**
3. Select **Safe Travels**
4. Review:
   - Description
   - Instructions
   - Sample knowledge
5. Click **Create**

A new Safe Travels agent is created in your environment.

---

## 5.3 Enable Generative AI

1. Open the agent settings
2. Locate **Generative AI**
3. Enable **Generative Answers**

This allows the agent to respond using instructions and knowledge sources.

---

## 5.4 Add a Public Knowledge Source

We will ground the agent using the European Union website.

1. Scroll to the **Knowledge** section
2. Select **Add knowledge**
3. Choose **Public websites**
4. Paste the following URL:

https://european-union.europa.eu/

5. Select **Add**
6. Select **Add to agent**

The agent can now retrieve information related to Europe travel.

---

## 5.5 Test the Agent

Click **Test** in the top-right corner.

Try the following prompts:

- “Do I need a visa to travel from the US to Amsterdam?”
- “How long does it take to get a US Passport?”
- “Where is the closest US embassy in Valencia, Spain?”

Observe:

- Accuracy of responses
- Helpfulness
- Activity Map (to verify grounding source)

Confirm responses are relevant and contextual.

---

## 5.6 Publish the Agent

1. Select **Publish**
2. Confirm in the dialog box
3. Optionally configure **Channels**
4. Add to Microsoft Teams if required

Agent is now live.

---

File structure:
lessons/05-prebuilt-agent-safe-travels/
├── README.md
└── lab-05-deploy-and-customize-safe-travels-agent.md
# lab-05-deploy-and-customize-safe-travels-agent.md

# Lab 05 – Deploy and Customize the Safe Travels Agent

---

## Lab Objective

In this lab, we will:

1. Launch Copilot Studio  
2. Deploy the Safe Travels agent template  
3. Enable generative AI  
4. Add a public knowledge source  
5. Test the agent  
6. Publish the agent  

---

## Prerequisites

- Copilot Studio enabled in your tenant
- Access to your Developer Environment
- Appropriate permissions to create and publish agents

If Copilot Studio is not visible, revisit your environment setup.

---

## 5.1 Launch Copilot Studio

1. Navigate to:  
   https://copilotstudio.microsoft.com  

2. Sign in using your Microsoft 365 work or school account  

3. Ensure you are in your **Developer Environment**

---

## 5.2 Choose the Safe Travels Template

1. From the homepage, select **+ Create an agent**
2. Scroll to **Start with an agent template**
3. Select **Safe Travels**
4. Review:
   - Description
   - Instructions
   - Sample knowledge
5. Click **Create**

A new Safe Travels agent is created in your environment.

---

## 5.3 Enable Generative AI

1. Open the agent settings
2. Locate **Generative AI**
3. Enable **Generative Answers**

This allows the agent to respond using instructions and connected knowledge sources.

---

## 5.4 Add a Public Knowledge Source

We will ground the agent using the European Union website.

1. Scroll to the **Knowledge** section
2. Select **Add knowledge**
3. Choose **Public websites**
4. Paste the following URL:

https://european-union.europa.eu/

5. Select **Add**
6. Select **Add to agent**

The agent can now retrieve information related to Europe travel.

---

## 5.5 Test the Agent

Click **Test** in the top-right corner.

Try the following prompts:

- “Do I need a visa to travel from the US to Amsterdam?”
- “How long does it take to get a US Passport?”
- “Where is the closest US embassy in Valencia, Spain?”

Observe:

- Accuracy of responses  
- Helpfulness  
- Activity Map (to verify where knowledge was retrieved from)  

Confirm responses are relevant and contextual.

---

## 5.6 Publish the Agent

1. Select **Publish**
2. Confirm in the dialog box
3. Optionally configure **Channels**
4. Add to Microsoft Teams if required

Agent is now live.

---

# Troubleshooting – If Publishing Fails

If you encounter publishing errors, missing permissions, or inability to add the agent to Teams, your administrator may need to perform the following actions.

---

## What Your Admin Needs to Do

### 1. Assign Copilot Studio License

In the **Microsoft 365 Admin Center**:

- Assign a Copilot Studio user license  
- Assign it either directly to your account or via a security group  

Without the correct license, publishing will fail.

---

### 2. Enable Teams App Settings (If Publishing to Teams)

In the **Microsoft Teams Admin Center**:

1. Navigate to:
   - Teams apps  
   - Setup policies  

2. Edit the relevant policy (e.g., Global)

3. Enable:

   "Upload custom apps"

If this setting is disabled, the agent cannot be added to Teams.

---

### 3. Configure Power Platform Settings

In the **Power Platform Admin Center**:

1. Go to **Tenant Settings**
2. Locate:

   "Copilot Studio Authors (preview)"

3. Add your security group to this setting

This allows users to create and manage agents.

---

### 4. Check Data Policies

In the **Power Platform Admin Center**:

1. Go to **Data policies**
2. Ensure required connectors (such as Microsoft Teams) are not blocked

Blocked connectors may prevent publishing or channel configuration.

---

### 5. Wait for Permission Propagation

After changes:

- Allow several hours (sometimes up to 24 hours)
- Log out and back in if necessary

Permission changes are not always instant.

---

## Lab Outcome

Pre-Built Agent Deployed: Yes  
Generative AI Enabled: Yes  
Knowledge Source Added: Yes  
Agent Tested: Yes  
Agent Published: Yes  

Mission Status: Complete
