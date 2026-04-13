# ⚡ Step 6 - Create the Power Automate Flow

> This flow is what actually sends the ticket details as an email
> to your shared mailbox. It is triggered directly from inside
> your Copilot Studio topic.

---

## What Are We Doing Here?

When a user completes the **Submit IT Ticket** topic, Copilot Studio needs
something to action the collected data. That is where **Power Automate** comes in.

In this step, you will build a flow that:
1. Receives the four variables from your Copilot topic
2. Sends a formatted email to your shared mailbox
3. Returns a confirmation status back to the agent

---

## 🛠️ Create the Flow

### Step 1 - Launch Power Automate From Copilot Studio

1. Open your **Submit IT Ticket** topic
2. Click the **+** below the confirmation message node
3. Select **Call an action** → **Create a flow**
4. Power Automate will open automatically with the trigger already set to **Run a flow from Copilot**

---

### Step 2 - Configure the Flow Inputs

1. Click the **trigger card** at the top of the flow
2. Click **Add an input** and add all four inputs below:

| Input Name | Type |
|---|---|
| `UserName` | Text |
| `UserEmail` | Text |
| `IssueDescription` | Text |
| `Urgency` | Text |

> **Important:** Input names are case-sensitive. Make sure they match
> exactly as shown — these must align with the variable names
> you set in your Copilot topic in Step 4.

---

### Step 3 - Add the Send an Email Action

1. Click **+ New step**
2. Search for `Send an email (V2)`
3. Select it using the **Office 365 Outlook** connector

---

### Step 4 - Configure the Email

Fill in the email fields as follows:

| Field | Value |
|---|---|
| **To** | `ithelpdesk@yourdomain.com` *(your shared mailbox address)* |
| **Subject** | `[IT Ticket]` + `UserName` input + `—` + `Urgency` input + `Priority` |
| **Body** | See template below |

Use the **dynamic content** tokens (lightning bolt ⚡ icon) inside each
field to insert the live values from the flow inputs rather than typing them manually.

---

### 📧 Email Body Template

Copy the template below and replace each bracketed item with the
matching **dynamic content token** from Power Automate:

```
A new IT support ticket has been submitted.

Submitted by:     [UserName]
Contact email:    [UserEmail]
Urgency:          [Urgency]

Issue description:
[IssueDescription]

---
This ticket was submitted automatically via the IT Help Desk Agent.
```

---

### Step 5 - Return a Status to Copilot Studio

1. Click **+ New step**
2. Select **Return value(s) to Power Virtual Agents**
3. Click **Add an output** and fill in:

| Field | Value |
|---|---|
| **Name** | `TicketStatus` |
| **Value** | `Submitted` |

---

### Step 6 - Save the Flow

1. Click **Save**
2. Name the flow: `IT Ticket — Send Email.`

> **Tip:** Give it a clear name now — if you build more flows later,
> A good name saves a lot of confusion when managing them in Power Automate.

---

## 📸 Reference Screenshots

![Power Automate Flow Inputs](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Power-Automate-create-flow.png)

![Send Email Configuration](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Power-Automate-send-email.png)

![Return Value Configuration](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/main/Images/Flow-Return-Value.png)

---

## ✅ Checklist Before Moving On

- [ ] Flow created from inside the Submit IT Ticket topic
- [ ] All four inputs added to the trigger — `UserName`, `UserEmail`, `IssueDescription`, `Urgency.`
- [ ] Send an email (V2) action added using Office 365 Outlook connector
- [ ] Email `To` field set to your shared mailbox address
- [ ] Email subject configured with dynamic content
- [ ] Email body populated with all four dynamic content tokens
- [ ] Return value added — `TicketStatus` = `Submitted`
- [ ] Flow saved and named `IT Ticket — Send Email.`

---

> **← Previous Step** [05 - Add a "Greeting" and "Fallback" Topic](../05%20-%20Add%20a%20%22Greeting%22%20and%20%22Fallback%22%20topic/README.md)  
> **Next Step →** `07 - Next Step Name Here`
