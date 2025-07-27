# 🛡️ Understand Network Security Group Rules

### 💻 Lab 16 – IronWall-az500-labs Series  
**Beginner-Friendly Azure Security Lab**  
⏱️ **Duration**: 1 hour

---

## 🔮 Scenario Setup

Mr. Eks2 arrived early this morning to the digital fortress training grounds of NordicCloud Denmark. The skies over Copenhagen were blue, and so was the Azure portal he just opened.

As always, **Kasper Madsen**, the ancient cyber-sufi, stood beside a whiteboard scribbled with firewall metaphors.

“Today,” Kasper whispered, “we learn to guard the gates.”

**Sofia Zaymera** joined with a warm smile, holding her laptop and some cinnamon rolls. “This lab is about creating rules that protect our Virtual Machine — like deciding who can knock on the digital door.”

Mr. Eks2 blinked thoughtfully. “So… we’re learning how to say yes or no to visitors?”

“Yes,” Sofia nodded. “With love… and Network Security Groups.”

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🔧 Step 1: Create a Virtual Machine

👨‍💼 **Mr. Eks2**: “How do we begin, Kasper?”

🇩🇰 **Kasper**: “Every tale begins with a home. Let’s build our digital house — a **Virtual Machine** inside a **ressourcegruppe** called **NordicFortress-RG**.”

- Go to **Virtual Machines** in the Azure portal.
- Click **+ Create > Azure virtual machine**.
- Fill in these details:
  - **Resource group**: NordicFortress-RG
  - **VM name**: NordicVault-VM01
  - **Region**: West Europe
  - **Image**: Windows Server 2022 Datacenter – Azure Edition – Gen2
  - **Size**: Standard_B2s
  - **Username**: A secure username
  - **Password**: A strong password
  - **Public inbound ports**: None
  - **Disk type**: Standard SSD

🧘 **Sofia**: “Keep **Boot diagnostics** off for now — we’re focusing only on access control.”

Click **Review + create**, then **Create**.

---

### 🔐 Step 2: Create an NSG Rule to Allow RDP (Port 3389)

👨‍💼 **Mr. Eks2**: “Can anyone visit our home yet?”

🇩🇰 **Kasper**: “Not yet. No one knows where the door is. Let’s open the gate — gently.”

- In **Virtual Machines**, choose **NordicVault-VM01**.
- Go to **Networking**.
- Click **+ Add inbound port rule**.
  - **Source**: Service Tag
  - **Source service tag**: Internet
  - **Destination**: Any
  - **Service**: RDP
  - **Action**: Allow
  - **Priority**: 100
  - **Name**: allow_rdp_3389
- Click **Add**.

💡 **Sofia**: “Only allow this when needed. Port 3389 is often targeted.”

---

### 🔗 Step 3: Connect via RDP

👨‍💼 **Mr. Eks2**: “So now I can enter?”

- Go to the **Overview** tab of the VM.
- Click **Connect > RDP > Download RDP File**.
- Open the file and use your credentials to log in.

📚 **Kasper**: “This is how admins enter their kingdom.”

---

### 🌐 Step 4: Enable HTTP and Install IIS

👨‍💼 **Mr. Eks2**: “Can our VM greet the world now?”

🇪🇸 **Sofia**: “Not yet. First, we’ll teach it to speak Web — using **IIS**.”

- On the VM, open **Server Manager > Add Roles and Features**.
- Click through until you reach **Server Roles**.
- Select **Web Server (IIS)**.
- Continue and click **Install**.

After it installs, open **Microsoft Edge** and visit `http://localhost`.

📜 **Kasper**: “Now it knows the language of the web.”

---

### 🌐 Step 5: Create NSG Rule to Allow HTTP (Port 80)

- Go to **Virtual Machines > NordicVault-VM01 > Networking**.
- Click **+ Add inbound port rule**.
  - **Source**: Service Tag
  - **Source service tag**: Internet
  - **Destination**: Any
  - **Port**: 80
  - **Action**: Allow
  - **Priority**: 110
  - **Name**: allow_http_80

💡 **Sofia**: “Now anyone can view your VM’s web page — just like a real website.”

---

### 🌍 Step 6: Test the Website

👨‍💼 **Mr. Eks2**: “Can I see it from Earth now?”

- In **Networking**, copy the **public IP address**.
- Paste it into a browser: `http://<public-ip>`.

You should see the **IIS welcome page**! 🎉

🇩🇰 **Kasper**: “You’ve built and protected your first digital hall.”

🧹 Don’t forget to delete the VM and other resources.

---

## 🌍 Real-World Reflection

Network Security Groups (NSGs) are like digital gatekeepers. In real cloud jobs, configuring these rules correctly means keeping out threats while letting the right people in. This lab teaches how to think like a security architect — one port, one permission at a time.

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In 2023, a 158-year-old British firm collapsed after a single compromised password let attackers roam free inside its systems. A simple misstep — no MFA, no alerts — and the legacy was gone.

By practicing **NSG rules**, **remote access control**, and **minimal exposure**, you are learning to protect not just data, but entire lifelines. Every secure setting matters.  
Read more here: [BBC Article](https://www.bbc.com/news/articles/cx2gx28815wo)

---

## 🧾 Guided by:

🛸 **Mr. Eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
🇩🇰 **Kasper Madsen** — a timeless cyber-sufi — a guardian of digital wisdom across centuries.  
🇪🇸 **Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity.  
✍️ **Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen.

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
