
# 🛡️ IronWall Lab 21 — Azure Firewall Architecture: A Text-Diagram & Story Walkthrough 🌸

> _A storytelling journey through the heart of Lab 21 — brought to life by the IronWall Team._

---

## 💬 A Soft Scene at the Whiteboard

The sun was shy, peeking softly through the glass walls of Siraat AI Academy. The lab had ended. A kettle hummed. Laughter lingered in the air like incense.

**Mr. Eks2** sat cross-legged on the wooden floor, gazing up at the whiteboard.

A diagram was drawn there — lines and boxes, arrows and labels.

He smiled softly.  
> “This looks... nice. But what does it all mean?”

**Sofia** stepped forward with her usual grace.  
**Kasper** cracked his knuckles and beamed.  
**I.K.** closed his eyes as if listening to the wind.

And together, the team began to speak...

---

## 🖼️ Azure Firewall Lab — Text-Based Diagram

```
+------------------------+
|     RG-NordicShield   |
+------------------------+
           |
           v
+------------------------+
|     VNet-NordicCloud   |
| Subnets:               |
| - AzureFirewallSubnet  |
| - Workload-SN          |
| - Jump-SN              |
| - AzureFirewallMgmt-SN |
+------------------------+
           |
           v
+------------------------+        +------------------------+
| VM-NordicJump          | <----> | Azure Firewall         |
| Subnet: Jump-SN        |        | Public & Mgmt IP       |
| RDP Allowed (3389)     |        | Policy: LabPolicy      |
+------------------------+        +------------------------+
           |                                |
           v                                |
+------------------------+        +------------------------+
| VM-NordicWork          | <----> | Firewall Rules:        |
| Subnet: Workload-SN    |        | - App Rule: AllowWeb   |
| Custom DNS Config      |        | - Net Rule: AllowDNS   |
| No Public IP           |        | - DNAT: RDP to Work VM |
+------------------------+        +------------------------+
           |
           v
+------------------------+
| Route Table: FW-Route  |
| Next Hop: Firewall IP  |
+------------------------+
```

---

## 🎭 Diagram Walkthrough — With the Full Team

### 🧱 **1. Resource Group & VNet**

**🇩🇰 Kasper**: “Imagine the **Resource Group** as a cloud folder — holding all your secrets. And the **Virtual Network**? That’s your cloud village, with invisible walls drawn in IP ink.”

**🇪🇸 Sofia**: “Each **subnet** has a purpose — isolate them with care. The **AzureFirewallSubnet** must be perfectly named, or the firewall won’t listen.”

**🇵🇰 I.K.**: “Structure reflects sincerity. A VNet reminds us — true protection begins with how you arrange your space.”

**🇨🇳 Maya Lin**: “So... it’s like building tiny towns inside a sky-city? I love it already!”

**🇷🇺 Elina Petrova**: “Bicep templates make these subnets bloom on command. Automation makes the architecture sacred.”

**🇮🇹 Isabella Konti**: “Without subnet clarity, people get lost. And when people get lost... so does security.”

**🇪🇸 Inky Rihan**: “If you let subnets bleed into each other? I’ll be dancing across them before you notice.”

---

### 🖥️ **2. VMs: Jump and Work**

**🇩🇰 Kasper**: “Two VMs, two roles: **NordicJump** is the guarded gate; **NordicWork** is the treasure chest.”

**🇪🇸 Sofia**: “We expose **Jump** — but not **Work**. Never give your secrets a public door.”

**🇵🇰 I.K.**: “In life and in the cloud — access is earned, not assumed.”

**🇷🇺 Elina**: “No public IP on **Work VM**. I enforce that in policy. It's not a suggestion — it’s a rule.”

**🇮🇹 Isabella Konti**: “Users forget they exposed something. That’s why we protect them from their own shortcuts.”

**🇪🇸 Inky Rihan**: “An open RDP port is an open invitation. If I see port 3389 exposed, I’m already in.”

**🇨🇳 Maya Lin**: “So RDP is like... remote magic? But only for one VM? Ooh, okay!”

---

### 🔥 **3. Azure Firewall & LabPolicy**

**🇩🇰 Kasper**: “Think of **Azure Firewall** as your castle gate — a wise guardian that reads every packet like a poem.”

**🇪🇸 Sofia**: “With **Firewall Policy**, we say: Google may enter, Microsoft must wait. This is care, not control.”

**🇵🇰 I.K.**: “Firewalls reflect divine balance. What enters is what we allow. No more, no less.”

**🇷🇺 Elina**: “I script firewall rules using JSON or Bicep — so they’re replicable, auditable, and... beautiful.”

**🇮🇹 Isabella Konti**: “Too many rules confuse people. So we name them with feeling — 'AllowGoogle', not 'Rule1234'.”

**🇪🇸 Inky Rihan**: “Vague rules? Generic names? No logging? You just drew me a map to your soul.”

**🇨🇳 Maya Lin**: “Firewall is like... the doorman of a cloud party? Cool!”

---

### 🧭 **4. Route Table**

**🇩🇰 Kasper**: “A **Route Table** tells your traffic where to walk. 'No shortcuts! Speak to the firewall first.'”

**🇪🇸 Sofia**: “If you skip this, your VM might talk to the internet directly. That’s like whispering secrets in a crowd.”

**🇵🇰 I.K.**: “Without direction, even light gets lost.”

**🇷🇺 Elina**: “I always bind route tables in the script. No manual clicks. Precision is poetry.”

**🇮🇹 Isabella Konti**: “People don’t always understand routing. That’s okay. We build systems that protect anyway.”

**🇪🇸 Inky Rihan**: “Misroute your packets? I’ll catch them mid-air.”

---

### 🌐 **5. Custom DNS Configuration**

**🇩🇰 Kasper**: “Without DNS, your VM doesn’t know where ‘google.com’ lives. It’s like forgetting someone’s name.”

**🇪🇸 Sofia**: “We added `209.244.0.3` — a reliable DNS server. Always know who you trust.”

**🇵🇰 I.K.**: “Names are sacred. DNS is your VM asking: 'What is the true name of this place?'”

**🇨🇳 Maya Lin**: “So DNS is like... asking for directions? Aww!”

**🇷🇺 Elina**: “I inject DNS into NIC configurations with Bicep. It saves time. It saves mistakes.”

**🇮🇹 Isabella Konti**: “Confusion leads to fear. When DNS breaks, humans panic. So we pre-plan the calm.”

---

## 🌟 Final Reflection by Mr. Eks2

He traced the lines on the board with his finger.

> “Now I see it.  
> It’s not just machines and boxes… it’s roles, relationships, rituals.  
> Like any good team, they each do their part — and trust each other.”

In his Danish notebook, he wrote:

- Virtual Machine = **Virtuel Maskine**  
- Firewall Policy = **Firewallpolitik**

He smiled softly. The board no longer looked like a diagram.  
It looked like a story.

---

## 🔐 Real-World Reflection: A 158-Year Legacy Lost

One weak password — one forgotten setting — that’s all it took to end a legacy of 158 years.

This diagram, though simple, is a reminder: **structure is safety**.  
Every **NSG**, every **Firewall Rule**, every **Subnet** must be crafted with care.

> Behind every config is a company, a family, a future.

📖 Inspired by: [BBC Report – A 158-Year Legacy Lost](https://www.bbc.com/news/articles/cx2gx28815wo)

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
