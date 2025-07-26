# Interview Task – Quick Recall Sheet (Lab 14 – VMSS with CLI)

- **Step 1**: Launched **Azure Cloud Shell** *(to access a CLI environment directly in the Azure Portal without local setup)*
- **Step 2**: Selected **Bash Shell** and applied settings *(to use shell scripting and run CLI commands smoothly)*
- **Step 3**: Created a **Virtual Machine Scale Set (VMSS)** using `az vmss create` *(to deploy scalable and manageable VMs for load balancing and performance)*
- **Step 4**: Used `--orchestration-mode flexible` *(to manage individual VM instances independently within the scale set)*
- **Step 5**: Verified **VMSS creation** with `az vm list` *(to confirm deployment and check instance details)*
- **Step 6**: Scaled out the VMSS using `az vmss scale` *(to increase capacity and handle more load or demand)*
- **Step 7**: Re-verified VM count using `az vm list` *(to ensure scaling applied correctly)*
- **Step 8**: Stopped **all VM instances** in the scale set with `az vmss stop` *(to reduce resource usage and cost temporarily)*
- **Step 9**: Stopped a **single VM instance** using `az vm stop` *(to manage individual VM for maintenance or testing)*
- **Step 10**: Deallocated a specific VM using `az vm deallocate` *(to release compute resources while preserving configurations)*
- **Step 11**: Started an individual VM with `az vm start` *(to bring a single machine back online for use)*
- **Step 12**: Started all VMSS VMs using `az vmss start` *(to restore operations across the environment)*
- **Step 13**: Restarted a VM using `az vm restart` *(to apply changes or resolve issues)*
- **Step 14**: Restarted the whole VMSS using `az vmss restart` *(to refresh the entire workload environment in one go)*
- **Final Step**: Deleted all resources *(to clean up and avoid unnecessary charges or clutter)*

________________________________________
🧾 Guided by:
🛸 Mr. eks2 — the curious whisper of Muhammad Naveed Ishaque, quietly turning steps into strength  
✍️ Muhammad Naveed Ishaque — the voice behind the journey, making learning feel human  
🔐 From the IronWall Labs — where security is care, and clarity is power.


# Save to a markdown file
file_path_recall = Path("/mnt/data/Lab-14-VMSS-with-CLI-Quick-Recall.md")
file_path_recall.write_text(recall_sheet_content)

file_path_recall.name
