# 🚀 Lab 7: Migrate Data to the Cloud with AzCopy

## 🔮 Scenario Setup

It was a cloudy Thursday morning in Denmark, and Mr. eks2 arrived at the lab with a USB drive in his hand and a question on his lips.

> “How do I move files… into the sky?” he asked gently.

🇩🇰 **Kasper** chuckled, “Ah, today we’re uploading earth-stuff into the cloud using a magical tool called **AzCopy**.”

🇪🇸 **Sofia** nodded warmly, “And you’ll learn how to **sync**, **upload**, and even **automate** the process. All from your terminal. It’s simpler than you think.”

Today’s mission? Move data from a local folder into **Azure Blob Storage** — like packing a suitcase, uploading it into a floating balloon, and making sure it stays updated.

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🧳 Step 1: Create a Storage Account

**Kasper**: “First, we need a digital suitcase — a **Storage Account**. It’s where your files will live in the cloud.”

**Steps:**
- Go to **Storage Accounts** > **+ Create**
- **Resource Group**: Create/select `NordicFiles-RG`
- **Storage Account Name**: `ncloudvault01`
- **Region**: East US
- **Redundancy**: GRS
- Under **Advanced**, enable **Hierarchical Namespace**

**Sofia**: “The *hierarchical namespace* helps structure your blobs like folders. It’s useful for organizing and syncing.”

**Mr. eks2**: “So this is like a smart backpack with labeled pouches. I like that.”

---

### 📦 Step 2: Create a Blob Container

**Kasper**: “Now we need a drawer inside our cloud suitcase — that’s the **Blob Container**!”

**Steps:**
- Go to the Storage Account
- Click **Containers** > **+ Container**
- Name it: `democontainer-eks2`

**Sofia**: “Remember — containers help separate different file types or teams.”

**Mr. eks2**: “So my logs don’t mix with my space poetry drafts? Perfect.”

---

### 💻 Step 3: Download and Configure AzCopy

**Kasper**: “Now we bring in the wizard: **AzCopy** — a tool that helps you move files super fast.”

**Steps:**
- Download from official link
- Extract to: `C:\Tools\AzCopy`
- In Command Prompt, navigate to folder:
  `cd C:\Tools\AzCopy`
- Run: `azcopy login` and complete the login in browser

**Sofia**: “AzCopy is powerful — but always login securely and verify what it’s accessing.”

**Mr. eks2**: “I logged in from the terminal… that felt like a moment of trust.”

---

### 📤 Step 4: Upload Files to Azure Blob Storage

**Kasper**: “Let’s do our first launch! Time to upload the files from earth to cloud.”

**Steps:**
- Prepare a folder: `C:\DataToUpload`
- Add sample files
- Use this command:
```bash
azcopy copy "C:\DataToUpload" "https://ncloudvault01.blob.core.windows.net/democontainer-eks2" --recursive=true
```
- Check the container in portal

**Sofia**: “The `--recursive=true` means it grabs all files — and subfolders too.”

**Mr. eks2**: “And just like that… my laptop is floating.”

---

### 🔁 Step 5: Modify & Sync Files

**Kasper**: “Now let’s change a file and sync! AzCopy checks what’s new and updates only that.”

**Steps:**
- Edit or add a file in `C:\DataToUpload`
- Run:
```bash
azcopy sync "C:\DataToUpload" "https://ncloudvault01.blob.core.windows.net/democontainer-eks2" --recursive=true
```

**Sofia**: “Sync is smart — it won’t re-upload what hasn’t changed.”

**Mr. eks2**: “It’s like a magical butler who only refreshes the towels.”

---

### ⏰ Step 6: Automate with Scheduled Task

**Kasper**: “Let’s automate it — every 5 minutes, AzCopy will sync your folder. Even while you nap.”

**Steps:**
- Open Notepad, paste the sync command
- Save as: `C:\Scripts\sync-ncloudedge.bat`
- In **Command Prompt (Admin)**:
```bash
schtasks /CREATE /SC minute /MO 5 /TN "AzCopy-Sync-NCloudEdge" /TR C:\Scripts\sync-ncloudedge.bat
```

**Sofia**: “This is helpful for regular updates — like from on-prem servers.”

**Mr. eks2**: “So the cloud checks my folder while I sip tea? Very Danish.”

---

### 🧹 Final Step: Delete Resources

Go to the portal and delete:
- **Storage Account**
- **Resource Group**
- **Scheduled Task**

---

## 🌍 Real-World Reflection

This lab shows you how to migrate and sync local files with **Azure Blob Storage** using **AzCopy**. In real jobs, this is used for backups, log transfers, or syncing on-prem data to the cloud. Learning to automate it makes you a time-saving hero in any cloud team.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word            |
|----------------------|-------------------------|
| Storage Account      | Lagerkonto              |
| Resource Group       | Ressourcegruppe         |
| Blob Container       | Blobbeholder            |
| AzCopy               | AzCopy (samme ord)      |
| Virtual Machine      | Virtuel Maskine         |
| Command Prompt       | Kommandoprompt          |
| Upload               | Overfør                 |
| Sync                 | Synkroniser             |
| Script File          | Scriptfil               |
| Scheduled Task       | Planlagt opgave         |

---

## 🧾 Guided by:
🛸 **Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
🇩🇰 **Kasper Madsen** — a joyful Danish Azure Security Specialist who turns labs into friendly journeys  
🇪🇸 **Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity  
✍️ **Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen  

🔎 See full character bios in the README file.

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
