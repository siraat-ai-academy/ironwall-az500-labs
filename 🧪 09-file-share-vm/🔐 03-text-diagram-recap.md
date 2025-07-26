
# 📊 AZ-500 Diagram + Friendly Breakdown  
**Lab 9: Create an SMB Azure file share and connect it to a Windows VM**

---

## 🖼️ Text-Based Diagram

```
+-----------------------+
|  Resource Group       |
|  DKSec-Resource01     |
+-----------------------+
            |
            v
+-----------------------+
|  Storage Account      |
|  NordicFilesStorage   |
+-----------------------+
            |
            v
+-----------------------+
|  File Share           |
|  qsfileshare          |
+-----------------------+
            |
            v
+-----------------------+
|  Uploaded File        |
|  qsTestFile.txt       |
+-----------------------+

            |
            v
+-----------------------+
|  Virtual Machine      |
|  VM-Kasper01          |
+-----------------------+
            |
            v
+-----------------------+
|  PowerShell Mapping   |
|  (Drive Letter Z:)    |
+-----------------------+
            |
            v
+-----------------------+
|  Snapshots Created    |
|  & Restored from VM   |
+-----------------------+
```

---

## 🎭 Friendly Walkthrough with Kasper, Sofia & Mr. eks2

**Kasper**: Alright eks2! Think of this setup like renting a digital storage unit in the cloud and then connecting it to your work PC — but without the heavy lifting or dusty keys!

**Sofia**: And because it's **Azure**, this file share is not just convenient, it's also secure and recoverable. You can even **snapshots** it like a time machine! ⏳

**Mr. eks2**: Wait… so I can go back to older versions of a file, even if I mess up?

**Kasper**: Exactly! One click and *poof* — your file goes back to its old self, before it saw anything embarrassing 😄

---

## 🔧 Tool-by-Tool Breakdown

### 🗃️ **Storage Account**
**Kasper**: This is like the digital warehouse. Everything begins here — like a main folder where other folders live.

**Sofia**: And remember, we chose **LRS (Locally Redundant Storage)** to keep three copies inside the same region. It's good for budget and still offers safety.

---

### 📁 **File Share**
**Kasper**: Think of it as a shared team folder, but in the cloud. Great for shared access from multiple machines.

**Sofia**: It supports **SMB** protocol, so Windows VMs can map it like a regular drive. Plus, you can control access with precise permissions.

---

### 💻 **Virtual Machine**
**Kasper**: Our test buddy! It’s like setting up a cloud-based laptop that lives in Azure. We used **Windows Server 2019**.

**Sofia**: Don’t forget to **limit RDP access** when you're done. Leaving ports open is like forgetting to lock your house!

---

### 🔄 **PowerShell Script (for Mapping)**
**Kasper**: This script tells your VM to "Hey! Mount this file share like Drive Z:". It’s like plugging in a USB stick without leaving your chair.

**Sofia**: Always review scripts before running them — especially if copied from outside sources.

---

### 📸 **Snapshots**
**Kasper**: Snapshots are like file selfies! They capture the moment so you can return to it later.

**Sofia**: And they're life savers in security audits and accidental deletions.

---

## 🌍 Real-World Reflection

This lab helps learners understand how **Azure File Shares** can be securely connected to VMs and backed up with **snapshots**. It's the kind of real-world task a junior cloud admin or security analyst might do in a hybrid IT setup — especially when managing shared data across teams.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word         |
|------------------------|---------------------|
| Resource Group         | Ressourcegruppe     |
| Storage Account        | Lagerkonto          |
| File Share             | Fildeling           |
| Snapshot               | Øjebliksbillede     |
| Virtual Machine        | Virtuel Maskine     |
| PowerShell             | PowerShell          |
| Windows Server         | Windows Server      |
| Region                 | Region              |
| Upload                 | Overfør             |
| Backup                 | Sikkerhedskopi      |

---

## 🧾 Guided by:  
🛸 **Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
**🇩🇰 Kasper Madsen** — a joyful Danish Azure Security Specialist who turns labs into friendly journeys  
**🇪🇸 Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity  
**✍️ Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen  
🔎 See full character bios in the README file.

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
