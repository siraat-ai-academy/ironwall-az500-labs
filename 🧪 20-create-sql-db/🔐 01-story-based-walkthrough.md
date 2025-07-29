
# 🧠 IronWall Lab 20: Create a SQL Database  
*A story-based beginner lab — full of joy, clarity, and little wonders in the cloud.*  

---

## 🌟 Meet the Minds Behind the Mission

| 🌍 Character       | 🎭 Role Description |
|-------------------|--------------------|
| 🇵🇰 **I.K.** | The Unseen Mentor — quiet, poetic strategist of trust and security. |
| 🇩🇰 **Mr. eks2** | The Curious Whisper of the Cloud — new in Denmark, soft-spoken learner. |
| 🇪🇸 **Sofia Zaymera** | The Calm Guardian of Clarity — makes Azure feel like gentle poetry. |
| 🇩🇰 **Kasper Madsen** | The Joyful Admin — explains with smiles, scripts, and strong coffee. |
| 🇪🇸 **Inky Rihan** | The Red Team Phantom — uncovers what others forget to lock. |
| 🇷🇺 **Elina Petrova** | The Cloud Whiz — brings beauty to Bicep and automation. |
| 🇮🇹 **Isabella Konti** | The Empathic Firewall — defends like a therapist, loves humans first. |
| 🇨🇳 **Maya Lin** | The Security Rookie — learns with awe, speaks with spark. |
| 🕶️ **ShadowNet** | The Phantom Adversary — hides in “default settings” and forgotten configs. |

---

## 🌥️ Scene: Eks2 Arrives at the Lab  

**Mr. eks2** walked into the cozy Azure training room, notebook in hand, eyes wide.  
Today’s mission? Create his very first **SQL Database**.  

**Kasper** greeted him with a cheerful grin and a cinnamon pastry.  
**“We’re building memory today, Eks2. Not for us, but for the cloud!”**  

**Sofia** joined, wrapping her scarf gently.  
**“And with memory comes responsibility,”** she whispered. **“Let’s begin softly.”**

---

## ☁️ Step 1: Create the Database — With Gentle Hands  

**Kasper** guided, “Click **Create a Resource**, then **Databases → SQL Database**. Choose a name that sings — like `NordicVaultDB`.”  

**Eks2** paused.  
> “Why do we choose names so carefully?”  

**Sofia** smiled. “Because in the cloud, names are like spells. They open doors and define identities.”  

They selected an existing **Resource Group [ressourcegruppe]**, chose **East US**, and clicked to create a **new SQL Server**.

---

## 🔐 Step 2: Server Setup — The Brain Behind the Curtain  

**Kasper** pointed:  
“Choose **SQL authentication**, and pick a **Server Admin** name — maybe `DbGuardian`.”  
“Give it a strong password — the kind that ShadowNet can’t guess in a thousand years.”  

> “What does the location mean?” Eks2 asked.  

**Sofia**: “It’s where your cloud heart lives. Always place it close to the people who’ll use it.”  

They selected **Basic tier** under **Compute + Storage**, and chose **Locally-redundant backup**. Simple. Sufficient. Safe.

---

## 🌐 Step 3: Network Settings — The Gatekeeper  

Now they reached the **Networking tab**.  

**Kasper**: “We choose **Public Endpoint** but guard it. It’s like giving your house an address, but locking the door.”

**Sofia** added softly:  
“Later we’ll limit access — just your **IPv4** and some trusted Azure services.”  

They reviewed. They created.  
**Eks2** took a deep breath. “It’s real now.”  

---

## 🔎 Step 4: Strengthen the Castle Walls  

After deployment, they opened the SQL Server’s **Networking settings**.  

**Sofia** explained:  
“Change **Public network access** to **Selected networks**. Add your own IP. Then tick the Azure box to let trusted friends in.”  

**Eks2** clicked **Save**, then whispered:  
> “Every lab feels like locking a new door.”

---

## 🧾 Step 5: Enter the Query Editor — Write the Story of Tables  

They opened the **Query Editor** and signed in with the SQL Admin.  

**Maya Lin** leaned over.  
**“Now we write the chapters. Tables are like pages. Each row, a story.”**

**Eks2** pasted the SQL script — and four beautiful tables emerged:  

- `person`  
- `student`  
- `course`  
- `credit`

**Sofia**: “These relationships? They protect meaning. Each foreign key, a thread of trust.”

---

## 🕶️ ShadowNet Moves...  

As they reviewed the tables, a slight lag blinked in the dashboard.  

**Inky Rihan** appeared from the corner.  
**“Did you disable anonymous query access?”**  

**Eks2** shook his head.  

🕶️ **ShadowNet** whispered in the logs:  
> “I don’t need a password. I just need what you forgot to check.”  

**Eks2** corrected the settings quickly — and watched the darkness fade.

---

## 🧹 Final Step: Clean Up Gently  

They deleted the **Resource Group**, sweeping all traces of the lab — clean cloud, clear conscience.  

**I.K.** spoke quietly from the hallway:  
**“A database is not just data. It is memory with power. Guard it like a soul.”**

---

## 🌍 Real-World Reflection  

This lab teaches more than SQL. It shows how to shape access, configure servers, and protect databases from being wide open to the world. For new learners and career changers, it’s a reminder: every database is a heartbeat — one mistake could echo far.

---

## 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password  

In 2024, the 158-year-old firm **Wilko** collapsed — not from hackers, but from a **single compromised password**. That’s all it took.  
This lab reminds us why configuring network access, using strong credentials, and limiting public exposure is vital. What you protect today, could save a legacy tomorrow.  
📎 [BBC Report on Wilko collapse](https://www.bbc.com/news/articles/cx2gx28815wo)

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
*With the inner voice of Eks2 — the whisper behind the work._  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
