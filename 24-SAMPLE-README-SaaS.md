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

# 📊 Corrected Mermaid Diagram

```mermaid
flowchart TD
    A[Policy Assigned to Resource Group] --> B{Deployment Request}
    B -->|Wrong Region (East US)| C[Denied]
    B -->|Approved Region (UK South)| D[Allowed]
```

## 📝 Key Takeaways
- Azure Policy enforces **rules consistently** across the cloud.  
- Location restrictions help ensure **compliance and predictability**.  
- Simple to apply, powerful for governance.  

---

## 📚 Glossary
- **Resource Group** → Container for related resources.  
- **Policy Assignment** → Binding a rule to a scope.  
- **Allowed Locations** → Defines regions where resources can/cannot be deployed.  

---

✒️ *Created by Muhammad Naveed Ishaque (Eks2)*  
*Technical Writer | AI & SaaS Documentation Specialist*  
