# 📊 AZ-500 Diagram + Friendly Breakdown  
**Lab 17 – Creating an Application Gateway**

---

## 🖼️ Text-Based Diagram (Path-Based Routing with Application Gateway)

```text
+-----------------------------+
|     Resource Group          |
|     NordicApp-RG            |
+-------------+---------------+
              |
              v
+-----------------------------+
|     Virtual Network         |
|     NordicNet-vnet          |
|     Address: 10.1.0.0/16    |
+------+------+---------------+
       |      |
       v      v
+-----------+   +--------------------------+
| Subnet A  |   | Subnet B                |
| myBackend |   | myAppGatewaySubnet      |
| Pool      |   |                          |
+-----+-----+   +------------+-------------+
      |                      |
      v                      v
+------------+         +------------------+
| Nordic-VM1 |         |  AppGateway      |
| (images)   |         |  Public IP: ✅   |
+------------+         +--------+---------+
                               |
               +---------------+----------------+
               | Route: /images/ → VM1 (images) |
               | Route: /videos/ → VM2 (videos) |
               +--------------------------------+
                               |
                         +-----------+
                         | ListenerA |
                         +-----------+
```

---

## 🎭 Diagram Walkthrough: Let’s Chat Through It!

### 🧱 Step 1: **Virtual Network** (virtuel netværk)

**🇩🇰 Kasper**: “This is the cloud town. The **Virtual Network** is your whole little kingdom in Azure. It holds roads, houses, and even wise gatekeepers.”

**🇪🇸 Sofia**: “We carved this kingdom into two subnets — one for the servers, and one just for the Application Gateway. Each with their own address range.”

**👨‍💼 Mr. Eks2**: “So it's like assigning neighborhoods to different departments?”

---

### 🏠 Step 2: **Virtual Machines**

**🇩🇰 Kasper**: “These are your two digital chefs. **Nordic-VM1** bakes images, and **Nordic-VM2** serves videos — all through the humble magic of IIS.”

**🇪🇸 Sofia**: “We placed both VMs in the backend subnet. Each serves a special folder with a unique HTML message.”

**👨‍💼 Mr. Eks2**: “Two kitchens, two menus — I love it.”

---

### 🛡️ Step 3: **Application Gateway**

**🇩🇰 Kasper**: “Ah… the traffic philosopher. One **Application Gateway**, one public IP, but many possible paths!”

**🇪🇸 Sofia**: “We used path-based routing. When a request says `/images/`, it’s directed to VM1. When it says `/videos/`, it goes to VM2.”

**👨‍💼 Mr. Eks2**: “So this one IP knows how to split the traffic based on the URL path? That’s beautiful.”

---

### 📬 Step 4: **Listener + Rules**

**🇩🇰 Kasper**: “The **Listener** is the gateway’s doorman. It listens for what comes to Port 80 and gently applies the correct rule.”

**🇪🇸 Sofia**: “We created **ListenerA**, along with **SettingA** that defines the port and protocol — all using HTTP.”

**👨‍💼 Mr. Eks2**: “It's like a receptionist forwarding calls to the right person — ‘Images? Please hold for VM1!’”

---

## 🌍 Final Takeaway

This diagram shows how **Application Gateways** help manage and control traffic with elegance. With **subnets**, **VMs**, and **routing rules**, we learned to design flow — not just allow access. It’s all about clarity, structure, and smart gatekeeping.

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

When a 158-year-old British company collapsed due to a single weak password, it wasn’t just poor authentication. It was a lack of segmentation, no traffic management, no zero-trust logic.

This lab taught us how to use **Application Gateways**, **subnet separation**, and **path control** — turning simple tools into serious security strategy.  
📎 [Read the BBC story](https://www.bbc.com/news/articles/cx2gx28815wo)

---

## 🧾 Guided by:

🛸 **Mr. Eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
🇩🇰 **Kasper Madsen** — a timeless cyber-sufi — a guardian of digital wisdom across centuries.  
🇪🇸 **Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity.  
✍️ **Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen.

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
