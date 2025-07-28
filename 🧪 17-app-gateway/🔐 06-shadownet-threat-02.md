# 🧠 Threat Modelling Dialogue — Mr. Eks2 Meets ShadowNet
### ✨ Human-centered security reflection through story, emotion, and insight

---

## 📘 Section Title:
### “Reflections After the Lab — Eks2’s Dialogue with ShadowNet”

---

## 🔍 Introduction
At the end of **Lab 17: Creating an Application Gateway**, all steps were completed successfully. The **Virtual Network** was built. **VMs** were deployed. **IIS roles** configured. The **Application Gateway** was routing traffic perfectly.

And yet, as the browser confirmed success, a cold breeze passed through the digital silence.

There was no error.
There was no alert.
But there was a presence.

In that moment, Mr. Eks2 felt it again:

**ShadowNet**. 

Not a bug. Not a person. But the echo of unchecked assumptions. 

It doesn’t break in. 
It waits for us to skip a step, to leave a port too open, or trust a default too blindly.

Tonight, it returned.

---

## 🎭 Dialogue: Mr. Eks2 vs. ShadowNet

> **Eks2:** I followed every step. The gateway works. So why are you here?

> **ShadowNet:** Because you followed... quickly.

> **Eks2:** What do you mean?

> **ShadowNet:** Two public-facing VMs. Both reachable. No WAF. No custom probe. You built a path...

> **Eks2:** ...and forgot to guard it.

> **ShadowNet:** You let the browser tell you it's safe. But not the logs.

> **Eks2:** I was going to monitor it tomorrow.

> **ShadowNet:** Tomorrow is when I move in.

> **Eks2:** Not this time.

> **ShadowNet:** We'll see. Next time... hide the webroot. Encrypt the path.

> **Eks2:** I will. And I’ll check every default before I hit ‘Create.’

> **ShadowNet:** Now you’re thinking like a defender.

---

## 🛡️ Threat Modelling Reflection Table

| 🔍 **Security Element** | 💭 **Eks2’s Reflection** |
|---------------------|----------------------|
| 🔓 What was exposed | Public VMs with open HTTP & RDP ports |
| ❗ Dangerous assumption | “It’s just a quick test environment.” |
| 🛠️ How I’ll improve | Use private subnets, lock NSGs, apply WAF, review logs |
| 🕶️ ShadowNet’s silent lesson | “The gateway you build for others, I walk through first.” |

---

## 🧠 Bonus Ending Quote by ShadowNet
> “I am not malware. I am misjudgment. 
Every default left unchanged is a door I remember.”

---

### ✒️ Created & Curated by
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
