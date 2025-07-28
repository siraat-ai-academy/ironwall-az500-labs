# 🌟 Eks2's “Lab to Soulful Story” — Lab 18: Load Balancing & ShadowNet

---

## 🌸 Meet the Minds Behind the Mission

| Character         | Role & Description                                                    |
|------------------|------------------------------------------------------------------------|
| 👨‍💼 **Mr. Eks2**     | A new Azure security trainee in Denmark — curious, emotional, growing |
| 🇩🇰 **Kasper Madsen** | Timeless cyber-sufi — explains cloud like he's teaching you the stars  |
| 🇪🇸 **Sofia Zaymera** | Warm, soft-spoken Zero Trust expert — always watching what others miss |
| 🌫️ **ShadowNet**     | The silent adversary — never breaks in, only waits where we forget     |

---

## 📖 The Story: "The Balancer’s Mistake"

### Scene 1: Cold Air, Warm Console

The air in the Copenhagen co-working space was chilled but calm. **Mr. Eks2** stared at the screen — **MyVNet**, **MyNSG**, **MyLoadBalancer**… all created, configured, clicking in place.

“Looks beautiful,” he whispered.

“Looks vulnerable,” said a soft voice behind his mind.

He turned. No one was there.

But he had felt it — like a shadow had passed through his firewall.

---

### Scene 2: Kasper’s Candlelight Wisdom

Later that evening, in a small Danish café lit with candles and rain-soaked windows, **Eks2** met **Kasper** and **Sofia**.

“I finished the lab,” said Eks2, “Created the VMs, configured the load balancer, even set the session persistence…”

“Session persistence,” Kasper echoed, stirring his coffee. “It is like inviting one guest to stay forever at your house. Lovely… until the second one knocks.”

Sofia smiled. “That’s why we later turned it off. To let the load balance — truly.”

---

### Scene 3: Hello World, but From Where?

From the Azure Bastion window, Eks2 tested the site. “Hello World from MyVM1…” he refreshed. “Again… MyVM1.”

The page wouldn’t change. Not to MyVM2.

He frowned. “Why won’t it switch?”

From deep within Azure logs, something stirred. A line repeated:  
`SessionAffinity: ClientIP_Protocol`  
A whisper: “Still mine…”

ShadowNet had nested in the comfort of his unchecked assumption.

---

### Scene 4: The Glitch That Wasn’t

Sofia noticed the logs and tilted her head. “It’s not broken,” she said gently, “It’s over-attached.”

Kasper tapped the screen. “Session persistence… lovely for stability. But chaos for distribution. You must choose: comfort or clarity.”

So Eks2 edited the rule. **Changed persistence to None**.

He hit save. Waited. Refreshed.

> “Hello World from MyVM2.”

And then — finally — balance.

---

### Scene 5: The Shadow Between Clicks

But even as joy crept in, a chill returned.

In the Diagnostic Logs, a strange entry:

`ProbeTimeout: 10.1.0.9 unreachable`

Eks2 froze.

“That’s not one of mine.”

ShadowNet was not gone. It had never entered — it had waited. Behind an open NSG rule. Behind a "just for now" exception.

> "I don’t attack," the whisper said again.  
> "I wait where you trust too easily."

---

## 🌍 Eks2’s Final Reflection

“I learned more than just how to configure a Load Balancer,” he wrote in his notes that night.  
“I learned how trust, when placed lazily, becomes an open door.”

He added a line under his notebook:

> “In security, silence isn’t safety. It’s the space between your assumptions.”

And in the margins, he doodled a small shadow — with a smile beneath it.

---

## 🔐 Threat Modelling Reflection Table

| 🔍 Security Element        | 💭 Eks2’s Reflection                                                   |
|---------------------------|------------------------------------------------------------------------|
| 🔓 What was exposed        | **Public NSG rule with broad access**                                  |
| ❗ Dangerous assumption     | “It’s just for testing”                                                 |
| 🛠️ How I’ll improve        | **Apply least privilege, use service tags, monitor outbound traffic**   |
| 🕶️ ShadowNet’s lesson       | “A threat does not break in — it enters where you never looked.”        |

---

## 🧠 Whispered Words from the Edge

> “I am not a hacker.  
> I am your forgotten configuration —  
> sipping tea on port 80.”

🕶️ — ShadowNet

---

### ✒️ Closing Signature

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
