# 🛠️ Lab 11: Create a VM with CLI

## 🔮 Scenario Setup

Mr. eks2 walked into the lab, eyes sparkling with curiosity. "Command line today?" he asked.

Kasper grinned, holding up an imaginary keyboard. "Yes, sir! Today we create a **Virtual Machine** using **Azure CLI**. No clicks, all commands!"

Sofia nodded warmly. "And we’ll teach you how the VM is born—line by line."

This lab helps you learn how to automate cloud tasks. In real jobs, CLI saves time, avoids errors, and looks pretty cool in meetings. 🧑‍💻

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🧪 Step 1: Open Cloud Shell

**Kasper**: “Imagine Cloud Shell as our magic cave. Open it from the Azure Portal—just click the little shell icon at the top.”

**Sofia**: “Choose **Bash**, unless you're feeling extra spicy with PowerShell. For today, Bash is easier.”

**Mr. eks2**: “I see... so this is where the magic begins?”

---

### 🔐 Step 2: Define Admin Credentials

**Kasper**: “Let’s not shout our password to the sky. We’ll whisper it into a variable.”

```bash
username="demouser"
password="YourSecurePassword123"
```

**Sofia**: “Remember, always use strong passwords. We call that ‘good hygiene’ in cloud security.”

**Mr. eks2**: “Aha! Quiet credentials. Safe and simple.”

---

### 🖥️ Step 3: Create the VM via CLI

**Kasper**: “Now we use one super-command to create a whole virtual kingdom. Watch this!”

```bash
az vm create \
  --name NordicVM01 \
  --resource-group DKSec-RG \
  --image win2019datacenter \
  --size Standard_B1s \
  --admin-username $username \
  --admin-password $password
```

**Sofia**: “This creates the **Virtual Machine**, its **VNet**, **Subnet**, **Public IP**, **NIC**, and **NSG**—all in one go.”

**Mr. eks2**: “So... it's like summoning a city with a single spell? Incredible!”

---

### 🖧 Step 4: Connect via RDP

**Kasper**: “We’ve built the house. Now let’s enter it! Go to the **Virtual Machine**, click **Connect**, then choose **RDP**.”

**Sofia**: “Don’t forget your credentials. And accept the certificate if prompted—it’s safe this time.”

**Mr. eks2**: “Feels like teleporting into my own computer in the sky.”

---

### 🧼 Step 5: Clean Up

**Kasper**: “Always clean your tools. After testing, delete all resources.”

**Sofia**: “Yes, keeping your subscription tidy saves money and avoids zombie VMs.”

**Mr. eks2**: “Lesson learned. Cloud cleanup is not optional—it’s cloud respect.”

---

## 🌍 Real-World Reflection

This lab shows how to build infrastructure the professional way—through automation. Azure CLI helps engineers create, replicate, and manage cloud environments efficiently. Whether you’re deploying one VM or a hundred, this technique keeps things fast, safe, and scalable.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word         |
|------------------------|---------------------|
| Resource Group         | Ressourcegruppe     |
| Virtual Machine        | Virtuel Maskine     |
| Network Security Group | Netværkssikkerhedsgruppe |
| Public IP              | Offentlig IP        |
| Virtual Network        | Virtuelt Netværk    |
| Subnet                 | Underordnet net     |
| Admin Username         | Admin Brugernavn    |
| Password               | Adgangskode         |
| Azure CLI              | Azure Kommandolinje |
| Cloud Shell            | Cloud Shell         |

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
