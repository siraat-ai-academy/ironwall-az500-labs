# Interview Task – Quick Recall Sheet (Lab 14 – VMSS with CLI)

## 🚀 Summary of Key Steps & Purpose

- **Step 1**: Launch **Azure Cloud Shell** *(to run CLI commands without needing local setup)*  
- **Step 2**: Choose **Bash** environment *(commonly used for Azure CLI tasks)*  
- **Step 3**: Create a **Virtual Machine Scale Set (VMSS)** using `az vmss create` *(to deploy scalable VMs with flexible orchestration for dynamic workloads)*  
- **Step 4**: Use `--generate-ssh-keys` *(to securely access your VMs via SSH)*  
- **Step 5**: Specify `--orchestration-mode flexible` *(to manage VMs individually in the scale set for better flexibility and control)*  
- **Step 6**: List VMs with `az vm list` *(to verify deployment and monitor instances in a clear table format)*  
- **Step 7**: Scale out VMSS using `az vmss scale` *(to increase capacity and simulate real-world traffic/load growth)*  
- **Step 8**: Confirm capacity change using `az vm list` *(to ensure expected VM instances are running)*  
- **Step 9**: Stop all instances with `az vmss stop` *(to save cost when resources are idle)*  
- **Step 10**: Stop a single VM with `az vm stop` *(to control specific workloads without affecting others)*  
- **Step 11**: Deallocate VM using `az vm deallocate` *(to release compute resources and save charges)*  
- **Step 12**: Start a VM using `az vm start` *(to bring a single VM back online for updates or testing)*  
- **Step 13**: Start all VMs with `az vmss start` *(to resume full workload after downtime or scaling)*  
- **Step 14**: Restart individual VMs or full scale set using `az vm restart` or `az vmss restart` *(to apply updates or recover from issues)*  
- **Final Step**: **Delete resources** *(to practice good cleanup and avoid unnecessary charges)*

---

## 🧾 Guided by:  
🛸 **Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, quietly turning steps into strength  
✍️ **Muhammad Naveed Ishaque** — the voice behind the journey, making learning feel human  
🔐 **From the IronWall Labs** — where security is care, and clarity is power.
