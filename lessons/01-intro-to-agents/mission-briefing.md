# Mission 01 — Introduction to Agents

## 🎯 Mission Brief

Welcome, Recruit.

Before you start building agents, you need a solid understanding of the AI concepts that power them. This mission establishes the **foundational mental models** behind conversational AI, Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), and the different types of agents you can build in Copilot Studio.

Think of this mission as learning how the engine works before you start flying the aircraft.

---

## 🔎 Objectives

By completing this mission, you will understand:

- What conversational AI is and where it is used
- How Large Language Models (LLMs) power modern chat experiences
- What Retrieval-Augmented Generation (RAG) adds to LLM-based systems
- The difference between conversational agents and autonomous agents
- How Copilot Studio brings all of these concepts together

---

## 🗣️ What Is Conversational AI?

Conversational AI refers to systems that can understand, process, and respond to human language (text or speech) in a natural, interactive way.

Common examples include:
- Chatbots that help you track orders or answer FAQs
- Virtual assistants embedded in productivity tools
- AI agents embedded in collaboration platforms like Microsoft Teams

Most modern conversational AI systems are powered by **Large Language Models (LLMs)**.

---

## 🧠 Large Language Models (LLMs) — The Basics

Large Language Models are neural networks trained on massive amounts of text data. Their goal is to learn the patterns of human language so they can generate coherent and context-aware responses.

### Key Concepts

**Training Data**  
LLMs are trained on terabytes of text such as web pages, books, articles, and documentation. This gives them broad, general-purpose knowledge.

**Tokenization**  
Text is broken down into tokens (words, parts of words, or characters). The model predicts the next token based on previous tokens.

**Context Window**  
Each model has a maximum number of tokens it can consider at one time. When the limit is exceeded, older parts of the conversation are truncated.

**Prompting**  
You interact with an LLM using prompts. Clear, well-structured prompts lead to better, more focused responses.

> **Pro Tip**  
> A useful analogy is to think of an LLM as a *very advanced autocomplete system*. It doesn’t “understand” meaning like a human, but it is extremely good at predicting what should come next.

---

## 🔎 Retrieval-Augmented Generation (RAG)

LLMs are trained on static data, which means:
- They may not know recent information
- They can hallucinate when asked about specific internal content

**Retrieval-Augmented Generation (RAG)** solves this problem by grounding the model’s responses in external data sources.

### How RAG Works

1. **User Query**  
   A user asks a question.

2. **Retrieval Step**  
   The system searches relevant knowledge sources such as:
   - SharePoint libraries
   - Dataverse
   - Internal documents
   - Websites or APIs

3. **Augmentation**  
   The retrieved content is injected into the prompt sent to the LLM.

4. **Generation**  
   The LLM generates a response using both the user’s question and the retrieved context.

With RAG, your agent can provide **accurate, up-to-date, and organization-specific answers**.

---

## 🤖 Conversational vs. Autonomous Agents

In Copilot Studio, the term *agent* can describe different operating models.

### Conversational Agents

- Operate through back-and-forth dialogue
- Maintain context across multiple conversation turns
- Can call tools or APIs during conversations
- Require explicit user interaction

**Common use cases**
- Customer support bots
- HR or IT helpdesk agents
- Guided data collection or FAQs

**Examples**
- An agent in Teams answering HR policy questions
- A website chatbot answering product queries

---

### Autonomous Agents

- Can act without continuous user interaction
- Triggered by events, schedules, or external signals
- Use reasoning loops such as *plan → act → observe → replan*
- Execute multi-step tasks independently

**Common use cases**
- Automated report generation
- Workflow orchestration
- Monitoring and response agents

**Examples**
- An agent that creates a travel itinerary and sends confirmations automatically
- A meeting summarization agent that writes notes without user prompts

---

### 🔑 Key Difference

| Conversational Agents | Autonomous Agents |
|----------------------|------------------|
| Require user dialogue | Triggered by events |
| React to user input | Act independently |
| Focus on interaction | Focus on execution |

---

## 🧩 Agents in Copilot Studio

Copilot Studio allows you to build both conversational and autonomous agents using a unified platform.

Key capabilities include:

- **Visual Agent Designer**  
  Drag-and-drop canvas to design and test agents

- **Model Selection**  
  Choose from supported LLM providers and models

- **Knowledge Integration**  
  Native RAG support using SharePoint, OneDrive, Dataverse, and more

- **Tool Integration**  
  Call Power Automate flows, APIs, and enterprise systems

- **Multi-Modal Support**  
  Text, file uploads, and speech-based interactions

- **Publishing & Distribution**  
  Deploy agents to Microsoft Teams, Microsoft 365 Copilot, or external channels

---

## ✅ Mission Complete

You now understand the foundational concepts behind agents:

- **LLMs** are the reasoning and language engine
- **RAG** grounds responses in real, up-to-date data
- **Conversational agents** focus on dialogue
- **Autonomous agents** focus on action
- **Copilot Studio** brings these together in a single development experience

---

## ➡️ Next Mission

Mission 02 will introduce the **core building blocks of Copilot Studio**, including:
- Knowledge
- Skills
- Autonomy

Stay sharp, Recruit — the real building begins next.
