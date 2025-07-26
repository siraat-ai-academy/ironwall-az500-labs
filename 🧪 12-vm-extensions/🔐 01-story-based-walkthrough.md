# ☁️ Lab 12: Deploying Software with VM Extensions — Friendly Story Mode

## 🔮 Scenario Setup

Mr. eks2 walked into the Azure lab with a coffee in one hand and curiosity in the other.

**Kasper** smiled, “Today, we’ll learn how to let Azure do the installing for us — with VM Extensions!”

**Sofia** nodded softly, “It’s like giving instructions to your virtual assistant — and she sets up your machine for you.”

Mr. eks2 whispered, “That sounds… magical.”

---

## 🛠️ Step-by-Step with Friendly Characters

### 🖥️ Step 1: Create the Virtual Machine

**Kasper**: “Let’s spin up a new **Virtual Machine**! Think of it like preparing a hotel room — you pick the location, the bed type, and who gets the key.”

We named ours **NordicOps-VM**, inside the **DKCloud-RG** [ressourcegruppe]. It's in East US and runs **Windows Server 2019**.

**Sofia**: “And always use strong passwords and enable secure access. Think of your VM like a vault — keep it safe.”

**Mr. eks2**: “So I’m basically making a tiny computer in the cloud?”

**Kasper**: “Exactly! And this one even runs on a **Standard SSD** — not bad for a cloud flat!”

---

### 🔧 Step 2: Add VM Extension for Software Deployment

**Sofia**: “Now we give our VM an upgrade — we install a **VM Extension**.”

**Kasper**: “It’s like telling the hotel staff, ‘Please put fresh towels and install the minibar plugin!’” 😄

We used the **Network Watcher Agent for Windows** — a handy tool to help us monitor networking inside the VM.

**Mr. eks2**: “And we don’t need to RDP to do that? It just installs by command?”

**Sofia**: “Correct. It’s automatic — like a silent butler.”

---

### 🔐 Step 3: Remote Desktop into the VM

**Kasper**: “Okay! Time to visit the room we prepared.”

We connected to **NordicOps-VM** using **RDP** (Remote Desktop Protocol).

**Sofia**: “Remember to always verify you’re using the correct public IP and use a secure login.”

**Mr. eks2**: “Feels like teleporting to another machine… from inside my own!”

---

### 🕵️ Step 4: Verify the Software Was Deployed

Inside the VM, we opened **Server Manager**, clicked **Tools**, and checked **Services**.

There it was — **Azure Network Watcher Agent** running nicely!

**Kasper**: “Job done, minibar stocked, agent running.”

---

### 🧹 Step 5: Delete the Resources

**Sofia**: “As always, clean up when you’re done — remove all the deployed resources.”

**Mr. eks2**: “So the room gets checked out, and the hotel doesn’t charge extra — smart!”

---

## 🌍 Real-World Reflection

This lab shows how you can automate software deployment in Azure using **VM Extensions** — a skill that’s key in modern DevOps and cloud security. For job switchers and beginners, it teaches how to manage cloud machines efficiently without logging into each one manually.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term             | Danish Word           |
|--------------------------|------------------------|
| Virtual Machine          | Virtuel Maskine        |
| Resource Group           | Ressourcegruppe        |
| Network Interface Card   | Netværkskort           |
| Disk                     | Disk                   |
| Server                   | Server                 |
| Remote Desktop Protocol  | Fjernskrivebord        |
| Network Watcher          | Netværksovervågning    |
| Agent                    | Agent                  |
| Extension                | Udvidelse              |
| Windows OS               | Windows Styresystem    |

---

### 🧾 Guided by:
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
