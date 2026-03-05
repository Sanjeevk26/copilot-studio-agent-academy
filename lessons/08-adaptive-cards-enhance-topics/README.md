# Lesson 08 – Adaptive Cards (Enhance Topic Capabilities)

## Overview

This lesson introduces Adaptive Cards in Copilot Studio and explains how they transform conversations from basic text-based interactions into rich, interactive, form-like experiences.

Adaptive Cards enable structured data collection and improved usability inside agent topics. Instead of asking multiple sequential questions in plain text, the agent can present a single interactive card with fields, choices, and submit actions.

This lesson also introduces using Power Fx within Adaptive Cards to dynamically generate card content from variables and outputs of previous nodes.

---

## Objectives

In this mission, you will learn:

- What Adaptive Cards are and how they enhance user interactions in Copilot Studio
- How to build interactive cards using JSON and Power Fx formulas for dynamic content
- How to use the Adaptive Card Designer and understand its main components
- How to create forms and structured data collection within topics using adaptive cards
- Best practices for building responsive, user-friendly cards

---

## What Is an Adaptive Card?

An Adaptive Card is an interactive UI element that can be embedded inside channels such as Microsoft Teams, Microsoft Outlook, and Copilot experiences.

An Adaptive Card is defined as a structured JSON object that determines:

- Which elements appear (text, images, buttons, inputs)
- How elements are arranged (layout)
- Which actions users can take (submit, open URL, etc.)

Because the card is JSON-based, the same definition can render consistently across different Microsoft experiences while automatically adapting to themes like light mode and dark mode.

---

## Why Adaptive Cards Matter in Copilot Studio

Adaptive Cards improve agent experiences by enabling:

- Interactive conversations: buttons, forms, and rich inputs instead of only text
- Cleaner data collection: users can submit multiple fields at once
- Better UX consistency: cards adapt visually to the channel (Teams, Copilot, etc.)
- Dynamic responses: card fields can be populated from variables and external data
- Higher completion rates: structured inputs reduce confusion and errors

---

## JSON and Power Fx in Adaptive Cards

Adaptive Cards can be authored in Copilot Studio in two ways:

### JSON Mode
- Directly define the card layout using JSON
- Useful for static or template-based cards
- Common approach when using the Adaptive Card Designer externally

### Formula Mode (Power Fx)
- Define the card payload using Power Fx
- Useful for dynamic cards that depend on variables and tool outputs
- Enables looping through datasets and conditionally showing sections

Power Fx is Excel-like and low-code. It can:

- Insert dynamic values (user name, device type, etc.)
- Format text and numbers
- Show/hide elements based on conditions
- Build repeating UI elements from data (such as device lists)

---

## Adaptive Card Designer (Conceptual Model)

The Adaptive Card Designer provides:

- A visual canvas to build cards
- A live preview of rendering output
- A structured outline of card element hierarchy
- A properties panel for element configuration
- The raw JSON payload editor for advanced customization

The designer generates JSON behind the scenes even when building visually.

---

## Common Use Cases

Adaptive Cards are commonly used for:

### Forms and Data Collection
- Device requests
- Leave requests
- Feedback forms
- Contact information capture

### Displaying Dynamic Information
- Ticket status
- Order summary
- Account balance
- Task lists

### Interactive Choices
- Pick from options
- Confirm or cancel actions
- Rating experiences

### Triggering Actions
- Submit a request
- View details
- Open a URL

---

## Best Practices

When designing Adaptive Cards:

- Keep cards simple and focused
- Use only necessary fields
- Use clear headings and short instructions
- Group related fields using Containers or ColumnSets
- Use clear Action labels (Submit Request, View Details)
- Avoid fixed widths; design for different screen sizes
- Prefer dynamic content when possible using Power Fx and variables
- Validate and test card behavior in the target channel

---

