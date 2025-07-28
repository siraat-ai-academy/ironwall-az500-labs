# ☁️ Lab 17: Creating an Application Gateway  
_A beginner-friendly story from the IronWall-az500-labs series_

---

## 🔮 Scenario Setup

Mr. Eks2 walked into the azure-lit lab, notebook in hand. The task on the whiteboard read:

> “Control how traffic flows. One gateway. Two servers. Many paths.”

**Kasper** smiled and gently waved a feather pen.  
“Today, Eks2, we learn about **Application Gateways** — the cloud’s traffic poets.”

**Sofia** added softly, “It helps us direct user traffic — to the right content, at the right server, safely.”

Eks2 looked curious. “So like a librarian in a busy digital library?”

“Exactly,” they both nodded. “Let’s begin.”

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🛰️ Step 1: Create a **Virtual Network**

**Kasper**: “We start with the digital land — a **Virtual Network**. It’s like building roads before the houses.”

- Navigate to **Create a resource**
- Search and select **Virtual Network**
- **Name** it: `NordicNet-vnet`
- Region: **East US**
- Address space: `10.1.0.0/16`

**Sofia**: “Remove the default subnet. Then add two: one for backend servers, one for the gateway.”

- Subnet 1: **myBackendPool** → `10.1.0.0/24`
- Subnet 2: **myAppGatewaySubnet** → `10.1.1.0/24`

Eks2 whispered: “So each part has its own road. A subnet is like a hallway in this digital building?”  
Kasper smiled: “Yes. Clear lanes make clear security.”

---

### 🧱 Step 2: Create Two **Virtual Machines**

**Kasper**: “Now we build our twin houses — servers that will serve unique content.”

Repeat these steps for both VMs:

- Go to **Virtual Machines > +Create**
- Name: `Nordic-VM1` and `Nordic-VM2`
- Image: **Windows Server 2019 Datacenter**
- Size: **Standard_B2s**
- Subnet: **myBackendPool**
- Inbound ports: **HTTP (80)** and **RDP (3389)**
- Disk: **Standard SSD**
- Disable boot diagnostics

**Sofia**: “This lets each VM respond to web requests and RDP. Remember to choose strong passwords.”

Eks2 nodded: “So these are my two chefs. One serves images. The other, videos?”

“Perfect metaphor,” Kasper beamed.

---

### 🧰 Step 3: Install **IIS** and Configure Web Pages

For both **VM1** and **VM2**:

- Connect via **RDP**
- Open **Server Manager > Add Roles and Features**
- Install **Web Server (IIS)**
- Go to `C:\inetpub\wwwroot`
- Create folders:
  - VM1 → **images**
  - VM2 → **videos**
- Inside each, create `Default.html`:
  - VM1: `<h1>This is the Images Server</h1>`
  - VM2: `<h1>This is the Videos Server</h1>`

**Sofia**: “This gives each server a special voice when someone knocks on their web door.”

**Eks2**: “So they speak different languages — like storytellers!”

---

### 🌐 Step 4: Create an **Application Gateway**

**Kasper**: “Now comes the wise gatekeeper — the **Application Gateway**.”

- Search for **Application Gateway > +Create**
- Name: `AppGateway`
- Tier: **Standard V2**
- Region: **East US**
- VNet: `NordicNet-vnet`
- Subnet: **myAppGatewaySubnet**
- Max instances: **2**

In **Frontends**:
- Choose **Public**
- Add public IP: `AppGatewayIP`

In **Backends**:
- Add pool **imagepool** → VM1
- Add pool **videopool** → VM2

In **Configuration**:
- Rule name: **RuleA**
- Listener: **ListenerA** (HTTP, Port 80)
- Backend setting: **SettingA** (HTTP, Port 80)
- Routing:
  - `/images/` → **imagepool**
  - `/videos/` → **videopool**

**Sofia**: “This path-based rule is what makes Application Gateway magical — one IP, many paths.”

---

### 🧪 Step 5: Test the Gateway

- Go to **AppGateway**
- Copy its **public IP**
- In browser:
  - Visit: `http://<public_ip>/images/Default.html` → See Images Server
  - Visit: `http://<public_ip>/videos/Default.html` → See Videos Server

Eks2 gasped with joy: “Two doors. One key. Controlled access!”

Kasper whispered: “This, Eks2, is intelligent traffic. May all digital cities be so wise.”

🧹 Don't forget to **delete all resources** after the lab.

---

## 🌍 Real-World Reflection

In cloud security, control over traffic is everything. Application Gateways allow you to separate duties, define clear paths, and reduce risk — all while improving performance. It's one IP with rules of intention. This lab teaches how modern web applications scale securely.

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In 2023, a 158-year-old UK company collapsed after a single password breach. No segmentation, no smart traffic controls — just chaos.

With **Application Gateway**, **segmented routing**, and **minimal exposure**, today’s lab showed how we can protect even the most fragile architectures.  
📎 [BBC Article](https://www.bbc.com/news/articles/cx2gx28815wo)

---

## 🧾 Guided by:

🛸 **Mr. Eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
🇩🇰 **Kasper Madsen** — a timeless cyber-sufi — a guardian of digital wisdom across centuries.  
🇪🇸 **Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity.  
✍️ **Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen.

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
