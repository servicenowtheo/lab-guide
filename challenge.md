## Bonus Challenge: Give Your Specialist Knowledge

**Objective:** Author a brand new knowledge article in the IT Knowledge Base, publish it, then create an incident that the AI L1 Service Desk Specialist will deflect using your article.

> **This is where Zero Touch Support gets personal** — the AI Specialist is only as good as the knowledge you give it. Better articles mean faster, more accurate resolutions.

### Step 1 — Navigate to Knowledge Center

1. In the filter navigator, type `Knowledge Center` and select **Knowledge > Knowledge Center**.

### Step 2 — Create a New Article

1. Under **Actions** on the right side of the page, select **Create an article**.
2. On the **Create new article** page:
   - **Select knowledge base:** Choose **IT**
   - **Select article template:** Choose **Standard**
3. Select **Next** in the top-right corner.

### Step 3 — Write Your Knowledge Article

1. In the **Short description** field, enter the title for your article (choose one of the options below or write your own).
2. In the article body canvas:
   - From the **Blocks** panel on the right, drag the **1 Column** component onto the canvas.
   - Then drag the **Text** block into the column.
   - Select the Text block and paste or type your article content.

---

#### Option A: Password Reset Self-Service Guide

**Short description:** `How to Reset Your Password Using Self-Service`

If you're locked out of your account or need to change your password, follow these steps to reset it without contacting the service desk.

**Reset via the Self-Service Portal:**

1. Navigate to the ServiceNow Employee Center at your instance URL + `/esc`.
2. On the login screen, select "Forgot Password."
3. Enter your corporate email address and select Submit.
4. Check your email for a password reset link. The link expires after 15 minutes.
5. Select the link and enter a new password that meets the following requirements: at least 12 characters, one uppercase letter, one lowercase letter, one number, and one special character.
6. Confirm your new password and select Save.
7. Return to the login page and sign in with your new password.

**Reset via Mobile Device:** If you have the ServiceNow mobile app installed, open the app, tap "Forgot Password" on the login screen, and follow the same steps above.

**Still locked out?** If you do not receive the reset email within 5 minutes, check your spam or junk folder. If the issue persists, contact the IT Service Desk and request a manual password reset. Please have your employee ID ready for verification.

---

#### Option B: Troubleshooting Common Outlook Issues

**Short description:** `Outlook FAQs — Fixing Sync, Crash, and Performance Issues`

This article covers the most common Microsoft Outlook issues reported by employees and how to resolve them.

**Outlook is not syncing emails:**
1. Check your internet connection by opening a web browser and navigating to any website.
2. In Outlook, go to File > Account Settings > Account Settings, select your email account, and choose Repair.
3. Follow the prompts to complete the repair process and restart Outlook.
4. If the issue persists, try removing and re-adding your email account.

**Outlook keeps crashing or freezing:**
1. Close Outlook completely.
2. Open Outlook in Safe Mode by holding the Ctrl key while launching Outlook, then select Yes when prompted.
3. If Outlook works in Safe Mode, the issue is likely caused by an add-in. Go to File > Options > Add-ins > Manage COM Add-ins > Go, and disable all add-ins. Re-enable them one at a time to identify the culprit.
4. If Outlook crashes in Safe Mode as well, try repairing the Outlook data file by running the Inbox Repair Tool (ScanPST.exe) located at `C:\Program Files\Microsoft Office\root\Office16`.

**Outlook is running slowly:**
1. Check your mailbox size by going to File > Mailbox Settings. If your mailbox is over 90% capacity, archive or delete old emails.
2. Disable unnecessary add-ins (see steps above).
3. Compact your Outlook data file by going to File > Account Settings > Data Files, selecting your data file, and choosing Compact Now.
4. Ensure Outlook and Windows are fully updated.

**Cannot send or receive attachments:** Attachments are limited to 25 MB per message. For larger files, upload the file to OneDrive or SharePoint and share a link instead.

---

#### Option C: Connecting to the Corporate VPN

**Short description:** `How to Connect to the Corporate VPN from Home or a Remote Location`

This article explains how to connect to the corporate VPN (Zscaler Private Access) to securely access company resources when working remotely.

