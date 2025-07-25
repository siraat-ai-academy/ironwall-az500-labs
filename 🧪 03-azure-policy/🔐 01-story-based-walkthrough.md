# 🛡️ Creating and Testing Azure Policies  
_IronWall-az500-labs | Lab 03_

---

## 🔮 Scenario Setup

👨‍💼 **Mr. eks2** arrived in the Azure Lab Room with a curious look. “Today feels like… policy day?”

🇩🇰 **Kasper** winked, “You bet! Today, we’re the rule-makers — Azure-style.”

🇪🇸 **Sofia** smiled warmly, “This lab shows how to control where resources can be created. It’s like drawing digital borders, to protect and organize your cloud.”

🧠 “In real jobs, this keeps things compliant and clean — no surprise VMs popping up in random places.”

---

## 🛠️ Step-by-Step with Story & Dialogues

### ✍️ Step 1: Create a Policy Assignment to Allow Only UK South

🇩🇰 **Kasper**: “Open the **Policy** service in the Azure Portal. Think of this as the Azure Rulebook.”

👨‍💼 **Mr. eks2**: “So… we’re writing laws for the cloud today?”

🇪🇸 **Sofia**: “Exactly. Now click the **Scope selector** — the three little dots. Choose your **Resource Group** [*ressourcegruppe*] — let’s say **DKCloudSecure-RG**.”

🇩🇰 **Kasper**: “On the left, go to **Definitions**, then search ‘**Allowed locations**’. This built-in policy lets us pick where people can create resources.”

👨‍💼 **Mr. eks2**: “So we’re saying, ‘Only in UK South, nowhere else’? Like giving out party invites to just one city?”

🇪🇸 **Sofia**: “Yes, and it’s for good reason. Companies often need to meet data residency rules.”

📋 Set:
- **Assignment Name**: *Allow UK South for DKCloudSecure-RG*
- **Description**: *Allow resources to be created in UK South only*
- **Enforcement**: Enabled ✅

🔽 Then choose **UK South** from the **Allowed locations** dropdown.  
Click **Review + Create**, then **Create**. 🎉 You’re officially a Policy Enforcer now.

---

### 🚧 Step 2: Test the Policy with a Virtual Network

🇩🇰 **Kasper**: “Let’s try to break the rule — just to see if it works!”

👨‍💼 **Mr. eks2**: “Ooooh, I love testing limits…”

🇪🇸 **Sofia**: “Search for **Virtual Networks**, click **+ Create**, and set up a new one. Put it in the same **Resource Group** and name it something friendly — like **NordicNet-VNet**.”

🇩🇰 **Kasper**: “Now try setting the **Region** to **East US** — anywhere *except* UK South.”

💥 Validation fails. ❌

👨‍💼 **Mr. eks2**: “Ah! The cloud said nope. The error says the location is not allowed by policy.”

🇪🇸 **Sofia**: “Perfect. That’s the policy doing its job.”

👨‍💼 “Let me try again with **UK South**... and yes! It works! I love when cloud rules are kind.”

---

### 🧹 Clean-Up Time

🇪🇸 **Sofia**: “Now delete the virtual network and remove the policy if you no longer need it. Clean cloud, happy cloud.”

---

## 🌍 Real-World Reflection

This lab shows how **Azure Policy** helps organizations set rules and stay in control. By limiting resource locations, companies protect data, stay compliant with laws, and avoid surprises. For beginners and job switchers, learning this skill builds trust — and shows that you understand both security and structure.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word            |
|------------------------|------------------------|
| Policy                 | Politikker             |
| Resource Group         | Ressourcegruppe        |
| Virtual Network        | Virtuelt netværk       |
| Location               | Placering              |
| Region                 | Region                 |
| Allowed                | Tilladt                |
| Assignment             | Tildeling              |
| Description            | Beskrivelse            |
| Create                 | Opret                  |
| Delete                 | Slet                   |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
