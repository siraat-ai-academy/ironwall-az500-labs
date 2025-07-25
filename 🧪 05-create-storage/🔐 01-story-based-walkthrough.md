# 🧊 Lab 5: Create a Storage Account

## 🔮 Scenario Setup

Mr. eks2 had just arrived at the glowing Azure Lab Hall nestled in the heart of Denmark. The air smelled like fresh coffee and cloud configurations.

As he adjusted his azure-blue trainee badge, 🇩🇰 **Kasper Madsen** waved from across the room.

> “Ready to make some storage magic today?” Kasper grinned.

🇪🇸 **Sofia Zaymera** smiled warmly, placing a soft hand on a storage blueprint.

> “Today’s journey is all about understanding how and where your data sleeps in the cloud.”

This lab will help you learn how to **create a Storage Account**, **store files**, and **set performance and access rules** — all the things a real cloud security job touches daily. And yes, it’s more fun than it sounds. 😄

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🧩 Task 1: Understand Performance, Redundancy, and Access Tiers

**Kasper** opened a large poster on the wall titled “How Safe is Your Data?”

> “Imagine you own a vault for Viking gold,” he said. “Now, you need to decide where to store it and how many backup vaults you want.”

He pointed to four options:

- **LRS (Locally-redundant storage)** — “Three copies in the same room 🏠.”  
- **ZRS (Zone-redundant storage)** — “Three copies in different city zones 🏙️.”  
- **GRS (Geo-redundant storage)** — “One copy flies across the country ✈️.”  
- **GZRS (Geo-zone-redundant storage)** — “A super combo of zones + geography 🌍.”

**Sofia** added softly, “And remember the temperature of your storage…”

She explained:

- **Hot**: “For everyday items, like coffee cups ☕.”  
- **Cool**: “Things you don’t need often — like winter coats 🧥.”  
- **Cold**: “Stored long-term, like photo albums 📸.”  
- **Archive**: “Deep storage. Like placing it in an ancient scroll room 🏺.”

**Mr. eks2** scribbled notes.

> “So… the cloud is like organizing a digital attic, fridge, and museum — all in one?”

**Kasper** chuckled. “Exactly. And in Danish, we call a **Resource Group** a *ressourcegruppe*!”

---

### 🧩 Task 2: Create a Storage Account

They all gathered around a shared holographic screen.

> “Let’s create our vault!” Kasper said.

**Steps:**

1. In the **Azure Portal**, search for **Storage accounts**.
2. Click **+ Create**.
3. In the **Basics** tab, fill in:
   - **Resource Group**: Select an existing one (e.g., **NordicShield-RG**).
   - **Storage Account Name**: e.g., `nordicvaultstorage`
   - **Region**: **East US**
   - **Performance**: **Standard**
   - **Redundancy**: **Locally-redundant storage (LRS)**

4. Click **Review + Create** → then **Create**.

**Sofia** leaned over.

> “It’s okay to keep defaults at this stage. It keeps things clean.”

**Mr. eks2** nodded slowly.

> “So this is like signing a lease for digital property?”

“Exactly,” Kasper replied. “Welcome to the landlord club.” 🏡

---

### 🧩 Task 3: Create a Blob Container

“Now let’s make a little storage room inside your vault,” said Kasper.

**Steps:**

1. Go to your newly created **Storage Account**.
2. Under **Data Storage**, click **Containers**.
3. Click **+ Container**.
4. Name it `fjordfiles25`, then click **Create**.

**Sofia** reminded, “Containers help separate things. Like folders on your computer.”

> Mr. eks2 smiled, “It’s like putting socks in their own drawer. Tidy!” 🧦

---

### 🧩 Task 4: Upload a Blob Object

Kasper handed Mr. eks2 a task.

> “Create a tiny webpage. Trust me.”

**Steps:**

1. Open **Notepad**.
2. Type: `<h1>This is a sample document!</h1>`
3. Save as `sample.html`.
4. In **Azure Portal**, go to your container `fjordfiles25`.
5. Click **Upload** and select `sample.html`.

**Sofia** whispered, “This is your first **blob** — a digital file that floats in the cloud.”

**Mr. eks2** looked amazed.

> “It’s uploaded! It's like mailing a letter into the sky.” ☁️📨

---

### 🧩 Task 5: Create a File Share

> “Let’s create a digital folder that can be accessed from multiple devices,” said Kasper.

**Steps:**

1. Inside the same **Storage Account**, go to **File shares**.
2. Click **+ File share**.
3. Name it `hyggefiles123`.
4. Choose **Hot access tier**.
5. Click **Create**.

**Sofia** smiled, “Hot tier means it’s ready to serve — like a Danish smørrebrød 🥪.”

**Mr. eks2** nodded.

> “Files with warmth. That’s poetic.”

---

### 🧩 Task 6: Upload a File to File Share

**Steps:**

1. Open the `hyggefiles123` share.
2. Click **Upload**.
3. Select any local file and upload.

**Kasper** said, “There it goes — from your laptop to the digital workplace.”

**Mr. eks2** whispered,

> “I just sent a part of my world into another world…”

**Sofia** softly concluded,

> “And now — we clean up.”

**Final Step:** Delete all resources to avoid charges.

---

## 🌍 Real-World Reflection

This lab teaches you the heart of secure, organized data storage in the cloud. In a real IT job, you'd help teams store data safely, make backups across locations, and choose cost-saving access tiers. This task shows how to protect and organize files — a small action with big impact.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word         |
|----------------------|---------------------|
| Resource Group       | Ressourcegruppe     |
| Storage Account      | Lagerkonto          |
| Virtual Machine      | Virtuel Maskine     |
| Container            | Beholder            |
| Blob                 | Blob                |
| File Share           | Fildeling           |
| Region               | Område              |
| Redundancy           | Redundans           |
| Upload               | Overfør             |
| Performance Tier     | Ydelsesniveau       |

---

## 🧾 Guided by:  
🛸 **Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
🇩🇰 **Kasper Madsen** — a joyful Danish Azure Security Specialist who turns labs into friendly journeys  
🇪🇸 **Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity  
✍️ **Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen  

🔎 See full character bios in the README file.

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
