# 🌐 Lab 21: Dancing with Firewalls — Protecting the Nordic Way 🔥

> **IronWall-az500-labs** | Story Edition 🌸✨  
> _Guided by Mr. Eks2 and friends — for learners, dreamers, and gentle defenders of the cloud._  

---

## 🌅 Arrival at the Lab: A Firewall Awakening

The mist was still rising over **Copenhagen’s azure hills**, when **Mr. Eks2** arrived early at the academy’s cloud garden — a peaceful place where ideas breathe freely. He had heard whispers of fire — not one that burns, but one that protects.

“Godmorgen!” smiled **Kasper Madsen**, stepping out from the Azure lounge with a steaming mug of coffee.

“Today,” he said, “you’ll learn how to build a real **Azure Firewall** — not just with clicks and IPs, but with care, clarity, and calm.”

From the olive-gold corridor, **Sofia Zaymera** appeared like a sunbeam. Her eyes kind, her words warm. “Firewalls are not blockades,” she whispered. “They’re boundaries made with wisdom.”

And with that — our lab began.

---

## 🛡️ What You’ll Learn
> 📖 **This lab helps you** understand how to:
- Build a **Virtual Network** with segmented **subnets**
- Deploy **Virtual Machines** behind secure layers
- Configure **Azure Firewall** policies (Application, Network, DNAT)
- Direct traffic with **Route Tables**
- Test, tweak, and trust your setup

This is the heart of modern cloud security 💙 — learning to **let the right things in, and keep the wrong ones out**.

---

## 🧩 Step 1: Weaving the Virtual Network

**Kasper** led the way with cheerful energy. “Think of this as laying the roads and neighborhoods of a little Azure city.”

🛠️ Create a **Virtual Network** with these subnets:
- **AzureFirewallSubnet** – `10.0.1.0`
- **Workload-SN** – `10.0.2.0/24`
- **Jump-SN** – `10.0.3.0`
- **AzureFirewallManagementSubnet** – `10.0.4.0`

🪄 Tip from **Sofia**: “Subnets are sacred spaces — isolate wisely. Especially **AzureFirewallSubnet**, it must be named exactly or the firewall won’t see it.”

**Mr. Eks2** looked thoughtfully: “Each subnet feels like a chamber of trust. We don’t let everyone into every room — and that’s okay.”

---

## 🖥️ Step 2: Planting the Servers

We now bring two VMs into our network. One will act like a secure gateway, the other a protected workload.

### 🧭 First VM — The **Jump Server**:
- Name: **NordicJump**
- Subnet: **Jump-SN**
- Allow RDP

### 🧭 Second VM — The **Workload Server**:
- Name: **NordicWork**
- Subnet: **Workload-SN**
- No public IP

**Kasper** smiled: “You see, **NordicJump** is like a doorbell — it lets you enter safely. But **NordicWork**? It hides. It trusts no public light.”

**Mr. Eks2** asked: “Why use two?”

**Sofia**: “Because access is like intimacy — it must be earned, never default.”

---

## 🔥 Step 3: The Azure Firewall Rises

> Now comes the guardian.

Set up your **Azure Firewall** like this:
- Name: **NordicShield-FW**
- Region: **West Europe**
- SKU: **Basic**
- Add new **Firewall Policy**: `NordicPolicy-Basic`
- Attach to the earlier **Virtual Network**
- Create public & management IPs

**Elina Petrova** joined from the scripting sanctum. “Automation’s lovely, but today — we click. One step, one breath.”

**Mr. Eks2** nodded. “It feels less like configuration, more like consecration.”

---

## 🧭 Step 4: Guiding the Traffic — The Route Table

“Imagine cars without signs,” **Kasper** chuckled. “Chaos! That’s why we build **Route Tables**.”

🚗 Add route:
- Name: **Route-To-Firewall**
- Destination: `0.0.0.0/0`
- Next hop: **Virtual Appliance**
- Address: **Firewall Private IP**

Then associate this table with **Workload-SN**.

**Sofia**: “With routes, we tell every packet — ‘Speak to the firewall first.’”

**Mr. Eks2**: “So even silence has a gatekeeper.”

---

## 🌐 Step 5: Allowing the Right Apps

Inside your **Firewall Policy**, add an **Application Rule**:

📜 Rule:  
- Name: `AllowWeb`  
- Source: `10.0.2.0/24` (Workload subnet)  
- Protocols: **http**, **https**  
- Destination: `www.google.com`  

**Inky Rihan** appeared quietly from the Red Team window.

“Control is beautiful,” he said, “when it’s *precise*. Let what you *trust* in. Nothing more.”

---

## 🔗 Step 6: Let DNS Breathe

🧠 Add a **Network Rule** for **DNS** access:
- Source: `10.0.2.0/24`
- Protocol: **UDP**
- Port: `53`
- Destination: `209.244.0.3`, `209.244.0.4`

**Sofia** whispered, “Without DNS, your servers won’t find their way.”

**Mr. Eks2** asked: “It’s like giving them a map?”

**Sofia**: “Yes, a gentle map — only to the roads you draw.”

---

## 🧩 Step 7: The DNAT Bridge

Create a **DNAT Rule** so you can RDP into **NordicWork** via firewall.

- Protocol: **TCP**
- Port: `3389`
- Destination IP: **Firewall Public IP**
- Translated Address: **Private IP of NordicWork**

**Kasper**: “It’s like whispering through a firewall crack — only you know the words.”

**Inky** nodded. “But even whispers can be heard — always guard them.”

---

## 🧠 Step 8: Set DNS Manually for Workload VM

Inside **NordicWork**, go to its **Network Interface** and set **DNS Servers**:
- `209.244.0.3`
- `209.244.0.4`

Then restart.

**Elina**: “Every config tells a story. DNS isn’t just a number — it’s who your VM trusts to speak names into numbers.”

---

## 🔍 Step 9: Test with a Gentle Touch

Connect to **NordicJump** via RDP → then from there, connect to **NordicWork**.

Disable **IE Enhanced Security**.

Try accessing:
- 🌍 `www.google.com` ✅
- 🛑 `www.microsoft.com` ❌

**Maya Lin**, the security rookie, clapped with delight.

“It works! The rules work!” she beamed.

**Isabella Konti** placed a gentle hand on her shoulder. “And so does your learning, Maya. Little by little — you are becoming a protector.”

---

## 🧹 Clean-Up

Delete all resources to avoid extra cost — but keep the memory.

> “Clouds must clear, so sunlight returns.” – **I.K.**

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In a world echoing with cyber threats, even the smallest configuration can be your strongest defense. This lab — through **application rules**, **route tables**, and **DNS control** — shows us that boundaries matter.

Much like the tragic fall of a 158-year-old UK firm due to one compromised password, [as told by the BBC](https://www.bbc.com/news/articles/cx2gx28815wo), **one unchecked port, one misrouted packet**, can collapse a legacy.

Let this lab remind us — **cybersecurity is care**.

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_

