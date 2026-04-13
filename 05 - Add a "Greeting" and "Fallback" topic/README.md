# 👋 Step 5 — Add a "Greeting" and "Fallback" Topic

> Two extra topics that make the agent feel complete and polished
> rather than half-built. These are the first and last impressions
> your users will have of the agent.

---

## What Are We Doing Here?

Copilot Studio includes built-in **System Topics** that handle key moments
in every conversation. In this step you will customise two of them:

| Topic | Purpose |
|---|---|
| **Greeting** | The first message a user sees when they open the agent |
| **Fallback** | What the agent says when it does not understand the user's input |

Customising these makes the agent feel intentional and professional
rather than using the generic Microsoft defaults.

---

## 🛠️ Edit the Greeting Topic

### Step 1 — Open the Greeting Topic

1. In your agent, click **Topics** in the left navigation
2. Click the **System** tab
3. Select **Greeting**

---

### Step 2 — Replace the Default Message

Find the existing **Send a message** node and replace the text with:

```
Hi! I am your IT Help Desk assistant.
I can help you submit a support ticket, check the status of an existing
one, or answer general IT questions.
How can I help today?
```

> **Tip:** This message sets expectations immediately — users know exactly
> what the agent can do before they type anything.

---

## 🛠️ Edit the Fallback Topic

### Step 1 — Open the Fallback Topic

1. In your agent, click **Topics** in the left navigation
2. Click the **System** tab
3. Select **Fallback**

---

### Step 2 — Update the Fallback Message

Find the existing **Send a message** node and replace the text with:

```
I am not sure I understood that.
You can say things like "Submit a ticket", "I have an IT issue",
or "Help with my computer".
Would you like to raise a support request?
```

> **Tip:** A good fallback message never leaves the user stuck —
> it always gives them examples of what to try next.

---

## 📸 Reference Screenshots

![Greeting Topic](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/main/Images/Greeting-Topic.png)

![Fallback Topic](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/main/Images/Fallback-Topic.png)

---

## ✅ Checklist Before Moving On

- [ ] Opened the System Greeting topic
- [ ] Greeting message replaced with custom IT Help Desk welcome
- [ ] Opened the System Fallback topic
- [ ] Fallback message updated with helpful redirect examples
- [ ] Both topics saved

---

> **← Previous Step** [04 - Build the "Submit a Ticket" Topic](../04%20-%20Build%20the%20%22Submit%20a%20Ticket%22%20topic/README.md)  
> **Next Step →** `06 - Next Step Name Here`
