
# 🧠 Interview Task – Quick Recall Sheet (Lab 21 – Creating Azure Firewall)

A soft, memory-friendly recall guided by the IronWall Team — making each step feel like a learning moment, not just a task list. 🌷✨

---

🛠️ **Step 1: Created a Virtual Network & Subnets**  
🇩🇰 **Kasper Madsen**: "The **Virtual Network** is like building invisible roads for your Azure town. And each **subnet**? A different district — clean, organized, and safe!"  
🌸 **Sofia Zaymera**: "We remove the default subnet and build intentionally. Each subnet has a role, and that clarity is protection."  
🧠 **I.K.**: "Begin by creating structure — with purpose. Every space holds meaning in the cloud of trust."  
😇 **Maya Lin**: "So the subnets are like little rooms in a house? Cool!"  

---

🛠️ **Step 2: Deployed Two Virtual Machines**  
🇩🇰 **Kasper**: "One VM acts like a guard booth (**Srv-Jump**), and the other — the vault (**Srv-Work**) — is hidden without public access."  
🌸 **Sofia**: "Public exposure is risk. That’s why **Srv-Work** stays in the shadows, with no open ports."  
🧠 **I.K.**: "Access must be earned. We build boundaries not to exclude — but to honor sensitivity."  
🕶️ **ShadowNet**: waits for exposed ports and forgotten RDP settings...  

---

🛠️ **Step 3: Deployed Azure Firewall with Policy**  
🇩🇰 **Kasper**: "This is your digital gatekeeper. Think of the **Firewall** as a wise sentinel that checks every guest before entry."  
🌸 **Sofia**: "The attached **Firewall Policy** ensures all traffic abides by predefined rules — Application, Network, and DNAT."  
🇷🇺 **Elina Petrova**: "I automate firewall and policy setup via Bicep. Repeatable, reliable, and clean."  
😇 **Maya Lin**: "It’s like setting house rules before opening the door. I love that!"  

---

🛠️ **Step 4: Created a Route Table**  
🇩🇰 **Kasper**: "Think of it as a cloud GPS — making sure traffic doesn’t wander, and always goes through the **firewall**."  
🌸 **Sofia**: "Routing mistakes bypass protections. That’s why this step matters so deeply."  
🧠 **I.K.**: "Even light must be guided. The route is as sacred as the destination."  
🕶️ **ShadowNet**: watches when packets slip through unintended roads...

---

🛠️ **Step 5: Added Application Rule to Firewall Policy**  
🇪🇸 **Inky Rihan**: "Let me be clear — if you allow everything, I’ll find my way in. Be precise like this **Allow-Google** rule."  
🇩🇰 **Kasper**: "It’s like saying: ‘Google may pass, others must knock.’ That’s cloud etiquette."  
🇮🇹 **Isabella Konti**: "Descriptive rule names reduce human error. ‘AllowWeb’ makes sense — ‘RuleX’ does not."  
😇 **Maya Lin**: "So it's like writing a guest list for your VM? Sweet!"  

---

🛠️ **Step 6: Added Network Rule to Firewall Policy**  
🇷🇺 **Elina**: "Without DNS, VMs get lost — can’t reach domains. This **UDP:53** rule solves that cleanly."  
🌸 **Sofia**: "Allowing only trusted DNS IPs limits unnecessary exposure."  
🧠 **I.K.**: "Even names need a trusted voice to reveal their meaning. This is digital dhikr."  

---

🛠️ **Step 7: Added DNAT Rule for RDP Access**  
🇩🇰 **Kasper**: "A clever detour — traffic hits the **firewall**, then reroutes to **Srv-Work** via **DNAT**."  
🇪🇸 **Inky**: "But if your DNAT rule isn’t restricted properly? That’s how I slip in."  
🇮🇹 **Isabella**: "People often forget DNAT exists — and attackers remember what admins forget."  
😇 **Maya Lin**: "Ohh! So this lets me reach **Srv-Work** through the firewall? Clever!"  

---

🛠️ **Step 8: Configured Custom DNS on Workload VM**  
🇩🇰 **Kasper**: "Custom **DNS** is like giving your VM a personal phonebook."  
🌸 **Sofia**: "We configure `209.244.0.3` and `0.4` so that name resolution works without going outside unfiltered."  
🇷🇺 **Elina**: "Automate NIC DNS configs where possible. It prevents human error."  
🕶️ **ShadowNet**: thrives in misconfigurations and forgotten DNS paths…

---

🛠️ **Step 9: Tested Firewall Access Control**  
🇪🇸 **Inky**: "Google opens. Microsoft blocks. This test proves the firewall rules are working — and working well."  
🇩🇰 **Kasper**: "Testing is celebration. It’s the part where you know your design didn’t just exist — it lived."  
😇 **Maya Lin**: "Seeing www.microsoft.com blocked felt... oddly satisfying!"  

---

## 🌈 Final Reflection by Mr. Eks2

“I now see how every task was more than a click — it was a lesson in structure, clarity, and protection.  
I’ll remember the Danish word for **flow** — *strøm* — because that’s what this lab gave me: structured strøm.”  

---

## 🔐 Real-World Reflection (BBC Insight)

One weak password destroyed a 158-year-old firm.  
This lab taught us how to place guardrails — from firewall routes to DNS rules — that stop **ShadowNet** before it gets in.  
Never underestimate the weight of one misconfiguration.

📎 [BBC Report – A 158-Year Legacy Lost](https://www.bbc.com/news/articles/cx2gx28815wo)

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
