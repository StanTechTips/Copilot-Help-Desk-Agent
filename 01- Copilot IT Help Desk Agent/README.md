# 🤖 Copilot IT Help Desk Agent - Setup Guide

> A complete step-by-step guide to building and deploying an AI-powered 
> IT Help Desk Agent for your Microsoft 365 tenant using Copilot Studio.

---

## 📋 Prerequisites

Before you begin, make sure everything below is in place.  
Skipping this step can cause silent failures that are difficult to debug later.

---

## Step 1 - Verify Licences & Access

Confirm that your tenant has the correct licences assigned before making any configuration changes.

### ✅ Required Licences

| Licence | Purpose |
|---|---|
| Microsoft 365 Business Standard or higher | Required for Power Automate and Shared Mailbox |
| Copilot Studio | Standalone or included via Microsoft 365 Copilot |
| Power Automate (Per-user or Per-flow) | Sends automated email on ticket submission |
| Exchange Online | Powers the shared mailbox that receives IT tickets |

### ⚠️ Important Notes

- If you are unsure which licences your tenant has, go to the 
  [Microsoft 365 Admin Centre](https://admin.microsoft.com) → **Billing** → **Licences**
- All licences must be **assigned to your account** before proceeding, 
  not just available in the tenant
- Copilot Studio has a **free trial** available if you do not yet have a licence

---

## ✅ Checklist Before Moving On

Before continuing to Step 2, confirm the following:

- [ ] Microsoft 365 Business Standard or higher — assigned
- [ ] Copilot Studio licence - assigned
- [ ] Power Automate licence - assigned
- [ ] Exchange Online - active on your tenant

---

> **Next Step →** [02 - Create or Verify a Shared Mailbox](../02%20-%20Create%20or%20verify%20a%20shared%20mailbox/README.md)
