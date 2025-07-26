
# 📊 AZ-500 Diagram + Friendly Breakdown  
**Lab 13: Creating an Availability Set**

---

## 🧱 Text-Based Diagram: High Availability Setup in Azure

```
+-----------------------+
|   Resource Group      |
|   DKInfra-RG          |
+-----------------------+
           |
           v
+-----------------------+
|   Availability Set    |
|   DK-HighAvail-Set01  |
+-----------------------+
     |             |
     v             v
+------------------+     +-------------------+
|  Virtual Machine |     |  Virtual Machine  |
|  VM-Nordic01     |     |  VM-Nordic02      |
+------------------+     +-------------------+

All VMs use:
- OS: Ubuntu Server
- Disk: Standard SSD
```

---

## 🎭 Diagram Story – Let's Walk Through It Together

👨‍💼 **Mr. eks2** (sipping tea): “Kasper, Sofia… I just finished this lab, but I’m still not sure why we built this little Azure fortress. What’s really going on?”

---

### 🔹 **Resource Group**  
🇩🇰 **Kasper**: “Ah, the **Resource Group** is like a shared lunchbox 📦. Everything in your lab—VMs, disks, even that cool **Availability Set**—lives inside this one container. In Danish, we call it a *ressourcegruppe*.”

🇪🇸 **Sofia**: “Yes, and remember: managing permissions at the **Resource Group** level makes life simpler and more secure.”

🛸 **Mr. eks2**: “So it’s like a folder in the cloud… with security rules? I can handle that!”

---

### 🔹 **Availability Set**  
🇩🇰 **Kasper**: “This is Azure’s version of not putting all your eggs in one basket. Imagine two pizza ovens 🍕 in different rooms—if one fails, the second keeps baking! That’s your **Availability Set**.”

🇪🇸 **Sofia**: “It ensures your **Virtual Machines** are placed in separate update and fault domains. This protects against hardware failure and planned maintenance.”

🛸 **Mr. eks2**: “Nice! So it’s like cloud-level redundancy with a touch of culinary flair.”

---

### 🔹 **Virtual Machines**  
🇩🇰 **Kasper**: “Meet **VM-Nordic01** and **VM-Nordic02**. These are your twin warriors ⚔️! One holds the fort, the other is the backup dancer. Both run Ubuntu, quietly doing their job.”

🇪🇸 **Sofia**: “Always use strong passwords for your VM users. And only open the ports you truly need.”

🛸 **Mr. eks2**: “They sound brave… and a little overworked. But safe, yes?”

---

## 🌍 Final Takeaway

This diagram shows how Azure ensures uptime and resilience. By placing **Virtual Machines** inside an **Availability Set**, you protect services from going down if a server fails. It’s a foundational pattern in high-availability architecture—especially useful in enterprise or mission-critical environments.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term          | Danish Word          |
|-----------------------|----------------------|
| Resource Group        | Ressourcegruppe      |
| Virtual Machine       | Virtuel Maskine      |
| Availability Set      | Tilgængelighedssæt   |
| Disk                  | Disk                 |
| Region                | Område               |
| Password              | Adgangskode          |
| User                  | Bruger               |
| Server                | Server               |
| Operating System      | Operativsystem       |
| Network               | Netværk              |

---

### 🧾 Guided by:
🛸 **Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
**🇩🇰 Kasper Madsen** — a joyful Danish Azure Security Specialist who turns labs into friendly journeys  
**🇪🇸 Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity  
**✍️ Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen  
🔎 See full character bios in the README file.

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
