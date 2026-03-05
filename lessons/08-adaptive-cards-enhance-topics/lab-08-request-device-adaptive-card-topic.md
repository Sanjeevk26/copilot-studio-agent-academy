# lab-08-request-device-adaptive-card-topic.md

# Lab 08 – Add Adaptive Cards and Enhance Topic Capabilities

## Lab Objective

Enhance the device experience by creating a new topic that uses an Adaptive Card to collect structured user input.

This lab will:

- Create a new topic named Request device
- Add an Ask with adaptive card node
- Build the card first using JSON as a base template
- Convert the adaptive card to Formula mode
- Use Power Fx to dynamically generate device options from a global variable created in Lab 07
- Update agent instructions to route conversations between topics
- Test cross-topic redirection and validate card rendering

---

## Use Case

As an employee  
I want to request a device  
So that I can request a device from the list of available devices  

---

## Prerequisites

- Devices SharePoint list exists in the Contoso IT SharePoint site (Lesson 00)
- Contoso Helpdesk Agent exists (Lesson 06)
- Available devices topic implemented (Lesson 07 / Lab 07)
- Global variable exists from Lab 07:

Global.VarDevices.value

This global variable stores the SharePoint Get items response (table of devices).

---

## 8.1 Create a New Topic with an Adaptive Card

### Create Topic From Blank

1. Open the Contoso Helpdesk Agent in Copilot Studio
2. Go to Topics
3. Select Add a topic
4. Select From blank

Topic name:

Request device

Trigger description:

This topic helps users request a device when they answer yes to the question that asks the user if they would like to request one of these devices.

Save the topic.

---

## 8.1 Add Ask with Adaptive Card Node

1. Select the plus icon under the trigger
2. Select Ask with adaptive card
3. Select the node to open Adaptive Card node properties
4. Select Edit adaptive card

This opens the Adaptive Card Designer.

---

## 8.1 Adaptive Card Designer Orientation (Optional)

In the designer, you can:

- Drag and drop elements (TextBlock, FactSet, Inputs)
- Preview how the card renders
- Inspect the card structure hierarchy
- Edit element properties
- Edit the card payload JSON directly

To reset the canvas:

- Use Undo to remove added elements
- Or select all payload text and delete before pasting a full payload

---

## 8.1 Paste the Base JSON Template

1. In the Card payload editor, select all text and delete it
2. Paste the JSON from the Request devices JSON file (provided in your lab assets)
3. Confirm the preview shows:
   - Intro text
   - A list of placeholder available devices

Select Save and Close to exit the designer.

In the topic canvas, confirm the adaptive card is visible.

---

## 8.1 Review Adaptive Card Output Variables

At the bottom of the adaptive card node, confirm output variables exist such as:

- commentsId
- deviceSelectionId

These output variables capture user input from the card elements and are used later in the flow.

---

## 8.1 Convert the Adaptive Card to Formula Mode

We now update the card so it dynamically displays devices returned from SharePoint.

1. Select the adaptive card node
2. Select the chevron and change authoring mode to Formula
3. Select the expand icon to enlarge the formula editor
4. Select all existing payload content and delete it
5. Paste the Power Fx formula from the Request Devices formula file (provided in your lab assets)

Key concept:

- The formula loops through Global.VarDevices.value using ForAll
- The choice label uses the device Model field
- The choice value uses the SharePoint item ID
- If(IsBlank()) wrappers ensure required properties are non-null to avoid rendering errors such as:
  Property cannot be null

Close the card modal.

Close the Adaptive Card node properties pane.

Save the topic.

---

## 8.2 Update Agent Instructions to Invoke Request Device Topic

Now that the Request device topic exists, we update the agent instructions for orchestration routing.

1. Go to Overview
2. Select Edit instructions
3. Add a new line under the previous device instruction:

2. If the user answers yes to the question of requesting a device, trigger [Request device]. Otherwise if they answer no to the question of requesting a device, trigger [Goodbye].

4. Replace [Request device] by selecting the bracketed text and typing:
   /Req
   Then select Request device from the topic list.

5. Replace [Goodbye] by selecting the bracketed text and typing:
   /Goodbye
   Then select Goodbye from the list.

Save instructions.

Expected behavior:

- User asks for devices, Available devices runs
- Agent asks if user wants to request one
- If user says yes, redirect to Request device and show adaptive card
- If user says no, redirect to Goodbye

---

## 8.3 Test Cross-Topic Redirection and Adaptive Card Rendering

1. Select Test and refresh the test pane
2. Open Activity map
3. Enable Track between topics

Test prompt:

I need a laptop

The agent should:

- Run Available devices
- Display device list
- Ask if the user wants to request a device

Respond:

yes please

Expected outcome:

- Conversation redirects to Request device topic
- The adaptive card renders with interactive elements
- Device options are populated dynamically from Global.VarDevices.value

Refresh the test pane to clear the session after validation.

---

## Completion Checklist

- New topic created: Request device
- Ask with adaptive card node added
- Base JSON template pasted successfully
- Card converted to Formula mode
- Power Fx formula applied using Global.VarDevices.value
- Output variables confirmed (deviceSelectionId, commentsId)
- Agent instructions updated for routing
- Track between topics enabled and verified
- Adaptive card displayed after redirect

---

## Result

The agent now supports device requests using an interactive Adaptive Card and can route from device lookup to device request using topic-based orchestration.
