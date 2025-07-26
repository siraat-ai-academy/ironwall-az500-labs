# 📊 AZ-500 Diagram + Friendly Breakdown  
**Lab 10: Deploy a Windows VM using an ARM Template**

---

## 🖼️ Azure Resources – Text-Based Diagram

```
+--------------------------+
|  Resource Group          |
|  RG-NordicInfra          |
+--------------------------+
             |
             v
+--------------------------+     +-------------------------+
|  Storage Account         |<--->|  Diagnostics            |
|  NordicStorageARM        |     +-------------------------+
+--------------------------+
             |
             v
+--------------------------+
|  Virtual Network (VNet)  |
|  NordicVNet              |
+--------------------------+
             |
             v
+--------------------------+
|  Subnet                  |
|  WebSubnet01             |
+--------------------------+
             |
             v
+--------------------------+
|  Network Security Group  |
|  NSG-NordicSecure        |
+--------------------------+
             |
             v
+--------------------------+
|  Network Interface Card  |
|  NIC-NordicVMNet         |
+--------------------------+
             |
             v
+--------------------------+
|  Public IP Address       |
|  PIP-NordicHost          |
+--------------------------+
             |
             v
+--------------------------+
|  Virtual Machine         |
|  VM-KasperWin            |
+--------------------------+
```

---

## 🎭 Diagram Explained — Over Coffee ☕

**Kasper** (laughing): “Alright, eks2, let me break this down like IKEA furniture — except this time, it actually makes sense!”

### 🧱 **Resource Group**
**Kasper**: “Think of this as a big moving box [📦]. Everything you need — VM, network, IP, storage — goes inside this box. We call it a **Resource Group** — or *Ressourcegruppe* in Danish.”

**Sofia**: “Yes, and when it’s time to clean up, you delete the box, and everything inside goes with it. Much safer and cleaner!”

**Mr. eks2**: “So it’s like a drawer that contains all my gadgets for this lab... I like that.”

---

### 💾 **Storage Account**
**Kasper**: “This is like your VM’s photo album. It stores logs, diagnostics, and sometimes your future backups — in a service called **Storage Account**.”

**Sofia**: “And always ensure secure access! You can use shared access signatures or restrict network access.”

**Mr. eks2**: “So even cloud photos need protection, huh?”

---

### 🌐 **Virtual Network (VNet)**
**Kasper**: “This is your VM’s invisible neighborhood. It keeps traffic flowing only where it should. We call it a **Virtual Network**.”

**Sofia**: “And we segment traffic with subnets to keep things tidy and secure.”

**Mr. eks2**: “So it’s like splitting the apartment building into safe hallways?”

---

### 🚧 **Network Security Group (NSG)**
**Kasper**: “Ah, the friendly bouncer of the network! Only lets the right people in — blocks everyone else.”

**Sofia**: “And it's very important to restrict inbound ports, especially RDP. You don’t want everyone knocking on your VM’s door.”

**Mr. eks2**: “Even digital bouncers wear blue in Azure, eh?”

---

### 🖥️ **Virtual Machine**
**Kasper**: “Finally, our guest of honor: the **Virtual Machine**. It’s like a remote Windows PC sitting in the sky, ready to work.”

**Sofia**: “We used an **ARM Template** to deploy it — that’s infrastructure as code. Great for automation, auditability, and consistency.”

**Mr. eks2**: “Feels like magic. But instead of a wand, we typed a JSON spell!”

---

## 🌍 Final Takeaway

This lab shows how multiple Azure building blocks — from networks to storage to compute — come together smoothly using an **ARM template**. It’s a powerful, secure way to deploy full environments with one command.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word           |
|------------------------|------------------------|
| Resource Group         | Ressourcegruppe        |
| Virtual Machine        | Virtuel Maskine        |
| Storage Account        | Lagerkonto             |
| Network Security Group | Netværkssikkerhedsgruppe |
| Virtual Network        | Virtuelt netværk       |
| Subnet                 | Undernet               |
| Public IP              | Offentlig IP           |
| Network Interface      | Netværksgrænseflade    |
| Deployment             | Udrulning              |
| ARM Template           | ARM-skabelon           |

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
