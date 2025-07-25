# 📊 AZ-500 Diagram + Friendly Breakdown  
_Lab 2: Resource Tags & Organization in Azure_

---

## 🖼️ Text-Based Azure Diagram

```
+-----------------------------+
|      Resource Group         |
|     DKCloudLab-RG           |
+-------------+---------------+
              |
              v
+-----------------------------+
|     Virtual Machine         |
|        DKResize-VM          |
|     Windows Server 2019     |
+-------------+---------------+
              |
              v
+-----------------------------+
|           Disk              |
|     Standard SSD (OS)       |
+-----------------------------+
              |
              v
+-----------------------------+
|           Tag               |
|   Name: Department          |
|   Value: IT                 |
+-----------------------------+
              |
              v
+-----------------------------+
|         Filter              |
|  Shows only Department=IT   |
+-----------------------------+
```

---

## 🎭 Diagram Walkthrough — Cloud Talk with Kasper, Sofia, and eks2

### 🧑‍🏫 Kasper’s Intro

“Alright eks2, imagine your Azure setup like a digital office filing system — super clean, super clever.”

“At the top, we have a **Resource Group** called **DKCloudLab-RG** — this is like your filing cabinet. Everything goes inside.”

---

### 🖥️ Sofia’s Security Scoop

“Next comes our **Virtual Machine** — like your very own Windows laptop running in the cloud. We used **Windows Server 2019** here.”

“And the **Disk**? That’s your VM’s memory card — a **Standard SSD**. Fast, simple, and affordable.”

---

### 🧑‍🚀 eks2’s Wonder Moment

“So the VM is in a cloud filing cabinet, and the disk is like its internal drive… neat! But where does the ‘tag’ go?”

---

### 🏷️ Kasper Tags It Up

“Ah! The **Tag** is like a digital sticky note. We wrote: ‘**Department: IT**’. Now it knows who it belongs to!”

---

### 🔍 Sofia Adds the Filter

“And with **Filters**, you can search all your Azure stuff by tag. Type ‘Department = IT’ — boom! You see only what you need.”

---

### 🧠 eks2 Reflects

“So tagging is like sorting socks — if you label them, you can find them. And filtering is like looking into a drawer labeled ‘IT only.’ That’s… kind of beautiful.”

---

## 🌍 Final Takeaway

This diagram teaches you how to **group**, **tag**, and **filter** Azure resources. For companies with hundreds of items in the cloud, this structure makes life easier, neater, and more secure. It’s not just for fun — it’s for focus and function.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word            |
|------------------------|------------------------|
| Resource Group         | Ressourcegruppe        |
| Virtual Machine        | Virtuel Maskine        |
| Tag                    | Mærkat                 |
| Filter                 | Filter                 |
| Department             | Afdeling               |
| Value                  | Værdi                  |
| Username               | Brugernavn             |
| Password               | Adgangskode            |
| Create                 | Opret                  |
| Delete                 | Slet                   |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
