# 🗺️ AZ-500 Diagram + Friendly Breakdown  
### Lab 18: Troubleshoot Routing, Load Balancing & Traffic Control  
---

## 📊 Text-Based Diagram: “The Cloud Village of NordicBridgeNet”

```plaintext
+---------------------------+
|    🏘️  Resource Group     |
|     NordicBridge-RG       |
+---------------------------+
             |
             v
+---------------------------+
|     🌐 Virtual Network     |
|     NordicBridgeNet       |
+---------------------------+
       |            |
       |            v
       |     +-----------------------+
       |     |  🚪 Azure Bastion     |
       |     |  (Secure Login)       |
       |     +-----------------------+
       |
       v
+----------------------------+
|  🔀 NAT Gateway            |
|  NorthLightNAT             |
|  ↔ Enables safe outbound   |
+----------------------------+
       |
       v
+----------------------------+
|  🧱 Subnet: myBackendSubnet |
+----------------------------+
       |
       v
+-----------------------------------------------------------+
|                     ⚖️ Load Balancer                      |
|                       SilkBalancer                        |
|  [Frontend IP: MyFrontendIP]                              |
|  [Backend Pool: MyBackendPool]                            |
|  [Health Probe: MyHealthProbe]                           |
|  [LB Rule: MyHTTPRule, Port 80]                          |
+-----------------------------------------------------------+
       |                      |
       v                      v
+------------------+   +------------------+
| 💻 Virtual Machine |   | 💻 Virtual Machine |
| NordicVault-VM1   |   | NordicVault-VM2   |
|  (HTTP via NSG)   |   |  (HTTP via NSG)   |
+------------------+   +------------------+

         🔐 NSG (SafeDoorsNSG)
         [Inbound Rule: Allow HTTP 80]

```

---

## 🎭 Diagram Explanation – Friendly Dialogue Format

**Mr. Eks2** stirred his cocoa as the digital map hovered gently in front of him. “So... this is what we built today?” he asked.

**🇩🇰 Kasper** stepped in with a warm smile. “Yes, Eks2. Welcome to the village of **NordicBridgeNet** — where every piece of Azure plays a role. Let's walk through it.”

---

### 🏘️ **Resource Group** → The Family Folder

**Kasper:** “Think of this as your digital folder in the sky — all your Azure stuff lives here together like cousins under one roof.”  
**Sofia:** “It also helps when deleting resources. Clean-up is a breeze.”  
**Eks2:** “Ah! Like putting all your socks in one drawer. Nice!”

---

### 🌐 **Virtual Network (VNet)** → The Village Roads

**Kasper:** “The VNet connects your homes (VMs). It’s the network of invisible roads they travel on.”  
**Sofia:** “And we set the right **IP Address space**, so nobody bumps into each other!”  
**Eks2:** “So, no traffic jams in my subnet? Sweet.”

---

### 🚪 **Azure Bastion** → The Secure Bridge

**Kasper:** “Instead of letting people enter through the front gate (public IP), we built a magical bridge — **Azure Bastion** — to enter securely.”  
**Sofia:** “It's one of the safest ways to log in. No direct public exposure.”  
**Eks2:** “Feels like knocking on the castle door with a secret knock.”

---

### 🔀 **NAT Gateway** → The One-Way Tunnel

**Kasper:** “Your VMs need to browse the web? This **NAT Gateway** gives them a way out without revealing their home address.”  
**Sofia:** “It protects outbound traffic. You go out, but bad guys can't come in.”  
**Eks2:** “Like writing anonymous love letters. Secure, yet distant.”

---

### ⚖️ **Load Balancer** → The Cloud Butler

**Kasper:** “Now this is fun — our **SilkBalancer** is like a smart butler. Every time a guest comes, it says: ‘You go to VM1. Next? You go to VM2.’”  
**Sofia:** “And the **Health Probe** checks if a VM is awake before the butler sends a guest in.”  
**Eks2:** “So if VM1 naps, traffic goes to VM2? How polite!”

---

### 💻 **Virtual Machines (VM1 & VM2)** → The Workers

**Kasper:** “Each VM is a quiet little house, replying ‘Hello World’ to any browser knock.”  
**Sofia:** “We used **IIS** to help them speak. It’s like giving them a voicebox.”  
**Eks2:** “VMs with voices — that’s adorable.”

---

### 🔐 **Network Security Group (NSG)** → The Village Guard

**Kasper:** “Every village needs security. Our **SafeDoorsNSG** checks who’s allowed in.”  
**Sofia:** “In this case, only visitors on **Port 80 (HTTP)** are allowed.”  
**Eks2:** “I’ll note the Danish word *Sikkerhedsgruppe* for this one.”

---

## 🌍 Final Takeaway

This diagram teaches us how Azure services connect like a living ecosystem. The VNet is the land, the VMs are the homes, the Load Balancer is the postman, and the NSG is the guard. When designed with love and logic, security becomes natural — not scary.

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In a tragic real-world incident, a company that stood for 158 years collapsed — because one single password was weak. That’s all it took.  
In this lab, we saw how using **NSGs**, secure login via **Bastion**, and traffic control via **Load Balancer** helps shield systems from these tiny cracks.  
What seems like “just a setting” is actually a legacy shield. Always configure with care.  
Read the story here: [BBC Report](https://www.bbc.com/news/articles/cx2gx28815wo)

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
