# 🧪 Lab 9: Connect SMB Azure File Share to Windows VM

## 📌 Lab Title  
**Create an SMB Azure file share and connect it to a Windows VM**

---

## 🔮 Scenario Setup  

Mr. eks2 arrived with a fresh cup of chamomile tea ☕ and a spark of curiosity in his eyes.  

Kasper waved from across the desk.  
**Kasper:** “Today, we’re going to make a shared folder in the cloud... and then link it to a Windows computer in the sky. Sounds like sci-fi? It’s just Azure!”  

**Sofia:** “Yes, and we’ll practice snapshots too. Think of them like time-travel saves for your files.”  

Mr. eks2 smiled, “Oh! Like bookmarks for the past... I’m in.”

---

## 🛠️ Step-by-Step with Friendly Dialogue

### 🧱 Step 1: Create a Storage Account  

**Kasper:** “Think of the **Storage Account** as your digital warehouse 🏢. All your files, blobs, and secrets rest here.”  

**Sofia:** “And we selected **Locally Redundant Storage (LRS)** — this keeps your data safe inside one data center. A solid start.”  

**Mr. eks2:** “And this warehouse lives in East US? That’s... far from Copenhagen.”  

---

### 📁 Step 2: Create a File Share  

**Kasper:** “Inside our warehouse, we made a shelf called **qsfileshare**. Azure File Shares are like those office shared drives – except floating in the cloud.”  

**Sofia:** “Don’t forget: we disabled backup here to keep things simple for testing. But in real life, always plan backup.”  

**Mr. eks2:** “Okay... a floating shelf. I like this.”

---

### 📤 Step 3: Upload a File  

**Kasper:** “We uploaded a simple text file — **qsTestFile.txt**. It’s like putting your very first note into your new cloud drawer.”  

**Sofia:** “Uploading files directly from the portal is handy for testing. For automation, use scripts or tools later.”  

**Mr. eks2:** “First note saved. It feels official!”

---

### 🖥️ Step 4: Deploy a Virtual Machine  

**Kasper:** “Now let’s create a **Virtual Machine** — a computer in the cloud. Ours is running **Windows Server 2019**.”  

**Sofia:** “We kept it small and simple: **Standard B2s** with **Standard SSD** disk. Just right for testing.”  

**Mr. eks2:** “Is this my cloud desktop now?”  

---

### 🔌 Step 5: Connect to the VM  

**Kasper:** “We use **RDP (Remote Desktop Protocol)** to log in. Like teleporting into your virtual office.”  

**Sofia:** “And remember to accept the certificate warning – it’s expected during test environments.”  

**Mr. eks2:** “Teleportation successful. This VM is cozy.”

---

### 🔗 Step 6: Map File Share to VM  

**Kasper:** “This is where magic happens! We ran a **PowerShell** script from Azure to connect the file share to the VM. It appears like a new drive – like G: or Z:.”  

**Sofia:** “This makes Azure File Shares feel like local drives. Very useful for migration or hybrid work.”  

**Mr. eks2:** “A cloud drive... connected like a USB. Nice!”

---

### ⏱️ Step 7: Create a Share Snapshot  

**Kasper:** “We took a **snapshot** – a little time capsule of the file. Then we edited the file and took another one.”  

**Sofia:** “Snapshots don’t cost much, and they help during accidental deletion or ransomware recovery.”  

**Mr. eks2:** “Time travel for text files. I like this part.”

---

### 🔍 Step 8–12: Browse, Restore, Delete, and View Versions  

**Kasper:** “We peeked into old snapshots, **restored** the file, and even checked **Previous Versions** from the VM side.”  

**Sofia:** “Using both snapshot restore and Windows’ Previous Versions is great for layered recovery.”  

**Mr. eks2:** “I restored a file like a pro. Can we do this for coffee too?”

---

## 🌍 Real-World Reflection  

This lab teaches how **Azure File Shares** can support hybrid environments. Whether it’s moving file servers to the cloud, backing up shared folders, or creating fast disaster recovery, you now know how to connect, snapshot, and restore. A key skill for modern IT security and cloud jobs!

---

## 📘 Bonus: Learn 10 Danish Tech Words  

| English Term         | Danish Word           |
|----------------------|------------------------|
| Storage Account      | Lagerkonto             |
| File Share           | Fildeling              |
| Virtual Machine      | Virtuel Maskine        |
| Snapshot             | Øjebliksbillede        |
| Resource Group       | Ressourcegruppe        |
| Disk                 | Disk                   |
| PowerShell           | PowerShell             |
| Backup               | Sikkerhedskopi         |
| File Explorer        | Stifinder              |
| Drive Letter         | Drevbogstav            |

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
