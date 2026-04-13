# 🗂️ Step 4 — Build the "Submit a Ticket" Topic

> Topics are the conversation scripts your agent follows.
> This topic triggers when a user wants to raise a ticket and collects
> four key pieces of information before handing off to Power Automate.

---

## What Are We Doing Here?

In Copilot Studio, **Topics** define how your agent responds to specific user intentions.
In this step, you will build the core topic of the entire agent — the conversation flow
that guides a user through submitting an IT support ticket step by step.

---

## 🛠️ Create the Topic

### Step 1 - Add a New Topic

1. Inside your agent, click **Topics** in the left navigation
2. Click **+ Add topic**
3. Select **From blank**
4. Name the topic: `Submit IT Ticket`

---

### Step 2 - Add Trigger Phrases

Trigger phrases are what the user types to activate this topic.
Add the following phrases, one per line:

```
I need IT help
Submit a ticket
Report an issue
I have a problem with my computer
IT support
Raise a support request
Something is broken
```

> **Tip:** The more trigger phrases you add, the better the agent
> is in recognising when a user wants to raise a ticket.

---

## 💬 Build the Conversation Nodes

Work through each node in order by clicking the **+** button below the previous node.

---

### Node 1 - Welcome Message

| Setting | Value |
|---|---|
| Node type | **Send a message** |
| Text | `Sure, I can help you raise an IT support ticket. Let me collect a few details.` |

---

### Node 2 - Collect Full Name

| Setting | Value |
|---|---|
| Node type | **Ask a question** |
| Question | `What is your full name?` |
| Identify | Person's Name |
| Save response to | `UserName` |

---

### Node 3 - Collect Email Address

| Setting | Value |
|---|---|
| Node type | **Ask a question** |
| Question | `What is your work email address?` |
| Identify | Email |
| Save response to | `UserEmail` |

---

### Node 4 - Collect Issue Description

| Setting | Value |
|---|---|
| Node type | **Ask a question** |
| Question | `Please describe your issue in a few sentences.` |
| Identify | Entire response |
| Save response to | `IssueDescription` |

---

### Node 5 - Collect Urgency Level

| Setting | Value |
|---|---|
| Node type | **Ask a question** |
| Question | `How urgent is this?` |
| Answer options | `Low` / `Medium` / `High` (quick-reply buttons) |
| Save response to | `Urgency` |

> **Tip:** Using quick-reply buttons here prevents users from typing
> freeform answers and keeps your data consistent for reporting.

---

### Node 6 - Confirmation Message

| Setting | Value |
|---|---|
| Node type | **Send a message** |
| Text | `Thanks {UserName}. I am submitting your ticket now — you will receive a confirmation at {UserEmail} shortly.` |

> **Note:** `{UserName}` and `{UserEmail}` are dynamic variables that will
> automatically populate with the answers the user provided earlier in the conversation.

---

## 📸 Reference Screenshots

![Submit a Ticket Topic](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Submite-a-ticket-1.png)

![Submit a Ticket Topic](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Submite-a-ticket-2.png)

---

## ✅ Checklist Before Moving On

- [ ] Topic created and named `Submit IT Ticket`
- [ ] All 7 trigger phrases added
- [ ] Node 1 - Welcome message added
- [ ] Node 2 - Full name question added, saved to `UserName`
- [ ] Node 3 - Email question added, saved to `UserEmail`
- [ ] Node 4 - Issue description added, saved to `IssueDescription`
- [ ] Node 5 - Urgency question added with quick-reply buttons, saved to `Urgency`
- [ ] Node 6 - Confirmation message added with dynamic variables
- [ ] Topic saved

---

> **← Previous Step** [03 - Create a New Agent in Copilot Studio](../03-Create%20a%20new%20agent%20in%20Copilot%20Studio/README.md)  
> **Next Step →** `05 - Next Step Name Here`
