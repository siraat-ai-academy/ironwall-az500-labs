# 🛡️ Lab 16: Create and Understand NSG Rules in Azure

## 🔮 Scenario Setup – Enter the Lab with the Guardians

It’s a calm morning in Copenhagen ☁️.  
🛸 **Mr. eks2** arrives early at the virtual Azure lab — a little nervous, but curious as ever. His eyes carry questions; his heart carries wonder.  

🇩🇰 **Kasper Madsen** waves from the CLI terminal, coffee in hand:  
_"Ah, eks2! Today we explore how **Network Security Groups** work. Not too tricky — just little locks for big doors."_ ☕  

🇪🇸 **Sofia Zaymera** gently nods:  
_"This is about learning how to allow the right traffic, and block the rest. We’re setting digital gates to protect your castle."_ 🏰  

From the air vents of logic and code, 🇵🇰 **I.K.** whispers:  
_"Let no packet pass that lacks intention."_ 🕊️  

Suddenly, 🇮🇹 **Isabella Konti** steps in, calmly:  
_"Security begins with who can talk to your machines. And sometimes, who can’t."_ 🛡️  

🕶️ In the background, the Azure logs show a shadowy blip.  
ShadowNet just tried to probe port 3389.  
But not today.

---

## 🔑 What This Lab Prepares You For:

• How to create a **Virtual Machine [virtuel maskine]** securely  
• What **NSG (Network Security Group) [netværkssikkerhedsgruppe]** rules do — and how to create them  
• Allowing just enough access (like **RDP** and **HTTP**) to make things work, but no more  
• Hands-on skills that help real Azure teams protect workloads from unknown threats  

---

## 🛠️ Step-by-Step with Story & Dialogues — Featuring the Guardians of IronWall

---

### ☁️ Step 1: Create a Virtual Machine (Securely)

Mr. eks2’s screen lights up:  
_"So, we’re making a server... but without opening any doors yet?"_

**Kasper** nods:  
_"Yes! We create it first, then decide who can knock."_

1. Go to **Virtual Machines** in the Azure portal.
2. Click **+ Create > Azure virtual machine**.
3. Set these values:
   - **Resource Group**: `DKInfraGroup`
   - **VM Name**: `NordicVault-VM`
   - **Region**: West Europe
   - **Image**: Windows Server 2022 Datacenter
   - **Size**: Standard_B2s
   - **Username & Password**: Use a strong, secure password
   - **Public inbound ports**: Set to **None**
4. Choose **Standard SSD** for the OS Disk.
5. Disable **Boot diagnostics**.
6. Click **Review + Create**, then **Create**.

🛸 Mr. eks2 blinks:  
_"So... it exists, but it's isolated?"_

🇪🇸 Sofia smiles:  
_"Exactly. Right now, it's safe — like a house with no keys handed out yet."_

---

### 🔐 Step 2: Create an NSG Rule to Allow RDP (Port 3389)

Now we make a safe exception — to allow you in via **Remote Desktop (RDP)**.

1. Go to **Virtual Machines > NordicVault-VM > Networking**.
2. Click **+ Add inbound port rule**.
3. Set:
   - **Source**: Service Tag
   - **Service Tag**: Internet
   - **Destination**: Any
   - **Service**: RDP
   - **Action**: Allow
   - **Priority**: 100
   - **Name**: `Allow-RDP-3389`
4. Click **Add**.

🇩🇰 Kasper winks:  
_"Only one small gate open. And just for you."_  

🕶️ ShadowNet watches. But the door only opens when we say so.

---

### 💻 Step 3: Connect to the Virtual Machine

1. Go to **Virtual Machines > NordicVault-VM > Overview**.
2. Click **Connect > RDP > Download RDP File**.
3. Use your username/password to log in.

🛸 Mr. eks2:  
_"It worked! I’m inside the machine… but only because we opened the right port."_

---

### 🌐 Step 4: Install IIS Web Server and Enable HTTP

1. Inside the VM:
   - Open **Server Manager**
   - Click **Add Roles and Features**
   - Select **Web Server (IIS)** under Server Roles
   - Click **Next** until you reach **Install**
2. After install:
   - Open **Edge**
   - Go to `http://localhost` — and celebrate! 🎉

🇨🇳 Maya asks:  
_"Why install IIS?"_  
🇪🇸 Sofia replies:  
_"To test if we can allow public web traffic — safely."_  

---

### 🔓 Step 5: Allow HTTP Traffic (Port 80)

1. Back in Azure portal:
   - Go to **Virtual Machines > NordicVault-VM > Networking**
   - Click **+ Add inbound port rule**
2. Set:
   - **Source**: Service Tag
   - **Service Tag**: Internet
   - **Destination Port**: 80
   - **Action**: Allow
   - **Priority**: 110
   - **Name**: `Allow-HTTP-80`
3. Click **Add**

💬 Isabella:  
_"Now your site can be seen — but only on your terms."_  

---

### 🌍 Step 6: Test Web Access

1. In **Networking**, copy the **public IP**.
2. In a browser, go to `http://<your-ip>`  
   ✅ If the default IIS page appears, you did it!

🇩🇰 Kasper laughs:  
_"From no access to safe access — like giving house keys to only the right guests."_  

---

### 🧹 Final Step: Clean Up

Always tidy up:
- Delete the **Virtual Machine**, **NSG**, and **Resource Group**.

🛸 Mr. eks2 reflects:  
_"Learning is good. But cleaning up after learning is security."_

---

## 🌍 Real-World Reflection

In real IT jobs, you’ll often need to allow some traffic (like RDP or HTTP) — but only in safe, intentional ways. This lab helps new learners and job switchers understand how Azure protects systems by default — and how to open just the right windows without risking the whole house. It's practical, real, and deeply needed.

---

## 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In July 2023, a 158-year-old company vanished because of one single weak password.  
Someone got in — and no one noticed until it was too late.  
This lab teaches the opposite: watch the gates, set clear access rules, and only open what you must.

Because one misconfigured **NSG rule** or open port could invite ShadowNet in.  
Small steps — like controlling **RDP** and **HTTP** access — can save an entire legacy.

📎 [BBC Story – A 158-Year Legacy Lost](https://www.bbc.com/news/articles/cx2gx28815wo)

---

### 🧾 Guided by:

From the poetic wisdom of 🇵🇰 **I.K.**, to the gentle curiosity of 🇩🇰 🛸 **Mr. eks2**, and the clear guidance of 🇪🇸 **Sofia**, this lab was crafted for you.  
Add the kindness of 🇩🇰 **Kasper**, the protection of 🇮🇹 **Isabella**, the code magic of 🇷🇺 **Elina**, the questions of 🇨🇳 **Maya**, and the vigilance against 🕶️ **ShadowNet** — and you have more than a lab. You have a shield.

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