**Before you begin:** Ensure that the Zscaler Client Connector application is installed on your device. It is pre-installed on all company-managed laptops. If you do not see the Zscaler icon in your system tray (Windows) or menu bar (Mac), contact the IT Service Desk to have it installed.

**Connecting to the VPN:**
1. Locate the Zscaler Client Connector icon in your system tray (Windows, bottom-right) or menu bar (Mac, top-right).
2. Select the icon and choose "Open Zscaler."
3. If you are not signed in, select Sign In and authenticate using your corporate email and password. Complete multi-factor authentication if prompted.
4. Once signed in, the Zscaler Client Connector will automatically establish a secure tunnel. The icon will turn green when connected.
5. Verify connectivity by accessing an internal resource such as the company intranet or SharePoint.

**Troubleshooting VPN connectivity:** If the Zscaler icon shows a red or yellow status:
1. Right-click the Zscaler icon and select Restart Service.
2. If the issue persists, disconnect from any personal VPNs or proxy services that may conflict with Zscaler.
3. Restart your device and try connecting again.
4. Ensure your operating system and Zscaler Client Connector are up to date.
5. If you are on a restricted network (hotel, airport, public Wi-Fi), try switching to a mobile hotspot to rule out network-level blocking.

**Still unable to connect?** Open a new incident with the IT Service Desk. Include: your device name, operating system version, the network you are connected to, and any error messages displayed by Zscaler.

---

### Step 4 — Save and Submit for Review

1. Review your article content for completeness.
2. Select **Save** in the top-right corner.
3. Update the **Workflow** field from `Draft` to `Review`.
4. Select **Save** again.

> The article is now in review and requires approval before it can be published. A banner will appear: *"This knowledge item is in review."*

### Step 5 — Approve the Knowledge Article

The article requires approval before it becomes available to the AI Specialist. You'll need to impersonate the approver.

1. On the knowledge article record, select the **Approvals** tab.
2. Note the **Approver** name listed (e.g., `Bernard Laboy`).
3. Select your **user avatar** in the top-right corner → **Impersonate another user**.
4. Type the approver's name and select them from the list → **Impersonate user**.
5. Navigate to **My Approvals**: filter navigator → `My Approvals` → **Service Desk > My Approvals**.
6. Sort by **Created** to find the most recent approval request.
7. Select the approval record for your knowledge article.
8. Review the **Summary of item being approved** to confirm it's your article.
9. Select **Approve**.

**End impersonation:** Select your user avatar → **End impersonation** to return to your admin account.

> Once approved, the article's workflow state changes to **Published** and the content becomes available to the AI Specialist's knowledge sources.

### Step 6 — Create a Matching Incident

1. Navigate to **Service Operations Workspace** (Workspaces > Service Operations Workspace).
2. Create a new incident:
   - **Caller:** Able Tuter
   - **Channel:** Email
   - **Short description:** Use a description that matches your article:

| If you wrote... | Create an incident with... |
|----------------|---------------------------|
| Password Reset Self-Service Guide | `I'm locked out of my account and need to reset my password` |
| Outlook FAQs | `Outlook keeps crashing every time I open it` |
| Corporate VPN Guide | `I can't connect to the VPN from my home network` |

3. In the **Assigned to** field, type `ai` and select **AI L1 Service Desk Specialist**.
4. Review the **Assign** dialog — note the Now Assist-generated work notes.
5. Select **Save**.

### Step 7 — Watch the AI Specialist Deflect the Incident

1. On the right sidebar, open the **Agentic Processes** menu item.
2. Select **Show steps** to watch the AI Specialist work through the incident in real time.
3. Observe as the AI Specialist:
   - Fetches task details
   - Researches knowledge sources
   - **Finds your newly published article**
   - Proposes a resolution using the content from your article
4. Review the **Activity** feed for the AI Specialist's resolution notes — you should see content sourced from the article you just wrote!

### ✅ Final Checkpoint

You have successfully:
- Created a new knowledge article in the IT Knowledge Base
- Submitted the article for review and approved it by impersonating the designated approver
- Published the article so it's available to the AI Specialist
- Created a matching incident and assigned it to the AI Specialist
- Watched the AI Specialist use your article to autonomously deflect the incident

**This is the power of Zero Touch Support — the more knowledge you feed the system, the smarter it gets.**
