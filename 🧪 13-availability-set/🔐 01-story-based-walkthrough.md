
# 🏗️ Lab 13: Creating an Availability Set

### A gentle, story-based guide for Azure beginners  
_Deploying highly available VMs — the cozy way_ ☁️🧡

---

## 🔮 Scenario Setup

👨‍💼 Mr. eks2 walked into the lab with a curious look on his face. “Today feels a little… resilient,” he smiled.  
🇩🇰 Kasper welcomed him with a grin, holding a diagram in one hand and coffee in the other.  
🇪🇸 Sofia nodded warmly, “We’re going to learn how to create something called an **Availability Set** — it keeps your servers cozy even when a rack in the datacenter has a bad day.”

“This lab helps ensure your **Virtual Machines** don’t all go down at once. It’s like putting twins in different rooms so both don’t catch the same cold!” 😄

---

## 🛠️ Step-by-Step with Dialogue

### 🧱 Step 1: Create an Availability Set

**Kasper:** “Alright eks2, go to ‘Create a resource’ and search for **Availability Set**. It’s like booking rooms for your servers in separate parts of the same hotel.”

**Sofia:** “And make sure you choose ‘Use managed disks’ — it helps with performance and alignment.”

**Mr. eks2:** “So we are giving my virtual machines... their own bunk beds but in different corners?”

---

### 💻 Step 2: Deploy the First Virtual Machine (VM-Primary)

**Kasper:** “Now let’s spin up a **Virtual Machine**. Name it something nice, like `DKPrimary-VM`. Choose the availability set you just made.”

**Sofia:** “Choose a secure **Password**, always. Think of it like locking the front door, even if you live in a nice cloud neighborhood.”

**Mr. eks2:** “So this VM lives in our bunk bed, but on the left side of the room, right?”

---

### 💻 Step 3: Deploy the Second Virtual Machine (VM-Secondary)

**Kasper:** “Great! Let’s make a sibling VM — call it `DKSecondary-VM`. Same setup, same availability set.”

**Sofia:** “But this time use a slightly different **Username** — good habit when managing multiple identities.”

**Mr. eks2:** “Ah, now we have two servers, living together but separately. Like flatmates with strong boundaries!”

---

### 🧹 Step 4: Clean Up

**Kasper:** “Once everything is tested, go ahead and delete the **Resource Group**. It’s like checking out of the hotel and leaving no towel behind.”

**Sofia:** “Yes — always clean up your cloud. Unused resources cost money.”

**Mr. eks2:** “Noted. Tidy cloud, tidy mind.”

---

## 🌍 Real-World Reflection

This lab teaches how to ensure **high availability** for critical workloads. If one VM crashes, the other keeps running. It's an essential pattern in cloud infrastructure — and something you'll often be asked to set up in real jobs!

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word         |
|----------------------|---------------------|
| Resource Group       | Ressourcegruppe     |
| Virtual Machine      | Virtuel Maskine     |
| Availability Set     | Tilgængelighedssæt  |
| Region               | Region              |
| Username             | Brugernavn          |
| Password             | Adgangskode         |
| Disk                 | Disk                |
| Managed Disk         | Administreret Disk  |
| Authentication       | Godkendelse         |
| Delete               | Slet                |

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
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
