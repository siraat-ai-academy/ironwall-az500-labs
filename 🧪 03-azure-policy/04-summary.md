# 🛡️ Azure Policy — Allowed Locations Example

## 📖 Overview
This document explains how to use **Azure Policy** to enforce location restrictions for resource deployment.  
By applying an *Allowed Locations Policy*, organizations can control where resources are created, ensuring compliance with company or regulatory requirements.

---

## 🎯 Use Case
- Prevent resources from being deployed in regions outside approved locations.  
- Ensure compliance with **governance, security, and legal standards**.  
- Example: Allow deployments only in **UK South**, block deployments in **East US**.

---

## 🚀 Steps
1. **Assign Policy**  
   - Assign the *Allowed Locations Policy* to the target **Resource Group**.  

2. **Test in Wrong Region**  
   - Try to create a **Virtual Network** in `East US`.  
   - Azure blocks the request → *policy enforcement confirmed*.  

3. **Test in Approved Region**  
   - Create the same Virtual Network in `UK South`.  
   - Azure allows deployment → *policy validated*.  

---

## 📊 Diagram
```mermaid
flowchart TD
    A[Policy Assigned to Resource Group] --> B{Deployment Request}
    B -->|Wrong Region (East US)| C[Denied ❌]
    B -->|Approved Region (UK South)| D[Allowed ✅]
