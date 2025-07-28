# 📄 Interview Task – Quick Recall Sheet (Lab 17 – Creating an Application Gateway)

---

## ✅ Step-by-Step Summary

- **Step 1**: Created a **Virtual Network** *(to define an isolated network space for communication between Azure resources)*

- **Step 2**: Defined two **Subnets** within the VNet:  
  - **myBackendPool** *(to host the backend VMs)*  
  - **myApplicationGatewaySubnet** *(to host the Application Gateway separately for clear segmentation)*

- **Step 3**: Created two **Virtual Machines (VM1 and VM2)** *(to act as backend servers, each serving unique content)*

- **Step 4**: Installed **IIS (Web Server)** on both VMs *(to enable basic web hosting and response to HTTP requests)*

- **Step 5**: Configured each VM with a different folder and `Default.html` file *(to simulate different content endpoints for routing)*

- **Step 6**: Created an **Application Gateway** *(to manage incoming traffic using intelligent routing and single-entry architecture)*

- **Step 7**: Assigned a **Public IP Address** to the Application Gateway *(to expose a single access point to the internet)*

- **Step 8**: Added **Backend Pools**:  
  - **imagepool** connected to VM1  
  - **videopool** connected to VM2  
  *(to group resources for routing based on URL path)*

- **Step 9**: Defined a **Routing Rule (RuleA)** using **ListenerA** *(to inspect path-based traffic and direct to the correct backend)*

- **Step 10**: Tested path-based routing:  
  - `/images/Default.html` → **Images Server (VM1)**  
  - `/videos/Default.html` → **Videos Server (VM2)**  
  *(to confirm correct behavior of path-based rules and frontend listener)*

- **Step 11**: Deleted all resources *(to follow best practices and avoid cost or exposure after lab completion)*

---

## 🧠 Why This Matters (Real-World Relevance)

This lab demonstrates how **Application Gateways** simplify traffic management and secure routing. It’s crucial for secure and scalable web applications — enabling one entry point with multiple controlled paths. Subnetting and backend separation also reflect real-world architecture best practices.

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In 2023, a 158-year-old British company collapsed after a single password breach. No segmentation, no gateway, no structured routing — just chaos.

This lab taught us to segment traffic, restrict direct access, and use a single controlled gateway to reduce risk and increase clarity. These small practices prevent massive damage.  
📎 [Read the full story on BBC](https://www.bbc.com/news/articles/cx2gx28815wo)

---

## 🧾 Guided by:
✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
