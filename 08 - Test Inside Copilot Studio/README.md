# 🧪 Step 8 - Test Inside Copilot Studio

> Before publishing, run a full end-to-end test from within Copilot Studio.
> This confirms the topic triggers correctly, variables are collected,
> and the Power Automate flow runs successfully.

---

## What Are We Doing Here?

Never publish an agent without testing it first. Copilot Studio has a built-in
test panel that lets you simulate a real conversation and verify everything
works exactly as expected — from the first trigger phrase all the way through
to the email landing in your shared mailbox.

---

## 🛠️ Run the Test

### Step 1 - Open the Test Panel

1. In Copilot Studio, click **Test your agent** in the top right corner
2. A chat window will open on the right side of the screen

---

### Step 2 - Trigger the Topic

Type the following message to start the conversation:

```
I need IT help
```

---

### Step 3 - Complete the Conversation

Follow each prompt the agent gives you and enter the test values below:

| Prompt | Test Value to Enter |
|---|---|
| Full name | `Test User` |
| Work email | `test@yourdomain.com` |
| Issue description | `This is a test ticket to verify the flow is working correctly.` |
| Urgency | Select `Low` |

---

### Step 4 - Check Your Shared Mailbox

After the agent sends its final confirmation message:

1. Open your shared mailbox at
   🔗 [https://admin.cloud.microsoft/exchange#/mailboxes](https://admin.cloud.microsoft/exchange#/mailboxes)
2. Wait **1-2 minutes** for the email to arrive
3. Open the email and verify all fields are populated correctly

---

## ✅ What to Check in the Email

Go through each item carefully before marking this step complete:

| Check | What to Verify |
|---|---|
| **Subject line** | Includes the test name and urgency level |
| **UserName** | Shows `Test User` in the email body |
| **UserEmail** | Shows `test@yourdomain.com` in the email body |
| **IssueDescription** | Shows the exact description text you typed |
| **Urgency** | Shows `Low` as selected during the conversation |
| **Delivery** | Email arrived in the **shared mailbox**, not a personal inbox |

---

## ⚠️ If the Flow Fails

If the email does not arrive or the flow errors, follow these steps to debug:

1. Go to 🔗 [https://make.powerautomate.com](https://make.powerautomate.com)
2. In the left navigation click **My flows**
3. Find and click **IT Ticket - Send Email**
4. Scroll down to **Run history** and click the failed run
5. Look for any steps highlighted in **red** - these show exactly where the failure occurred
6. Common issues to check:

| Issue | Fix |
|---|---|
| Flow not triggered | Check the Call an action node is saved correctly in the topic |
| Email not sending | Verify the shared mailbox address has no typos |
| Variables showing blank | Re-check variable mapping from Step 7 |
| Connector error | Re-authenticate the Office 365 Outlook connector in Power Automate |

---

## 📸 Reference Screenshots

![Test Panel in Copilot Studio](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Test-Panel-in-Copilot-Studio.png)

![Test Email in Shared Mailbox](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Test-Email-in-Shared-Mailbox.png)

![Power Automate Run History](https://raw.githubusercontent.com/StanTechTips/Copilot-Help-Desk-Agent/refs/heads/main/Images/Power-Automate-run-history.png)

---

## ✅ Checklist Before Moving On

- [ ] Test panel opened in Copilot Studio
- [ ] Trigger phrase `I need IT help` sent successfully
- [ ] All four prompts completed with test values
- [ ] Agent sent the final confirmation message
- [ ] Test email received in the shared mailbox within 2 minutes
- [ ] Subject line includes name and urgency
- [ ] All four fields correctly populated in the email body
- [ ] Email delivered to shared mailbox, not a personal inbox

---

> **← Previous Step** [07 - Connect the Flow Back to the Topic](../07%20-%20Connect%20the%20flow%20back%20to%20the%20topic/README.md)  
> **Next Step →** [09 - Test and Publish](../09%20-%20Test%20and%20Publish/README.md)
