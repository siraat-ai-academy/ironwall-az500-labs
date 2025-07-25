# 🛡️ Lab 4: Set Up Alerts for a Virtual Machine

## 🔮 Scenario Setup

The morning sun peeked through the soft clouds over Copenhagen. 🌤️ Mr. eks2 had just entered the Azure training lab, wearing his cozy hoodie with “Curious Always” stitched in tiny letters.

“Godmorgen!” smiled **Kasper Madsen**, already at the keyboard with his coffee mug. “Ready for a little magic with Azure alerts?”

Beside him, **Sofia Zaymera** nodded gently, “Today we’ll teach our cloud to *talk back* to us — when something happens, it should *let us know.*”

Mr. eks2’s eyes lit up. “You mean… like a digital whisper? When something important changes?”

Kasper chuckled. “Exactly! This lab helps you get notified when important events happen. Very useful when you're a security guard of the cloud castle.”

Let’s dive in! 🚀

---

## 🛠️ Step-by-Step with Story & Dialogues

### ✅ Step 1: Create a Virtual Machine

**Kasper**: “Alright, we’re building a small server in the cloud — like setting up a little office computer, but in the sky!” ☁️

- Go to **Virtual Machines** in the **Azure Portal**.
- Click **+ Create > Azure virtual machine**.
- Under the **Basics** tab, fill in:
  - **Resource Group**: `NordicInfra-RG`
  - **VM name**: `NordicVault-VM`
  - **Region**: East US
  - **Availability**: No infrastructure redundancy required
  - **Security type**: Standard
  - **Image**: Windows Server 2022 Datacenter
  - **Size**: B2s
  - **Username**: nordicuser
  - **Password**: SomethingSecure!123
  - **Inbound Ports**: None

**Sofia**: “Don’t forget to go to the **Disks** tab and change the disk type to **Standard SSD**. It saves money and is good for testing.”

> 💡 “Disk” means the computer’s storage — in Danish, we say **disk** or **lager**.

- Click **Review + Create**, then **Create**.

**Mr. eks2**: “So… we just built a virtual machine (virtuel maskine) that lives somewhere in East US. Feels like cloud Lego.”

---

### 🔔 Step 2: Create an Alert for the Virtual Machine

**Kasper**: “Now, let’s make sure our cloud whispers to us if something important happens — like someone restarting the VM.”

- Go to your VM: **NordicVault-VM**
- Under **Monitoring**, select **Alerts**
- Click **+ Create > Alert rule**

**Sofia**: “The *scope* defines where the alert watches — like telling your camera what part of the house to monitor.”

- Click **+ Select scope**
- Search for **Virtual Machines**
- Select **NordicVault-VM** and click **Apply**

- Under **Condition**, click **See all signals**
- Search for **All Administrative operations**
- Click **Apply**

**Mr. eks2**: “So we’re watching for any admin-level actions, like restarting or changing settings?”

**Sofia**: “Exactly — it’s like listening for someone opening the control panel.”

- Under **Action**, click **+ Create action group**
- Fill in:
  - **Resource Group**: `NordicInfra-RG`
  - **Action Group Name**: `NordicAlertGroup`
  - **Display Name**: `AlertMe`

- Under **Notifications**, choose **Email**
  - Name: `NordicEmail`
  - Tick **Email**, enter your email, confirm.

- Click **Review + Create**, then **Create**.

- Back in **Alert rule**, name it: `User-Admin-Alert`
- Click **Review + Create**, then **Create**

**Mr. eks2**: “It’s like we’re giving our VM a voice! When it feels a poke, it tells us.” 😄

---

### 🔄 Step 3: Trigger and Verify the Alert

**Kasper**: “Let’s test it. Time to *poke* the VM.”

- Go back to **Virtual Machines**
- Open **NordicVault-VM**
- Click **Restart**

**Sofia**: “Now, wait a few minutes. Then check your email inbox. If everything’s set up, the alert will arrive like a little cloud message.”

**Mr. eks2**: (checks inbox) “It worked! I got an email — it says an admin action occurred. That’s… kind of amazing.”

- 🧹 Finally, delete all resources to clean up.

---

## 🌍 Real-World Reflection

This lab teaches how to set up alerts — a basic but powerful skill for cloud defenders. In real IT jobs, alerts help security teams stay informed when something changes. Imagine a hacker tries to restart your server, or a teammate makes an accidental change — with alerts, you’ll know right away. It’s like having a digital early-warning system. 🚨

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word           |
|------------------------|-----------------------|
| Resource Group         | Ressourcegruppe       |
| Virtual Machine        | Virtuel Maskine       |
| Storage Disk           | Lagerdisk             |
| Alert                  | Alarm / Varsel        |
| Action Group           | Handlingsgruppe       |
| Email Notification     | E-mailnotifikation     |
| Monitoring             | Overvågning           |
| Restart                | Genstart              |
| Scope                  | Omfang                |
| Condition              | Betingelse            |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
