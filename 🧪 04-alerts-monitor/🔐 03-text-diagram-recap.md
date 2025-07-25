# 🔷 AZ-500 Diagram + Friendly Breakdown  
**Lab 4: Working with Alerts**

---

## 🖼️ Azure Architecture Diagram (Text-Based)

```
+-----------------------+
|   Resource Group      |
|  NordicInfra-RG       |
+----------+------------+
           |
           v
+----------+------------+
|  Virtual Machine       |
|  NordicVault-VM        |
|  (Windows Server 2022) |
+----------+------------+
           |
           v
+--------------------------+
|      Azure Alerts        |
| - Monitors Admin Ops     |
+----------+---------------+
           |
           v
+--------------------------+
|      Action Group        |
|  NordicAlertGroup        |
| - Sends Email to eks2    |
+--------------------------+
```

---

## ☕ Let’s Talk Through It – Over Coffee with Kasper & Sofia

### 🧑‍💼 Mr. eks2:  
“That diagram looks nice! But what exactly is going on here?”

---

### 🇩🇰 Kasper:  
“Great question! At the top, we’ve got our **Resource Group** — think of it like a digital folder (or a ‘ressourcegruppe’) where all your Azure stuff lives. In this case, we called it **NordicInfra-RG**.”

### 🇪🇸 Sofia:  
“And keeping resources grouped helps with security and budgeting. You can apply access controls to the whole group.”

### 🧑‍💼 Mr. eks2:  
“Ah! So instead of 10 sticky notes, we just use one clean folder.”

---

### 🇩🇰 Kasper:  
“Next, we’ve got the **Virtual Machine** — it’s our little computer in the cloud, named **NordicVault-VM**. We installed Windows Server on it, but it could run anything really.”

### 🇪🇸 Sofia:  
“Always make sure access is restricted. No public ports, no guessing passwords. Just tight control.”

### 🧑‍💼 Mr. eks2:  
“It’s like a secret laptop floating over the East US… spooky but cool.”

---

### 🇩🇰 Kasper:  
“Below that is the real magic — **Azure Alerts**! It watches the logs and says, ‘Psst! Someone restarted the VM!’ We told it to watch **Administrative operations**.”

### 🇪🇸 Sofia:  
“That’s a very common and smart move. Alerts reduce risk by keeping you informed in real time.”

### 🧑‍💼 Mr. eks2:  
“So it’s a cloud whisperer! When it senses trouble, it tells me.”

---

### 🇩🇰 Kasper:  
“Last but not least: the **Action Group**. That’s where you say *how* you want to be notified. We said, ‘Send an email to eks2!’ — And Azure listens.”

### 🇪🇸 Sofia:  
“In real life, you can also send texts, voice calls, even trigger automated scripts.”

### 🧑‍💼 Mr. eks2:  
“Nice! Now I won’t miss a cloud sneeze again.”

---

## 🌍 Final Takeaway

This diagram shows how Azure resources work together like a well-trained team. Your **VM** is your worker, your **Alerts** are the observers, and the **Action Group** is the messenger. It’s all stored inside your **Resource Group**. You’ve now seen how Azure helps security teams catch changes fast — and stay in control.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word           |
|------------------------|-----------------------|
| Resource Group         | Ressourcegruppe       |
| Virtual Machine        | Virtuel Maskine       |
| Alert                  | Varsel                |
| Action Group           | Handlingsgruppe       |
| Email Notification     | E-mailnotifikation     |
| Monitoring             | Overvågning           |
| Admin Operations       | Administrative handling |
| Restart                | Genstart              |
| Scope                  | Omfang                |
| Disk                   | Lagerdisk             |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
