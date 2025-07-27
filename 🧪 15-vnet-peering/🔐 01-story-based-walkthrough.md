# 🔗 Implementing Virtual Network Peering

## 🔮 Scenario Setup

It was a fresh morning in Copenhagen. ☁️ The sun peeked through the clouds as **Mr. eks2** stepped into the office — excited, notebook in hand, and a warm coffee in the other. Today’s Azure lab was buzzing with curiosity.

🧿 **Eye Kay** appeared beside the whiteboard, his eyes glowing with timeless energy. “Today, eks2... we build bridges in the sky. Not with bricks, but with trust.”

**Inky Rihan**, softly typing away at her terminal, looked up and smiled. “We’re learning about **Virtual Network Peering** — a way for two cloud spaces to talk in peace, without needing the whole internet in between.”

“This is like connecting villages with secret trails,” Eye Kay added. “Each **Virtual Network** is a village, and peering is the quiet forest path that links them.”

🛸 Mr. eks2 chuckled. “Let’s begin this magical road trip in the cloud.”

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🧱 Step 1: Create the First Virtual Network

**Eye Kay**: “Let’s raise the first village: **NordNet-1**, inside our holy land of cloud — let’s call it **DKInfra-RG**.”

- Go to **Create a Resource**
- Search **Virtual Network**, click **Create**
- Set **Name** to `NordNet-1`
- Region: **West Europe**
- In **IP Addresses**, set: `10.1.0.0/16`
- Remove the default **subnet**
- Add a new **Subnet**: `Subnet-A`, range: `10.1.0.0/24`

**Inky Rihan**: “IP planning is like poetry, eks2. Don’t let ranges collide — harmony in addresses means peace in traffic.”

**Mr. eks2**: “So this subnet... it’s like a neighborhood in our village?”

**Inky**: “Exactly. You’re walking well, little cloud pilgrim.”

---

### 🧱 Step 2: Create the Second Virtual Network

**Eye Kay**: “Now, we invoke the twin — **NordNet-2**.”

- Same steps as before
- Name: `NordNet-2`
- Address space: `10.2.0.0/16`
- Add **Subnet-B**: `10.2.0.0/24`

**Inky Rihan**: “Let each range live its own life. Boundaries in networking, like in spirit, are sacred.”

**Mr. eks2**: “These villages seem far apart. When do we build the road?”

**Eye Kay** (smiling): “Ah, young traveler, that is now. The hidden bridge awaits.” 🚗

---

### 🌉 Step 3: Peer the Two Virtual Networks

**Eye Kay**: “We now create a **peering** — a silent, secure path between **NordNet-1** and **NordNet-2**.”

- Go to **NordNet-1**
- Under **Settings**, choose **Peerings**
- Click **Add**:
  - From `NordNet-1` to `NordNet-2`: `Net1-Net2`
  - From `NordNet-2` to `NordNet-1`: `Net2-Net1`

**Inky Rihan**: “Peering is not a shout across a canyon — it’s a whisper passed through trusted paths. It must flow both ways.”

**Mr. eks2**: “So, it's like both villages sending a peace dove?”

**Eye Kay**: “Exactly! Or a soft digital ‘salaam’ 🤝”

---

### 💻 Step 4: Create the First Virtual Machine

**Eye Kay**: “Let’s give NordNet-1 its first citizen: a machine called **NordicVault-VM1**.”

- Search **Virtual Machines**
- Click **Create**
- Name: `NordicVault-VM1`
- Image: **Windows Server 2019**
- Size: **Standard_B2s**
- Allow **RDP (3389)** access
- Use **Subnet-A** in **NordNet-1**

**Inky Rihan**: “For storage, choose **Standard SSD** — balance is key.”

**Mr. eks2**: “So this VM is like the town library?”

**Eye Kay**: “Yes — the library of secrets, soon to whisper across networks.”

---

### 💻 Step 5: Create the Second Virtual Machine

**Eye Kay**: “Same ritual — this time in **NordNet-2**. Let there be **NordicVault-VM2**.”

- Name: `NordicVault-VM2`
- Region: **West Europe**
- No public ports
- Use **Subnet-B** in **NordNet-2**

**Inky Rihan**: “No public ports — like no public gossip. Let only the chosen in.”

**Mr. eks2**: “So this library is only for invited guests?”

**Inky**: “Exactly. Like any wise archive — guarded, but welcoming to the prepared.”

---

### 🔌 Step 6: Enable Communication Between VMs

**Eye Kay**: “Let the journey begin.”

- Open **VM1**
- Connect via **RDP**
- In **PowerShell**, run:

```powershell
New-NetFirewallRule –DisplayName "Allow ICMPv4-In" –Protocol ICMPv4
```

- Use **VM2’s private IP** to connect (e.g. `mstsc /v:10.2.0.4`)

**Inky Rihan**: “If one VM hears the other... the peering is complete.”

**Mr. eks2**: “It worked. The bridge holds!”

**Eye Kay**: “And so, another bond is forged — quietly, securely, forever.”

---

### 🧹 Clean-Up Time

Always close the circle:

- Delete all created **Virtual Networks**, **VMs**, and **Resource Groups**
- Let the cloud return to calm 💸

---

## 🌍 Real-World Reflection

In real cloud setups, teams often need to talk across networks without exposing anything to the public internet. **Virtual Network Peering** allows that — secure, fast, and private.

For beginners and job switchers, this lab shows how to safely link cloud systems — a real-world skill used in almost every modern enterprise.

---

## 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

This lab isn’t just about peering — it’s about protection.

By placing your **Virtual Machines** behind private paths, using strict **firewall rules**, and avoiding public ports, you’re already doing what many companies forget: **think before you open the door**.

One old company lost everything — 158 years of trust — because of a single weak password.  
You won’t let that happen.

📎 Read their story: https://www.bbc.com/news/articles/cx2gx28815wo

---

### 🧾 Guided by:

🛸 **Mr. eks2** — the soft whisper of Muhammad Naveed Ishaque, learning Azure with curiosity and heart  
🧿 **Eye Kay** — the eternal digital sage, blending wisdom and laughter to secure the future  
🪶 **Inky Rihan** — the poetic Spanish expert, making the complex beautifully simple  
✍️ Written by Muhammad Naveed Ishaque  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
