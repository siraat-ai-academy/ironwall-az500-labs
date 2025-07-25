# 🛡️ Create a Virtual Machine & Add Azure Resource Locks

## 🔮 Scenario Setup

Mr. eks2 had just finished his morning tea in the cozy café near his cloud security office in Denmark. He walked into the Azure Lab Room — a warm space filled with light, learning, and a little bit of Danish hygge.

“Godmorgen, Mr. eks2!” smiled **Kasper Madsen**, waving a cinnamon roll. “Ready to lock down some resources today?”

“Hola and welcome,” added **Sofia Zaymera**, arranging some lab notes. “Today’s lab will teach you how to create a **Virtual Machine** and protect it with **resource locks**. These locks stop others from deleting or changing things by accident. Very useful for security!”

Mr. eks2 nodded, “Let’s begin. But... what’s a lock in the cloud? Do we need keys too?” he asked with wonder.

Kasper chuckled. “Not physical keys — just digital safeguards!”

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🔧 Task 1: Create a Virtual Machine

👨‍💼 **Mr. eks2** entered the **Azure Portal**, eyes wide with curiosity.

🇩🇰 **Kasper**: “Click on **Create a resource**. Choose **Virtual Machine** — or in Danish, *Virtuel Maskine*. Imagine it like building a little server in the sky!”

🇪🇸 **Sofia**: “Let’s use friendly names. Create a **Resource Group** [*ressourcegruppe*] and call it **NordicVault-Resources**. This is like a folder to hold everything.”

👨‍💼 **Mr. eks2**: “So we’re organizing our things before we begin. Like setting up kitchen shelves before cooking?”

🧑‍💼 **Kasper**: “Exactly! Now name your VM: **NordicVault-VM**.”

🧑‍🎓 Sofia added: “Set **Availability Options** to *No infrastructure redundancy required*. Choose **Trusted Launch** for **Security Type** — it gives your VM more protection.”

🧑‍💼 “We’ll use **Ubuntu Server 20.04 LTS Gen2**,” Kasper said. “It’s stable and secure.”

🧑‍🎓 “Pick the **B2s size** — not too big, not too small,” Sofia guided.

👨‍💼 “And for login… I’ll use username **NordicUser** with a strong password!”

🧑‍💼 “Good choice! Now under **Disks**, choose **Standard SSD** — it’s reliable and cost-friendly.”

🎉 Click **Review + Create**, then **Create**. Your Virtual Machine is flying into the cloud!

---

### 🔐 Task 2: Add a Delete Lock to the Virtual Machine

👨‍💼 **Mr. eks2** looked at his new VM. “Now it’s live… but how do we protect it from being deleted?”

🧑‍💼 Kasper smiled: “Go to **Settings > Locks** in the left menu.”

🧑‍🎓 Sofia explained: “Click **Add**, then name the lock: **VMDeleteLock**.”

🧑‍💼 “Set the **Lock Type** to **Delete**. This means no one can delete this VM unless they remove the lock first.”

👨‍💼 “Ah, like a padlock on a bicycle. You can still ride it, but no one can take it!”

🧑‍🎓 “Exactly, mi amigo.”

---

### 🛑 Task 3: Add a Read-Only Lock to the Resource Group

🧑‍💼 Kasper: “Now let’s lock the whole **Resource Group** with a **Read-only lock**. This means people can see, but not change things.”

👨‍💼 “Like a museum display. Look but don’t touch?”

🧑‍🎓 Sofia: “Perfect metaphor. Go to **NordicVault-Resources**, then **Settings > Locks**.”

🧑‍💼 Add a lock called **RGReadOnly** and set type to **Read-only**.

👨‍💼 “Done! Everything feels much safer now.”

---

## 🧹 Clean-Up (Delete Resources)

🧑‍🎓 Sofia reminded: “Now try to delete the **Virtual Machine**… you’ll see the lock stops you.”

🧑‍💼 Kasper added: “To clean up, remove both locks first — then delete the VM and Resource Group.”

👨‍💼 Mr. eks2 smiled, “So locks are like invisible shields. Gentle, but firm.”

---

## 🌍 Real-World Reflection

This lab teaches a very real skill: how to protect cloud resources from accidents or mistakes. In real IT jobs, people often delete things too quickly — these **locks** act like safety nets. If you’re a beginner or switching careers, knowing how to use **resource locks** makes you a trusted guardian of the cloud.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word            |
|------------------------|------------------------|
| Resource Group         | Ressourcegruppe        |
| Virtual Machine        | Virtuel Maskine        |
| Storage Account        | Lagerkonto             |
| Lock                   | Lås                    |
| Read-only              | Kun læsbar             |
| Delete                 | Slet                   |
| Password               | Adgangskode            |
| Username               | Brugernavn             |
| Disk                   | Disk                   |
| Size                   | Størrelse              |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
