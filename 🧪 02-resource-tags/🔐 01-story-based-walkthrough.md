# 🏷️ Organizing Azure Resources with Tags  
_IronWall-az500-labs | Lab 02_

---

## 🔮 Scenario Setup

👨‍💼 **Mr. eks2** stepped into the Azure Lab Room once again — today with a curious twinkle in his eyes. "What do we do with all these cloud things? How do we keep them organized?"

🇩🇰 **Kasper** grinned, holding up a label maker. “We tag them, my friend! Like putting name stickers on your lunchbox.”

🇪🇸 **Sofia** nodded, “Yes — tags help you find, manage, and report on Azure resources, especially in big companies.”

💡 “This lab will teach you how to create a **Virtual Machine**, add a **tag**, and filter based on that tag — so you can organize like a pro.”

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🖥️ Task 1: Create a Virtual Machine

🇩🇰 **Kasper**: “Let’s start by creating a new **Virtual Machine** — this time we’ll call it **DKResize-VM**. Click **+ Create > Azure Virtual Machine**.”

🇪🇸 **Sofia**: “Place it in a **Resource Group** [*ressourcegruppe*] named **DKCloudLab-RG**. Choose **Windows Server 2019** as the image. For size, pick **B1s** — small and efficient.”

👨‍💼 **Mr. eks2**: “Sounds like we’re building a cozy little workstation in the cloud. Do I need to turn on the ‘Spot Instance’ thing?”

🇪🇸 **Sofia**: “Nope, leave it off for now — that’s for special cost-saving situations.”

🇩🇰 **Kasper**: “Give it a username and a strong password. Then choose **Standard SSD** for the disk — fast, simple, and affordable. Then hit **Create**!”

---

### 🏷️ Task 2: Apply Tags to the Virtual Machine

👨‍💼 **Mr. eks2** stared at the Azure Portal. “Okay, I made the VM… now how do I tag it? Do I just say ‘Hi, I name you’?”

🇩🇰 **Kasper** chuckled: “Almost! Go to **Settings > Tags** on your VM. Add a tag like this: **Name: Department**, **Value: IT**.”

🇪🇸 **Sofia** added: “Tags are like metadata — invisible labels that help you sort and manage. It’s not just for fun — many companies use them to track billing and ownership.”

👨‍💼 “So it’s like saying ‘This VM belongs to the IT team.’ Smart!”

---

### 🔍 Task 3: Filter Resources by Tag

🇩🇰 **Kasper**: “Now let’s test your tag! Go back to **Resource Groups**, pick **DKCloudLab-RG**, and click **Add filters**.”

🇪🇸 **Sofia**: “Select the tag: **Department = IT**. Then click **Apply** — and voila, your VM appears.”

👨‍💼 “Ahh! It’s like a magic search trick for the cloud. I want to tag everything now!”

---

### 🧹 Clean-Up Time

🇪🇸 **Sofia**: “When you’re done, delete all the resources — it keeps your environment clean and safe.”

---

## 🌍 Real-World Reflection

This lab is all about staying organized in Azure. In the real world, companies have hundreds of resources — and tags help sort them like folders, track costs, and apply rules. If you're switching to cloud or just starting, tagging is a superpower you'll use every day.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word            |
|------------------------|------------------------|
| Resource Group         | Ressourcegruppe        |
| Virtual Machine        | Virtuel Maskine        |
| Tag                    | Mærkat                 |
| Filter                 | Filter                 |
| Department             | Afdeling               |
| Value                  | Værdi                  |
| Username               | Brugernavn             |
| Password               | Adgangskode            |
| Create                 | Opret                  |
| Delete                 | Slet                   |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
