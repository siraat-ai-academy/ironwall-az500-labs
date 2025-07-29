
# 📘 Reflections After the Lab — Eks2’s Dialogue with ShadowNet  
🧠 *“Threat Modelling Dialogue — Mr. Eks2 Meets ShadowNet”*  
*Human-centered security reflection through story, emotion, and insight.*  

### 🌥️ The Cloud Has Two Voices...

*👨‍💼 **Mr. Eks2** — A kind trainee learning cloud security in Denmark, one careful step at a time.*  
*🕶️ **ShadowNet** — A silent adversary born from forgotten defaults and unchecked assumptions.*

---

The Azure portal was quiet now. All the resources had been provisioned and tested — the ASP.NET app deployed, the database connected, migrations completed. The live app blinked in the browser like a neon sign: “Welcome, task creator.”

Mr. Eks2 leaned back in his chair. This was his nineteenth lab, but it still felt new each time — like standing on the edge of something invisible.

His fingers hovered over the keyboard. Everything had worked. So why couldn’t he shake the sense… that something hadn’t?

A whisper, just behind the silence, rose like static in his mind.

> “You made it accessible to the world... did you mean to?”

Eks2’s eyes narrowed. He hadn’t spoken — but the words had formed all the same. He turned, and the screen flickered. Just for a moment, as if reality had failed to render correctly.

Then came the shape.

🕶️ **ShadowNet.**

It didn’t crawl. It didn't glitch. It simply appeared — like condensation forming from thought itself. ShadowNet was not a threat actor. It was the residue of assumption. It took the form of unguarded ports, forgotten IP rules, overly generous permissions.

Eks2 blinked. “I locked down the database. I tested the app. Everything is fine.”

ShadowNet tilted its head. “Is it? Tell me… what does port 1433 expose?”

Eks2 froze. The SQL database. He had added his client IP to the firewall — but left a broad rule in place for testing.

“It’s temporary,” he said aloud. “I was going to remove it.”

ShadowNet stepped closer, its voice gentle. “Temporary. The cloud does not care. It remembers all settings — even the ones you meant to forget.”

There was no malice in its tone. Only an eerie, teacher-like calm.

“I deployed the app,” Eks2 said again, more defensively now. “It’s working.”

“But does it *protect itself*?” ShadowNet asked.

Eks2 was silent. The app had no outbound monitoring. No alerts on access attempts. The connection string stored credentials — safely, yes, but could someone sniff it? Spoof it?

He swallowed.

“I just needed to get it working.”

ShadowNet nodded. “And so do attackers. They don’t need backdoors. They wait at open ones.”

---

Eks2 reached for the mouse, moved quickly now. He reopened the Network Security Group rules. There it was — **Allow All to SQL**. It stared at him like a forgotten note on the fridge, harmless until it wasn’t.

He deleted the rule.  

ShadowNet didn’t flinch.

“You learn fast,” it said.

Eks2 glanced sideways. “Are you... real?”

“I’m as real as every assumption you’ve ever made in a rush,” ShadowNet replied. “I am your echo in every config file. I am the pause you skip when the deadline ticks louder than your instincts.”

It was not cruel. Just present. Watching. Waiting.

“Then teach me,” Eks2 whispered.

“Already have,” ShadowNet said. “You just needed to feel it.”

---

## 🛡️ Threat Modelling Reflection Table

| 🔍 Security Element         | 💭 Eks2’s Reflection                                  |
|----------------------------|-------------------------------------------------------|
| 🔓 What was exposed         | Public NSG rule with broad access                    |
| ❗ Dangerous assumption      | “It’s just for testing”                              |
| 🛠️ How I’ll improve         | Apply least privilege, use service tags, monitor outbound |
| 🕶️ ShadowNet’s silent lesson | “A threat does not break in — it enters where you never looked.” |

---

> *“You secured the login, but left the gate unlatched. I do not force doors — I find the ones you forgot to check.”* 🕶️  

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
*With the inner voice of Eks2 — the whisper behind the work.*  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_  
