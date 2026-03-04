# Lab 07 – Add a New Topic with Triggers, Variables, and a SharePoint Tool

## Lab Objective

Build a structured custom topic that:

- Captures the requested device type from the user
- Retrieves matching devices from a SharePoint list using the SharePoint connector
- Filters results dynamically using Power Fx
- Returns the available devices list to the user
- Integrates the topic into agent instructions so orchestration can invoke it automatically

---

## Use Case

As an employee  
I want to know what devices are available  
So that I can see a list of available devices  

---

## Prerequisites

- Devices SharePoint list exists in the Contoso IT SharePoint site (Lesson 00)
- Contoso Helpdesk Agent exists (Lesson 06)
- You have permissions to use SharePoint connectors in Copilot Studio

---

## 7.1 Create a Topic from Blank

1. Open the Contoso Helpdesk Agent in Copilot Studio
2. Select the Topics tab near the agent name
   - If Topics is not visible, select the plus icon in the navigation and choose Topics
3. In Topics, confirm you are viewing Custom topics
4. Select Add a topic
5. Select From blank

Topic name:

Available devices

Trigger description:

This topic helps users find devices that are available from our SharePoint Devices list. User can ask to see available devices and it will return a list of devices that are available which can include laptops, smartphones, accessories and more.

---

## 7.2 Define Topic Inputs and Outputs

### Open Topic Details

1. Select the ellipsis in the topic header
2. Select Details
3. Select the Input tab

### Create Input Variable

Select Create a new variable and configure:

Variable name:

VarDeviceType

Update Identify as:

User’s entire response

Description:

List of possible values: Laptop, Desktop, Smartphone

Leave defaults for:

- How will the agent fill this input?
- Variable data type
- Display name

### Create Output Variable

Select the Output tab and create a new variable:

Variable name:

VarAvailableDevices

Variable data type:

Table

Variable description:

List of available devices by device type

Close the Topic details pane.

---

## 7.3 Add a Tool Using the SharePoint Connector

### Add SharePoint Get Items

1. Select the plus icon under the trigger node
2. Select Add a tool
3. Select Connector tab
4. Search for Get items
5. Select the SharePoint connector action Get items
6. Select Submit

### Configure Tool Properties

1. Select the ellipsis on the Get items node
2. Select Properties

In the Initiation tab, set Usage Description:

Retrieves devices from SharePoint list

In the Inputs tab:

- Select the Contoso IT SharePoint site
- Select the Devices list

### Apply Filter Query Using Power Fx

In the Filter Query field:

1. Select the ellipsis next to the field
2. Select Formula tab
3. Expand the formula editor
4. Insert this Power Fx expression:

Concatenate("Status eq 'Available' and AssetType eq '", Topic.VarDeviceType, "'")

Select Insert.

### Limit Columns by View

Set Limit Columns by View to:

All items

---

## 7.4 Configure Outputs and Store the Results

### Rename the Output Variable from Get Items

1. In the Get items configuration pane, select Outputs
2. Select the GetItems variable
3. Rename it to:

VarDevices

Set the Usage scope to:

Global

Close the variable pane.

### Set the Topic Output VarAvailableDevices

1. Select the plus icon under the Get items node
2. Choose Variable management
3. Select Set a variable value

Set the variable to:

VarAvailableDevices

For the value:

1. Select the ellipsis for the value field
2. Select Formula tab
3. Expand the formula editor
4. Insert the Power Fx expression that assigns the returned table value

Insert and save the expression.

---

## 7.5 Update Agent Instructions to Invoke the Topic

1. Go to Overview
2. Select Edit instructions
3. Locate the section about device assistance
4. Remove the old device instructions
5. Add this new instruction line:

1. Help find available devices and give full details using [Available devices]. Always extract the VarDeviceType from the inputs. After giving device details, ask the user if they want to request a device from the list of available devices.

6. Highlight the topic placeholder [Available devices]
7. Type forward slash / and select the Available devices topic
8. Save instructions

---

## 7.6 Test the Topic

1. Select Test in the top-right
2. Start a new test session
3. Enter:

I need a laptop

4. When prompted to allow connector access, select Allow

Expected outcome:

- The agent triggers the Available devices topic
- The SharePoint Get items action runs
- Devices are filtered to Status = Available and AssetType = Laptop
- The response includes device details in a readable list

---

## 7.7 Validate Connections Used by the Agent

1. Select the ellipsis in the agent menu
2. Select Manage connection
3. Confirm the SharePoint connector is listed
4. Select the Used By value to inspect details
5. Confirm the usage description is visible:

Retrieves devices from SharePoint list

Close the connection details.

---

## Completion Checklist

- Topic created from blank: Available devices
- Input variable created: VarDeviceType
- Output variable created: VarAvailableDevices (Table)
- SharePoint Get items tool added and configured
- Filter query implemented using Power Fx
- Output stored and scoped correctly
- Agent instructions updated to invoke topic
- Topic tested successfully
- Connections validated in Manage connection

---

## Result

The agent now supports device availability queries using a structured topic that retrieves live data from SharePoint and responds with results grounded in enterprise data.
