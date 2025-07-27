# 📄 Interview Task – Quick Recall Sheet (Lab 16 – Understand Network Security Group Rules)

---

## 🔁 Step-by-Step Summary

- **Step 1**: Created a **Resource Group**  
  *(to logically group all Azure resources and manage them together)*

- **Step 2**: Created a **Virtual Machine (VM)**  
  *(to provision a Windows Server 2022 system as a cloud-based host environment)*

- **Step 3**: Disabled **Public Inbound Ports** during VM setup  
  *(to reduce the VM's initial exposure to internet-based attacks)*

- **Step 4**: Added a **Network Security Group (NSG) rule for RDP (Port 3389)**  
  *(to allow remote desktop access — with caution, for management only)*

- **Step 5**: Used **RDP** to connect to the VM securely  
  *(to administer the server and install internal features like IIS)*

- **Step 6**: Installed the **IIS Web Server role** inside the VM  
  *(to host a basic website and validate the server’s web functionality)*

- **Step 7**: Added a second **NSG rule for HTTP (Port 80)**  
  *(to allow public access to the default IIS web page via browser)*

- **Step 8**: Copied the **Public IP Address** and tested the website in a browser  
  *(to confirm network routing, NSG configuration, and IIS availability)*

- **Step 9**: Deleted all resources after testing  
  *(to follow best practices and avoid unnecessary billing or security risks)*

---

## 🧠 Why This Matters (Real-World Relevance)

This lab reinforces the principle of **least privilege**, proper **access control**, and safe **port management**. It demonstrates how NSGs function like cloud firewalls — allowing only the necessary traffic into cloud environments, a fundamental skill for every security-conscious engineer.

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In 2023, a 158-year-old British firm was brought down by one weak password. With no network security layers and unchecked access, attackers took full control.

In this lab, we practiced using **NSGs**, **restricted port access**, and **secure login methods** — which are the very defenses that might have saved that legacy.  
📎 [Read the full story](https://www.bbc.com/news/articles/cx2gx28815wo)

---

## 🧾 Guided by:
✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
