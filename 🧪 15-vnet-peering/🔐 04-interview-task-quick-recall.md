
# 📄 Interview Task – Quick Recall Sheet (Lab 15 – Virtual Network Peering)

## 🔁 Summary of Actions & Intent

- **Step 1**: Created a **Resource Group** *(to logically group all related Azure resources together for easier management and cleanup)*

- **Step 2**: Created **Virtual Network: NordNet-1** *(to define a private IP space and isolated network environment for our first set of resources)*

- **Step 3**: Added **Subnet-A** to **NordNet-1** *(to divide the network and place resources like VMs in a specific IP range for control and security)*

- **Step 4**: Created a second **Virtual Network: NordNet-2** *(to simulate another isolated environment that we may want to connect securely with the first)*

- **Step 5**: Added **Subnet-B** to **NordNet-2** *(to organize resources and enable subnet-level control)*

- **Step 6**: Configured **VNet Peering** between **NordNet-1** and **NordNet-2** *(to allow private, low-latency communication between the two VNets without internet exposure)*

- **Step 7**: Created **Virtual Machine: NordicVault-VM1** in **Subnet-A**, enabled **RDP** *(to simulate a publicly accessible server that can be logged into and used to test connectivity)*

- **Step 8**: Created **Virtual Machine: NordicVault-VM2** in **Subnet-B**, no public ports *(to simulate a secure, internal-only resource within the second VNet)*

- **Step 9**: Enabled internal communication by adding a **Firewall Rule** via **PowerShell** on **VM1** *(to allow ping requests for testing network connectivity between the VMs)*

- **Step 10**: Used **mstsc /v:[VM2 IP]** command *(to initiate internal RDP session from VM1 to VM2 using private IP — validating successful peering and connectivity)*

- **Final Step**: Deleted all resources *(to avoid unnecessary billing and keep the environment clean)*

---

## 💡 Core Learnings
- Understand how **Virtual Networks**, **Subnets**, and **Peering** enable secure internal traffic across isolated environments.
- Practice minimal exposure principles: **one VM** was public, the other **remained private**.
- Reinforce use of **PowerShell** to apply **firewall rules** and control traffic at the OS level.
- Demonstrate secure remote access and testing via **RDP over private IP**.

---

### ✒️ Closing Signature:
________________________________________
🧾 Guided by:  
🛸 **Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, quietly turning steps into strength  
✍️ **Muhammad Naveed Ishaque** — the voice behind the journey, making learning feel human  
🔐 From the **IronWall Labs** — where security is care, and clarity is power.
