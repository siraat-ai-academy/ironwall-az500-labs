
# 🛡️ Lab 1: Create Azure Resource Locks

---

## 🔮 Scenario Setup

A quiet morning in Denmark. The sky is pale blue, and the air smells like fresh coffee ☕.  
**Mr. eks2** walks into the SikkerCloud office, notebook in hand, eyes full of curiosity.

“Godmorgen!” says **Kasper Madsen**, waving. “Today, we’ll protect your Azure resources like royal jewels.”

**Sofia Zaymera** smiles softly from her screen. “We're going to learn about **resource locks**. They help stop accidental deletion or unwanted changes to your important cloud resources.”

> “So, it's like putting a safety seal on my cloud things?”  
> — Mr. eks2, wide-eyed.

“Exactly!” says Kasper. “Let's begin!”

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🧱 Task 1: Create a Virtual Machine

**Kasper**: “We start by creating a **Virtual Machine** — like your digital computer in the cloud. Think of it as your superhero base!”

> 🖱️ In the **Azure portal**, click **Create a resource**  
> ➕ Select **Virtual Machine**, then **Create**

**Sofia**: “Give your VM a safe name. We’ll call it **NordicVault-VM** and put it in a new **Resource Group** (📦 *ressourcegruppe*) named **DKSec-RG**.”

Here’s what we filled:

- **Resource Group**: DKSec-RG  
- **Virtual Machine Name**: NordicVault-VM  
- **Availability Options**: No infrastructure redundancy required  
- **Security Type**: Trusted launch virtual machines  
- **Image**: Ubuntu Server 20.04 LTS Gen2  
- **Size**: B2s (click *See all sizes*)  
- **Authentication Type**: Password  
- **Username**: DKUser  
- **Password**: StrongPassword@123

Click **Next: Disks >**

On the **Disks** tab:

- **OS Disk Type**: Standard SSD (Locally-redundant Storage)

Click **Review + Create**, then **Create**

> 💬 Mr. eks2: “Why Ubuntu, not Windows?”  
> 🧘 Sofia: “Ubuntu is lighter, faster, and often used for cloud security labs. Plus, it’s open source!”

---

### 🔒 Task 2: Add a Delete Lock to the Virtual Machine

**Kasper**: “Now imagine you don’t want anyone (even yourself!) to accidentally delete this VM. Let’s lock it — like putting a ‘Do Not Delete’ sticker.”

Go to your **Virtual Machine** (NordicVault-VM).  
On the left menu, scroll to **Locks** under **Settings**.

Click **Add**:

- **Lock Name**: VMDeleteLock  
- **Lock Type**: Delete

Click **OK** ✅

> 💬 Mr. eks2: “So this stops people from removing it?”  
> 🌸 Sofia: “Yes — it’s perfect for important resources. Even admins must remove the lock before deletion.”

---

### 📦 Task 3: Add a Read-Only Lock to the Resource Group

**Kasper**: “Now let’s protect the whole box — your **Resource Group** (DKSec-RG). We’ll make it **read-only** so nobody can change anything inside.”

Go to **Resource Groups** > **DKSec-RG**  
Click **Locks** under **Settings**

Click **Add**:

- **Lock Name**: RGReadOnly  
- **Lock Type**: Read-only

Click **OK** ✅

> 💬 Mr. eks2: “This is like putting the whole treasure chest under glass!”  
> 🧘 Sofia: “Beautiful metaphor. Yes — everything inside becomes view-only.”

---

### 🧹 Delete All Resources (Optional Cleanup)

Now that we’re done, you can remove all the resources — **but** you’ll first need to **remove the locks**.

> 🧊 Sofia: “Think of it as unlocking a safe before moving the contents.”

---

## 🌍 Real-World Reflection

In real cloud jobs, people sometimes delete or change things by mistake. These **locks** are simple, powerful tools to protect important systems. For beginners or career-changers, learning to use locks is like learning to save your work — essential for safety and trust in IT.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term         | Danish Word             |
|----------------------|-------------------------|
| Resource Group        | Ressourcegruppe         |
| Virtual Machine       | Virtuel Maskine         |
| Lock                  | Lås                     |
| Delete                | Slet                    |
| Read-only             | Kun læsbar              |
| Settings              | Indstillinger           |
| Disk                  | Disk                    |
| Image (OS)            | Billede (Styresystem)   |
| Username              | Brugernavn              |
| Password              | Adgangskode             |

---

## 🧾 Final Summary (Character Intros)

### 👨‍💼 Muhammad Naveed Ishaque  
Muhammad is a content creator who believes that even shy voices can shine through writing. His work helps beginners feel confident and calm while learning hard things like security and cloud.

### 🛸 Mr. eks2  
Mr. eks2 was once a quiet whisper — now, he is a beginner cloud security trainee in Denmark. He learns slowly, kindly, and deeply. He always asks, “Can this be more human?”

### 🇩🇰 Kasper Madsen  
Kasper is a warm and funny Azure Security Specialist. He believes that labs should be joyful, not scary. He loves guiding new learners, especially by making things feel real and not robotic.

### 🇪🇸 Sofia Zaymera  
Sofia was born in Spain and brings both kindness and clarity to every lab. She understands advanced security concepts, but explains them in soft words, so learners can feel peace while learning.

### 🎓 Siraat AI Academy  
**“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”**  
Siraat is a creative initiative to make hard tech feel easy, especially for those new to IT, from non-tech backgrounds, or from hidden corners of the world.  
Built with purpose. Built for peace.

---

## ✅ Signature Close

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
