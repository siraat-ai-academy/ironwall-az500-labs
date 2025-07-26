# 🧩 AZ-500 Diagram + Friendly Breakdown  
## Lab 11: Create a VM with CLI (Command Line Interface)

---

## 🖼️ Text-Based Diagram (ASCII Style)

```plaintext
+------------------+
|  Resource Group  |
|  DKSec-CLI-RG    |
+------------------+
         |
         v
+------------------+
| Virtual Machine  |
|  NordicCLI-VM    |
+------------------+
         |
         v
+-------------------------+
| Network Interface (NIC)|
|  NordicCLI-NIC         |
+-------------------------+
         |
         v
+--------------------------+
| Network Security Group  |
|  NordicCLI-NSG          |
+--------------------------+
         |
         v
+----------------------+
|  Virtual Network     |
|  NordicCLI-VNet      |
+----------------------+
         |
         v
+----------------------+
|  Public IP Address   |
|  NordicCLI-PublicIP  |
+----------------------+
```

---

## 🎭 Diagram Walkthrough — Coffee Time with Kasper, Sofia & Mr. eks2

**Mr. eks2** *(sipping coffee)*: “This lab was so fast! But Kasper, what just happened behind the scenes when I ran that one command?”

### 🔹 1. **Resource Group**
**Kasper**: “Ah! Imagine this as a labeled box 📦 in your cloud attic. You throw all your cloud items into it — and when it’s time to clean, you delete the box instead of hunting for socks everywhere.”

**Sofia**: “Yes, and in real life, naming your **Resource Group** [ressourcegruppe] clearly helps manage budgets and access rules.”

**Mr. eks2**: “So... it’s like my ‘project folder’ in Azure?”

---

### 🔹 2. **Virtual Machine**
**Kasper**: “Meet **NordicCLI-VM** — your cloud computer in the sky ☁️. It runs Windows Server 2019 and loves to receive commands!”

**Sofia**: “Don’t forget to choose strong credentials. And limit who can RDP into it — that’s a security gateway.”

**Mr. eks2**: “Feels like I spun up a computer without plugging in any wires.”

---

### 🔹 3. **Network Interface (NIC)**
**Kasper**: “This is the network plug — it connects your VM to the world 🌍. No NIC, no internet!”

**Sofia**: “And every NIC should be connected to the right **Network Security Group** — think of it as a smart firewall.”

**Mr. eks2**: “Ahh… like the network cable in my old server room.”

---

### 🔹 4. **Network Security Group (NSG)**
**Kasper**: “This is your friendly bouncer at the digital door. It checks who’s allowed in and who’s politely told ‘not today, sir.’”

**Sofia**: “NSGs let you allow or block traffic using rules. Always use the least privilege approach.”

**Mr. eks2**: “So RDP was allowed just for testing?”

---

### 🔹 5. **Virtual Network (VNet)**
**Kasper**: “Think of this as your private neighborhood. All your cloud machines live here — they can talk to each other quietly.”

**Sofia**: “Yes, and you can set up subnets for even better isolation.”

**Mr. eks2**: “Like the Danish streets with polite fences!”

---

### 🔹 6. **Public IP**
**Kasper**: “That’s the address you share with the world when you say ‘connect to me!’ But it’s best to only use it when needed.”

**Sofia**: “Use **Just-in-Time access** or Bastion for safer VM access in the future.”

**Mr. eks2**: “Makes sense… my address should not always be public.”

---

## 🌍 Final Takeaway

Even one CLI command in Azure quietly creates multiple building blocks: **Virtual Machine**, **VNet**, **NSG**, **NIC**, **Public IP**, and all wrapped in a nice **Resource Group**. You deployed a tiny cloud datacenter — all from your keyboard!

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word         |
|----------------------|---------------------|
| Resource Group       | Ressourcegruppe     |
| Virtual Machine      | Virtuel Maskine     |
| Public IP Address    | Offentlig IP-adresse|
| Network Interface    | Netværksgrænseflade |
| Network Security Group | Netværkssikkerhedsgruppe |
| Virtual Network      | Virtuelt netværk    |
| CLI                  | Kommandolinje       |
| Cloud Shell          | Skykonsol           |
| Deployment           | Implementering      |
| Admin Username       | Adminbrugernavn     |

---

### 🧾 Guided by:
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
