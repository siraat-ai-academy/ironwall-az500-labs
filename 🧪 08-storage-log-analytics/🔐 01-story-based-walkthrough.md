# 📦 Lab 8: Monitor and Troubleshoot Azure Storage with Log Analytics  
_IronWall-az500-labs — Story-based Guide_  
✨ **For beginners, learners, and the ever-curious Mr. eks2**

---

## 🔮 Scenario Setup

As the clouds over Copenhagen softly shift, 👨‍💼 **Mr. eks2** arrives at his next Azure lab.

🇩🇰 **Kasper** waves from the screen, holding his coffee: “Today, we’re going to watch our Azure storage like hawks. Well… gentle hawks.”

🇪🇸 **Sofia** smiles calmly: “We’ll use **Log Analytics** to understand what’s going on inside your storage account. It’s like putting on x-ray glasses, but for cloud files.”

“X-ray glasses? Ooooh,” whispers Mr. eks2 with a grin. “This is going to be fun.”

---

## 🛠️ Step-by-Step Lab (Told as a Friendly Story)

### 🌐 Step 1: Create a Storage Account

**Kasper**: “Let’s build a place to keep our files. We’ll call it **NordicVault-Storage** — think of it as your digital basement.”

**Sofia**: “Make sure the **redundancy** is set to GRS. That means your data is backed up in another region, in case something goes wrong.”

**Mr. eks2**: “A basement… with another secret basement in a different city. I like it.”

---

### 📦 Step 2: Add a Blob Container

**Kasper**: “Inside our basement, we add a **Blob Container** called **monitor-blobs-container**. It’s like a drawer in your storage box.”

**Sofia**: “Containers help organize different types of data. Clean and safe.”

**Mr. eks2**: “One drawer for snacks, another for secrets. Got it!”

---

### 📂 Step 3: Upload Some Test Files

**Kasper**: “Now we drop in a few files — like sending paper notes into the drawer.”

**Sofia**: “Wait between uploads. Azure needs a moment to capture what’s happening. It's like writing journal entries — you can’t write them all at once.”

**Mr. eks2**: “One file, two file… ah, this cloud has patience.”

---

### 📊 Step 4: Create a Log Analytics Workspace

**Kasper**: “Time to build our detective’s desk. This is **Log Analytics** — where all your clues show up.”

**Sofia**: “It collects logs from different Azure services. We’ll name it **log-ncloudwatch-dk**.”

**Mr. eks2**: “A detective’s desk? With sticky notes and magnifying glass?”

---

### 🛠️ Step 5: Connect Diagnostic Settings

**Kasper**: “Now we connect our storage to our desk. That’s done through **Diagnostic Settings**.”

**Sofia**: “We tell Azure what type of data we want — like **StorageRead** — and where to send it (our workspace).”

**Mr. eks2**: “It’s like installing a baby monitor in the storage room. I can hear the files move!”

---

### 📥 Step 6: Download a Blob (Trigger Logs)

**Kasper**: “Let’s poke the system by downloading a file. Just click **Download** on one of the blobs.”

**Sofia**: “That action will generate a log. Azure sees it and writes it down in our workspace.”

**Mr. eks2**: “So even one click gets noticed? This cloud is very watchful.”

---

### 🔍 Step 7: Query Logs with KQL

**Kasper**: “Now the fun part. We ask Azure: ‘Hey, who downloaded that blob?’”

**Sofia**: “Using **Kusto Query Language** — or **KQL** — you can filter by operation and see things like time and user ID.”

**Mr. eks2**: “This feels like opening a guest book and seeing who touched the cookies.”

---

## 🌍 Real-World Reflection

This lab shows how Azure doesn’t just store data — it watches, logs, and reports on every action. Whether you're an admin, auditor, or curious learner, knowing how to track storage access is key to security and troubleshooting. For any IT or cloud job, this kind of visibility is gold.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term              | Danish Word              |
|---------------------------|---------------------------|
| Storage Account           | Lagerkonto                |
| Blob Container            | Blobbeholder              |
| Upload                    | Overfør                   |
| Log Analytics             | Loganalyse                |
| Diagnostic Settings       | Diagnostiske indstillinger|
| Resource Group            | Ressourcegruppe           |
| File                      | Fil                       |
| Query                     | Forespørgsel              |
| Download                  | Hent                      |
| KQL (Kusto Query Language)| KQL (samme på dansk)      |

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
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of eks2 — the whisper behind the work._  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
