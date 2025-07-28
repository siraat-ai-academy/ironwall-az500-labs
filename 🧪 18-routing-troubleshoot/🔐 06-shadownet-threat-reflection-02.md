
# 🌌 Reflections After the Lab — Eks2’s Dialogue with ShadowNet

The sky above Azure’s digital field was quiet. Not a storm, not a glitch, not even an alert beeped. Everything was… working.

The **Virtual Machines** hummed silently in **West Europe**, load balanced to perfection. **MyFrontendIP** responded gracefully to every click, distributing requests between **MyVM1** and **MyVM2** like a practiced conductor.

Mr. Eks2 leaned back in his chair. “Done,” he whispered to no one in particular. But as his hand hovered over the logout button, something flickered across the console — not an error… more like a shadow.

The terminal dimmed slightly. The cursor blinked. Then a line appeared on screen, untyped by any hand:

**“You did everything, except what you didn’t question.”**

Eks2 straightened. “Who’s there?”

From the silence emerged a low pulse, like a heartbeat from the firewall itself. The console darkened, and out stepped a figure built not from code, but from oversight.

### 👤 ShadowNet had arrived.

It wasn’t wearing a hoodie. No wires, no malware. It was more… intimate. Familiar.

> **ShadowNet:** “Why do you leave the door open just because you're home?”  
> **Eks2:** “I closed all inbound ports… except 80.”  
> **ShadowNet:** “And so I entered with respect. Through what you thought was safe.”

Eks2’s screen began flashing diagnostics. The **Network Security Group** had allowed HTTP. Just for this lab. Just for ease. Just for a moment.

> **Eks2:** “But it’s just testing. This isn’t production.”  
> **ShadowNet:** “I don’t attack systems. I inherit assumptions.”

Suddenly, the **load balancer** logs shimmered. Not with errors — but with silence. And that silence? That was ShadowNet's cloak.

> **ShadowNet:** “Session persistence… a convenience. What happens when convenience hardens into habit?”  
> **Eks2:** “I disabled it. Eventually.”  
> **ShadowNet:** “But only after I taught you what sticks when you're not watching.”

A chill ran down Eks2’s spine. It wasn’t fear — it was clarity.

He looked around at his configuration. So many toggles, so many defaults. The story wasn't about open ports — it was about trust. Trusting what Azure configures for you, what tutorials skip, what you think no one will touch.

He whispered, “I get it now.”

> **ShadowNet:** “Good. Because I never needed to breach. I only needed to wait. Behind your unchecked boxes. Beneath your hurried clicks.”

The terminal faded to normal.

Only a single log remained in the system:

> “Audit: SessionPersistenceChanged | Rule Updated | User: eks2 | Reason: ShadowNet”

---

## 🛡️ Threat Modelling Reflection Table

| 🔍 Security Element | 💭 Eks2’s Reflection |
|----------------------|-------------------------|
| 🔓 What was exposed | Public NSG rule with broad access |
| ❗ Dangerous assumption | “It’s just for testing” |
| 🛠️ How I’ll improve | Apply least privilege, use service tags, monitor outbound |
| 🕶️ ShadowNet’s silent lesson | “A threat does not break in — it enters where you never looked.” |

---

### 🧠 Bonus Ending Quote

> **ShadowNet:**  
> “You call me ‘threat’.  
> But I am only what your confidence forgot.” 🕶️  

---

### ✒️ Closing Signature

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
