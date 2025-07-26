# 🔒 Lab 6: Network Access to Storage Accounts

## 🔮 Scenario Setup

Mr. eks2 entered the Azure lab room, this time wearing a little “🌐 NETWORKS” badge clipped to his cloud-blue sweater.

> “Today we’re connecting the dots — and by dots, I mean networks and storage,” said 🇩🇰 **Kasper**, juggling a few Ethernet cables like spaghetti.

🇪🇸 **Sofia** smiled softly and added, “And by the end, you’ll understand how to keep your storage safe — by letting only your private network access it.”

This lab is all about how to **secure storage accounts** by **removing public access**, setting up **Private Endpoints**, and accessing them from a **Virtual Machine** inside a **Virtual Network**. Let’s get into it — gently, joyfully. ☁️🔐

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🌐 Step 1: Create a Virtual Network

**Kasper**: “Let’s build a little cloud neighborhood! A **Virtual Network** is like your city zone — where only trusted houses (VMs, Storage, etc.) live.”

**Steps:**
- Go to **Create a resource** → Search and select **Virtual Network**
- Name it `vnet-DKSecure-west1`
- Use the **West Europe** region
- On the **IP Addresses** tab:
  - Remove default space 🧹
  - Add new space: `10.0.0.0/24`
  - Create a **Subnet**: Name `subnet-NordicApp` and assign same range

**Sofia**: “Always customize your network’s IP space. Don’t keep the defaults. It helps with security and organization.”

**Mr. eks2**: “It’s like choosing a calm street instead of a noisy one... but for cloud traffic.”

---

### 🏢 Step 2: Create a Storage Account with Private Endpoint

**Kasper**: “Now we’ll make a digital vault — and only our private street can reach it!”

**Steps:**
- Go to **Storage Accounts** → **Create**
- Name: `nordicvaultstore001`
- Region: **West Europe**
- **Performance**: Standard
- **Redundancy**: GRS (default)

On the **Networking** tab:
- Choose **Private access only**
- Click **+ Add private endpoint**
  - Name: `pe-nordicblob01`
  - Sub-resource: **blob**
  - Virtual Network: `vnet-DKSecure-west1`
  - Subnet: `subnet-NordicApp`

**Sofia**: “Private Endpoints use the Azure backbone network. No data touches the public internet. It’s like teleporting safely.”

**Mr. eks2**: “Teleporting blob data… I could write poetry about that.”

---

### 🖥️ Step 3: Create a Virtual Machine

**Kasper**: “Every neighborhood needs a house! Let’s build a **Virtual Machine** inside our new network.”

**Steps:**
- Go to **Virtual Machines** → **+ Create**
- Name: `VM-DKAccessNode`
- Image: **Windows Server 2019**
- Size: `Standard_B2s`
- Allow RDP (3389)
- Use the same Virtual Network + Subnet

**Sofia**: “This VM will be your gateway to test access — but be sure to allow only what’s needed. No open doors!”

**Mr. eks2**: “So it’s like letting a friend in with a key, not leaving the door unlocked.”

---

### 🧪 Step 4: Access Storage from the VM

**Kasper**: “Here comes the fun part! Let’s log into the VM and peek into the storage — safely.”

**Steps:**
- Connect via **RDP**
- Use **VM credentials** when prompted
- Turn off **IE Enhanced Security** (under Local Server)
- Install **Azure Storage Explorer**
- Use **Connection String** from Storage Account Access Keys
- In Explorer: Go to **Blob Containers** > `$logs`

**Sofia**: “Disabling IE security is only for lab testing. Never do that in real production environments.”

**Mr. eks2**: “Exploring storage through a secure tunnel… feels like cloud spelunking.”

---

### 🧹 Final Step: Clean Up Resources

> Kasper: “Alright, time to clean our digital desk!”

Delete:
- **Virtual Network**
- **Storage Account**
- **Virtual Machine**

---

## 🌍 Real-World Reflection

This lab shows how to **lock down your storage** in the cloud and only allow access through **private connections**. In a real job, this keeps your data safe from the public internet — a huge win for compliance, security, and peace of mind.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word           |
|----------------------|------------------------|
| Virtual Network      | Virtuelt netværk       |
| Storage Account      | Lagerkonto             |
| Private Endpoint     | Privat endepunkt       |
| Virtual Machine      | Virtuel maskine        |
| Resource Group       | Ressourcegruppe        |
| Subnet               | Undernetværk           |
| IP Address           | IP-adresse             |
| Redundancy           | Redundans              |
| Blob                 | Blob                   |
| Access Key           | Adgangsnøgle           |

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
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
