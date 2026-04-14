# 🔗 Step 7 - Connect the Flow Back to the Topic

> After saving the flow, you return to Copilot Studio.
> Now you must map the conversation variables collected from the user
> to the flow's input parameters so the email sends correctly.

---

## What Are We Doing Here?

In Step 6, you built the Power Automate flow that sends the ticket email.
In this step, you will **connect that flow to your Copilot topic** by mapping
each variable collected during the conversation to the matching flow input.

Think of this as plugging the wires in - the data collected from the user
needs to be explicitly told where to go.

---

## 🛠️ Map the Variables

### Step 1 - Locate the Call an Action Node

1. Return to your **Submit IT Ticket** topic in Copilot Studio
2. Find the **Call an action** node in your conversation flow
3. Click on it and select your flow: **IT Ticket — Send Email**

---

### Step 2 - Map Each Input to Its Variable

For each input field in the node, click the arrow and select
the matching variable collected earlier in the conversation:

| Flow Input | Variable to Map |
|---|---|
| `UserName` | *(Variable)* `UserName` |
| `UserEmail` | *(Variable)* `UserEmail` |
| `IssueDescription` | *(Variable)* `IssueDescription` |
| `Urgency` | *(Variable)* `Urgency` |

> **Important:** If a variable does not appear in the dropdown,
> go back and check that the variable names in your topic nodes
> match exactly — they are case-sensitive.

---

### Step 3 - Handle the Returned TicketStatus (Optional)

The flow returns a value called `TicketStatus` with the value `Submitted`.
You can optionally use this to send a dynamic follow-up message:

1. After the **Call an action** node, add a new **Send a message** node
2. Use the `TicketStatus` variable in the message, for example:

```
Your ticket status is: {TicketStatus}
Our IT team will be in touch at {UserEmail} shortly.
```

> **Tip:** Using the returned `TicketStatus` value makes the agent feel
> more dynamic and confirms to the user that the flow ran successfully.

---

### Step 4 - Save the Topic

Click **Save** in the top right of the topic editor to save all changes.

---

## 📸 Reference Screenshots

![Call an Action Node](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Map%20Variables.png)

![Variable Mapping](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Variable%20Mapping.png)

---

## ✅ Checklist Before Moving On

- [ ] Returned to the Submit IT Ticket topic in Copilot Studio
- [ ] Call an action node located and flow selected
- [ ] `UserName` mapped to `UserName` variable
- [ ] `UserEmail` mapped to `UserEmail` variable
- [ ] `IssueDescription` mapped to `IssueDescription` variable
- [ ] `Urgency` mapped to `Urgency` variable
- [ ] Optional follow-up message added using `TicketStatus`
- [ ] Topic saved

---

> **← Previous Step** [06 - Create the Power Automate Flow](../06%20-%20Create%20the%20Power%20Automate%20flow/README.md)  
> **Next Step →** [08 - Test inside Copilot Studio](../08%20-%20Test%20Inside%20Copilot%20Studio/README.md)
