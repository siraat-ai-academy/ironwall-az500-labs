
# 🔗 Implementing Virtual Network Peering

## 🔮 Scenario Setup

It was a fresh morning in Copenhagen. ☁️ The sun peeked through the clouds as **Mr. eks2** stepped into the office — excited, notebook in hand, and a warm coffee in the other. Today’s Azure lab was buzzing with curiosity.

“Godmorgen, eks2!” said **Kasper Madsen** with a grin. “Ready to build some bridges in the cloud?”

**Sofia Zaymera**, already setting up her dashboard, smiled. “We’re learning about **Virtual Network Peering** — it's how we let different networks talk to each other, securely and privately.”

“This is like setting up roads between small towns,” Kasper added. “Each **Virtual Network** is a town, and peering is the friendly road that connects them!”

🛸 Mr. eks2 chuckled. “Let’s begin this magical road trip in the cloud.”

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🧱 Step 1: Create the First Virtual Network

**Kasper**: “We’ll start by creating our first town: **NordNet-1**, inside our main **Resource Group** — let’s call it **DKInfra-RG**.”

- Go to **Create a Resource**
- Search **Virtual Network**, click **Create**
- Set **Name** to `NordNet-1`
- Region: **West Europe**
- In **IP Addresses**, set: `10.1.0.0/16`
- Remove the default **subnet**
- Add a new **Subnet**: `Subnet-A`, range: `10.1.0.0/24`

**Sofia**: “Be sure to plan your address ranges carefully. They must not overlap with others.”

**Mr. eks2**: “Subnet... is that like a neighborhood in our town?”

**Sofia**: “Exactly. You're thinking like an engineer already.”

---

### 🧱 Step 2: Create the Second Virtual Network

**Kasper**: “Now we build the second town: **NordNet-2**.”

- Same steps as before
- Name: `NordNet-2`
- Address space: `10.2.0.0/16`
- Add **Subnet-B**: `10.2.0.0/24`

**Sofia**: “Always keep IP ranges separate — it avoids confusion later.”

**Mr. eks2**: “These towns are far apart now. When do we build the road?”

**Kasper**: “Ah, good question! That’s our next step.” 🚗

---

### 🌉 Step 3: Peer the Two Virtual Networks

**Kasper**: “Now we build a **peering** — the secure tunnel between **NordNet-1** and **NordNet-2**.”

- Go to **NordNet-1**
- Under **Settings**, choose **Peerings**
- Click **Add**:
  - From `NordNet-1` to `NordNet-2`: `Net1-Net2`
  - From `NordNet-2` to `NordNet-1`: `Net2-Net1`

**Sofia**: “Remember, peering is bidirectional — both towns need to agree.”

**Mr. eks2**: “So it’s like a handshake between mayors?”

**Kasper**: “Exactly! Or a warm ‘hej hej’ 🤝”

---

### 💻 Step 4: Create the First Virtual Machine

**Kasper**: “Let’s bring some life to **NordNet-1** — with a server named **NordicVault-VM1**.”

- Search **Virtual Machines**
- Click **Create**
- Name: `NordicVault-VM1`
- Image: **Windows Server 2019**
- Size: **Standard_B2s**
- Allow **RDP (3389)** access
- Use **Subnet-A** in **NordNet-1**

**Sofia**: “Choose **Standard SSD** for storage. It balances cost and performance.”

**Mr. eks2**: “So this VM is like the central library in our town?”

**Kasper**: “Yes! And we’ll log in and use it soon.”

---

### 💻 Step 5: Create the Second Virtual Machine

**Kasper**: “Same process, now for **NordNet-2** — we’ll create **NordicVault-VM2**.”

- Name: `NordicVault-VM2`
- Region: **West Europe**
- No public ports (we'll reach it internally)
- Use **Subnet-B** in **NordNet-2**

**Sofia**: “No public access keeps it more secure. We'll use private roads only.”

**Mr. eks2**: “So only insiders can visit this library?”

**Sofia**: “Exactly. Good cybersecurity is like a quiet town — only welcome guests get in.”

---

### 🔌 Step 6: Enable Communication Between VMs

**Kasper**: “Time for our first cloud ride!”

- Open **VM1**
- Click **Connect > RDP**
- Log in using credentials
- In **PowerShell**, run:

```powershell
New-NetFirewallRule –DisplayName "Allow ICMPv4-In" –Protocol ICMPv4
```

- Then connect to **VM2’s** private IP (e.g. `mstsc /v:10.2.0.4`)

**Sofia**: “This lets VM1 ping or reach VM2 — like driving over that private road.”

**Mr. eks2**: “So, if VM1 can reach VM2, the peering is successful?”

**Kasper**: “Yes! Cloud networking magic confirmed.” ✨

---

### 🧹 Clean-Up Time

After the journey:

- Delete all created **Virtual Networks**, **VMs**, and **Resource Groups**
- This keeps your environment clean and budget safe 💸

---

## 🌍 Real-World Reflection

In real jobs, teams often work across different networks and departments. With **Virtual Network Peering**, you let them collaborate — without compromising security. It’s like letting departments talk while still keeping their doors locked.

New learners and job switchers will often configure VMs and peering — this is a real-world cloud foundation skill. Many companies need secure communication across cloud resources, and you’ll now know how to do it.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word          |
|----------------------|----------------------|
| Resource Group       | Ressourcegruppe      |
| Virtual Network      | Virtuelt netværk     |
| Subnet               | Undernetværk         |
| Virtual Machine      | Virtuel maskine      |
| IP Address           | IP-adresse           |
| Region               | Region               |
| Firewall Rule        | Firewall-regel       |
| Peering              | Sammenkobling        |
| Storage              | Lager                |
| Network Interface    | Netværksgrænseflade  |

---

## 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

This lab teaches more than buttons and menus — it trains your instincts. When **Virtual Machines** are locked behind private networks, when **firewall rules** are added with care, and when peering is configured wisely — you're building a secure foundation.

In the real world, a 158-year-old company collapsed due to a single compromised password. One misstep undid a century of work. Read their story: https://www.bbc.com/news/articles/cx2gx28815wo

🛡️ Every peering rule, every private IP, every denied public port — it all matters. You’re not just learning Azure. You’re protecting legacies.

---

### 🧾 Guided by:

🛸 **Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
**🇩🇰 Kasper Madsen** — a joyful Danish Azure Security Specialist who turns labs into friendly journeys  
**🇪🇸 Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity  
**✍️ Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
