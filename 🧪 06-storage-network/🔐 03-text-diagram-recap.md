# 🌐 AZ-500 Diagram + Friendly Breakdown  
**Lab 6: Network Access to Storage Accounts**

---

## 🖼️ Text-Based Diagram

```
+------------------------+
|   Resource Group       |
|   NordicTech-RG        |
+----------+-------------+
           |
           v
+------------------------+
|   Virtual Network      |
|   vnet-DKSecure-west1  |
+----------+-------------+
           |
           v
+---------------------+         +---------------------------+
|     Subnet          |         |     Storage Account       |
|  subnet-NordicApp   |-------->|  nordicvaultstore001      |
+----------+----------+         +------------+--------------+
           |                                 |
           |                                 v
           |                         +----------------------+
           |                         |  Private Endpoint     |
           |                         |  pe-nordicblob01      |
           |                         +----------------------+
           |
           v
+------------------------+
|   Virtual Machine       |
|   VM-DKAccessNode       |
+------------------------+
           |
           v
+------------------------+
| Azure Storage Explorer |
|   (Connected via Key)  |
+------------------------+
```

---

## 🎭 Diagram Explanation – Friendly Dialogue Format

### 🧺 Step 1: **Resource Group** is the Backpack

**Kasper**: “Everything starts in a **Resource Group** — or as we say, *ressourcegruppe*. It’s your digital backpack. All your cloud stuff goes inside!”

**Sofia**: “It’s important for management and cleanup. You delete the group, you clean the whole lab.”

**Mr. eks2**: “I like the backpack analogy. I’m going to zip this one up nicely.”

---

### 🌍 Step 2: **Virtual Network** + **Subnet** = Your Neighborhood

**Kasper**: “Think of the **Virtual Network** as your cloud city — and the **Subnet** as the peaceful street where all the houses live.”

**Sofia**: “Security-wise, having a subnet helps separate roles and control traffic. It’s good practice to keep things tidy.”

**Mr. eks2**: “So I’m building my cloud neighborhood — with no strangers allowed.”

---

### 🔒 Step 3: **Storage Account** with **Private Endpoint**

**Kasper**: “This is your digital vault — the **Storage Account** — and the **Private Endpoint** is like a secret tunnel leading into it.”

**Sofia**: “Exactly. No public access. It connects through the private network only. That’s strong Azure hygiene!”

**Mr. eks2**: “So… my data travels underground, like a ninja. I love that.”

---

### 🏠 Step 4: **Virtual Machine** in the Subnet

**Kasper**: “Your **Virtual Machine** is like your little house inside the subnet. We use it to access the vault — but safely.”

**Sofia**: “Always lock the front door — allow only what you need. In our case, RDP was okay for the lab.”

**Mr. eks2**: “One house, one safe tunnel, no street noise. I feel like a cloud monk.”

---

### 🔑 Step 5: Use **Storage Explorer** with **Access Key**

**Kasper**: “Then we used **Azure Storage Explorer** — kind of like a cloud window — to peek into the vault using the **connection string**.”

**Sofia**: “Just remember — those **Access Keys** are precious. Don’t share them or leave them in open files.”

**Mr. eks2**: “Keys to the kingdom… I’ll keep mine hidden in my digital sock drawer.”

---

## 🌍 Final Takeaway

This diagram shows how to safely access storage in Azure using **private paths**, not the internet. You build a **Virtual Network**, add a **Subnet**, connect a **Storage Account** using a **Private Endpoint**, and access it from a **Virtual Machine** — safely and securely. This is a big step toward real-world cloud security.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word           |
|----------------------|------------------------|
| Resource Group       | Ressourcegruppe        |
| Storage Account      | Lagerkonto             |
| Virtual Network      | Virtuelt netværk       |
| Private Endpoint     | Privat endepunkt       |
| Virtual Machine      | Virtuel maskine        |
| Subnet               | Undernetværk           |
| IP Address           | IP-adresse             |
| Blob                 | Blob                   |
| Access Key           | Adgangsnøgle           |
| Region               | Område                 |

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
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of eks2 — the whisper behind the work._  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
