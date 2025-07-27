# 🗺️ AZ-500 Diagram + Friendly Breakdown  
**Lab 16: Understand Network Security Group Rules**

---

## 📊 Text-Based Diagram

```text
+-------------------------+
|  Resource Group         |
|  NordicFortress-RG      |
+-----------+-------------+
            |
            v
+-------------------------+
|  Virtual Machine        |
|  NordicVault-VM01       |
|  Windows Server (IIS)   |
+-----------+-------------+
            |
            v
+-------------------------+
|  Network Security Group |
|  NSG-NordicShield       |
+-----------+-------------+
     |                     |
     v                     v
[RDP Port 3389]       [HTTP Port 80]
   (Inbound)             (Inbound)

            |
            v
+-------------------------+
|  Public IP Address      |
|  (VM accessible from    |
|   browser or RDP tool)  |
+-------------------------+
```

---

## 🎭 Diagram Walkthrough: Azure with a Smile

### ☕ Scene: Azure Café – Afternoon Reflections

**Mr. Eks2** was sipping elderflower tea while staring at the whiteboard. “Okay… I clicked so many things… but how do they all connect?”

**🇩🇰 Kasper Madsen** leaned in, smiling. “Let me draw it for you, Eks2. Think of it as building a digital cottage in the sky.”

---

### 🧱 **Resource Group**

**Kasper**: “Start with your **Resource Group** — or *ressourcegruppe*. It’s like a basket that holds all your cloud tools. If it’s not in the basket, it’s probably in the laundry.”

**Sofia**: “Organizing your resources into groups is key for clean billing and easier deletion. Always label wisely!”

**Eks2**: “So if I delete the basket… everything inside goes too?”  
**Sofia**: “Exactly. No cloud clutter!”

---

### 🖥️ **Virtual Machine (VM)**

**Kasper**: “Next, we created the **Virtual Machine** — our sky-cottage. It’s a Windows Server with IIS, which means it can serve web pages like a bakery serves hot bread.”

**Sofia**: “Be mindful: VMs are like unlocked doors when misconfigured. That’s why we don’t open all ports.”

**Eks2**: “So this VM is running a website *and* I can remote into it?”

**Kasper**: “Yes, just don’t leave the RDP door wide open for strangers.”

---

### 🛡️ **Network Security Group (NSG)**

**Kasper**: “Now comes the moat — the **Network Security Group**. It guards your castle. No one gets in unless we say so.”

**Sofia**: “We allowed **Port 3389** (RDP) for remote desktop and **Port 80** (HTTP) to view the website. But we set them carefully, with priorities and names.”

**Eks2**: “So every open port is a potential risk?”  
**Kasper** *(whispers)*: “Every open port… is a forgotten prayer.”

---

### 🌐 **Public IP Address**

**Kasper**: “Last but not least, the **Public IP** — your VM’s address in the sky. Like writing ‘Come visit!’ on your mailbox.”

**Sofia**: “It lets users visit your site. But don’t keep it public forever. Turn it off when you don’t need it.”

**Eks2**: “So... if I give someone the IP and open the right port, they can visit my VM?”  
**Kasper**: “Yes, just like a digital guesthouse.”

---

## 🧠 Final Takeaway

This diagram shows how Azure pieces fit like Lego blocks: secure, organized, and modular. From the **Resource Group** to the **NSG**, each piece plays a role in guarding and delivering services in the cloud. It’s not just about making things work — it’s about making them **secure** and **intentional**.

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

A 158-year-old company collapsed because of a single exposed password. No firewall. No alerts. No limits. It was a digital tragedy — avoidable.  

In this lab, we learned to set **NSG rules**, use **only needed ports**, and guard access with intention. These small actions can prevent major catastrophes.  
📎 [Read the BBC Story](https://www.bbc.com/news/articles/cx2gx28815wo)

---

## 🧾 Guided by:

🛸 **Mr. Eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
🇩🇰 **Kasper Madsen** — a timeless cyber-sufi — a guardian of digital wisdom across centuries.  
🇪🇸 **Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity.  
✍️ **Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen.


**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
