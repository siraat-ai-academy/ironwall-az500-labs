
# 📊 AZ-500 Diagram + Friendly Breakdown
### Lab 15: Implementing Virtual Network Peering

---

## 🖼️ Text-Based Diagram: Azure Virtual Network Peering

```
+---------------------------+         +----------------------------+
|    Resource Group         |         |    Resource Group          |
|    DKInfra-RG             |         |    DKInfra-RG              |
+---------------------------+         +----------------------------+
           |                                      |
           v                                      v
+---------------------------+         +----------------------------+
|   Virtual Network:        |         |   Virtual Network:         |
|   NordNet-1 (10.1.0.0/16) |<------->|   NordNet-2 (10.2.0.0/16)  |
+---------------------------+         +----------------------------+
           |                                      |
           v                                      v
+------------------------+         +------------------------+
| Subnet-A (10.1.0.0/24) |         | Subnet-B (10.2.0.0/24) |
+------------------------+         +------------------------+
           |                                      |
           v                                      v
+------------------------+         +------------------------+
|  VM: NordicVault-VM1   |         |  VM: NordicVault-VM2   |
|  Public RDP Enabled    |         |  Private Only          |
+------------------------+         +------------------------+
           |
           v
    PowerShell: Allow Ping
           |
           v
Remote Desktop --> [ Internal IP: VM2 ]
```

---

## 🎭 Diagram Walkthrough with Kasper, Sofia & Mr. eks2

**Mr. eks2**: “Whoa... that looks like two tiny cities with a secret bridge!” 🏙️🌉

### 🔹 Kasper: “That’s exactly it!”

**Kasper**: “Imagine **DKInfra-RG** as our big filing cabinet 🗂️, and inside it, we’ve got two separate city blocks — **NordNet-1** and **NordNet-2**. They live far apart, but we connected them with a magical cloud tunnel called **VNet Peering**.”

**Sofia**: “And it’s private! No internet involved. Just a direct line between two friends. Safer, quieter, and faster.”

**Mr. eks2**: “So it’s like two clubs with a VIP-only hallway between them?”

**Kasper**: “Spot on! Just remember your club pass.”

---

### 🧱 Sofia: “Let’s talk about Subnets!”

**Sofia**: “Within each **Virtual Network**, we created **Subnets** — like neighborhoods within our cities. **Subnet-A** and **Subnet-B** are where we place our servers — the **Virtual Machines**.”

**Kasper**: “Think of these like cloud apartments — VM1 lives in block A, VM2 in block B. But they don’t know each other unless you introduce them.”

**Mr. eks2**: “So VM1 and VM2 can wave to each other because of peering?”

**Kasper**: “Exactly, if you also unlock the right window!”

---

### 💻 Sofia: “Now, meet the VMs.”

**Sofia**: “**NordicVault-VM1** is friendly — we gave it public **RDP access** (just for now). But **NordicVault-VM2** is private, no outside entry.”

**Kasper**: “It’s like one has a doorbell and mailbox, and the other is just... hiding in a bunker.” 😄

**Mr. eks2**: “That bunker VM… it’s safe, right?”

**Sofia**: “Very. That’s good cloud hygiene.”

---

### 🔐 Kasper: “Don’t forget Firewall Rules!”

**Kasper**: “To let VM1 reach VM2, we used **PowerShell** to unlock a tiny window — allowing ping with `Allow ICMPv4-In`. Just one little rule.”

**Sofia**: “Be careful: only open what’s needed. Each open rule is like a door. Keep them few, and locked when not needed.”

**Mr. eks2**: “So… ping is like knocking to say hi?”

**Kasper**: “Yes. If VM2 replies, it means the handshake worked.” 👋

---

## 🌍 Final Takeaway

This diagram shows how Azure resources are built like little cities with zones, tunnels, and buildings. You decide who can visit, who can connect, and who stays hidden. Mastering these layouts means you're learning to architect secure environments — one subnet at a time.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word          |
|----------------------|----------------------|
| Resource Group       | Ressourcegruppe      |
| Virtual Network      | Virtuelt netværk     |
| Subnet               | Undernetværk         |
| Virtual Machine      | Virtuel maskine      |
| Firewall Rule        | Firewall-regel       |
| Peering              | Sammenkobling        |
| IP Address           | IP-adresse           |
| Region               | Region               |
| PowerShell           | PowerShell           |
| Remote Desktop (RDP) | Fjernskrivebord      |

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

It’s easy to think these are just tiny setups in a test lab. But this diagram represents a **secure structure** — where each VM, each subnet, and each connection is managed and protected.

When one weak password destroyed a 158-year-old company (yes, it really happened — [read it here](https://www.bbc.com/news/articles/cx2gx28815wo)), it wasn’t because the tech was bad. It was because the structure wasn’t protected.

What you build today — matters. A single firewall rule or subnet design could be what saves your future company.

---

### 🧾 Guided by:

🛸 **Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
**🇩🇰 Kasper Madsen** — a joyful Danish Azure Security Specialist who turns labs into friendly journeys  
**🇪🇸 Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity  
**✍️ Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
