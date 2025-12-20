## 🔒 Microsoft Azure — Understanding Resource Locks  
### AZ-104 & AZ-500 Certification Lab

# 📊 AZ-500 Diagram + Friendly Breakdown  
_Lab: Create a VM and Add Resource Locks (Lab 01)_

---

## 🖼️ Text-Based Azure Diagram

```
+------------------------+
|   Resource Group       |
|   NordicVault-Group    |
+-----------+------------+
            |
            v
+------------------------+
|  Virtual Machine       |
|  NordicVault-VM        |
|  Ubuntu Server         |
+-----------+------------+
            |
            v
+------------------------+
|     OS Disk (SSD)      |
|  Standard, LRS Backup  |
+------------------------+

            |
            v
+----------------------------+
| 🔐 Resource Locks           |
+----------------------------+
| VMDeleteLock (Delete Lock)|
| RGReadOnly (Read-only)    |
+----------------------------+
```

---

## 🎭 Diagram Walkthrough — Told Like a Story

### 🧑‍🏫 Kasper Explains:

“Okay, eks2, picture this like a little castle setup in the cloud!

At the top, we have the **Resource Group** — like a folder or box where you keep all your cloud stuff together. Ours is called **NordicVault-Group** — very secure, very Danish 🇩🇰.

Inside this group, we place our mighty **Virtual Machine** — named **NordicVault-VM**. It’s like your own private computer in the sky, running **Ubuntu Server**."

---

### 🔒 Sofia Adds:

“We added locks! A **Delete Lock** on the VM — so no one can delete it by accident. And a **Read-only Lock** on the whole **Resource Group**. These are our digital seatbelts.”

---

### 🤔 Mr. eks2 Reflects:

“So the **Virtual Machine** lives inside the **Resource Group**… and then we locked both! Like putting a bike in a garage and locking both the bike and the garage door?”

---

## 💡 Final Takeaway

This simple diagram teaches us how Azure resources are **grouped**, **protected**, and **structured**. By using **resource locks**, even beginners can set up a strong defense against accidental changes or deletions. It's not just cloud computing — it’s cloud safety.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word            |
|------------------------|------------------------|
| Resource Group         | Ressourcegruppe        |
| Virtual Machine        | Virtuel Maskine        |
| Storage Account        | Lagerkonto             |
| Lock                   | Lås                    |
| Delete                 | Slet                   |
| Read-only              | Kun læsbar             |
| Disk                   | Disk                   |
| Password               | Adgangskode            |
| Username               | Brugernavn             |
| Size                   | Størrelse              |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
