
# 🧠 Reflections After the Lab — Eks2’s Dialogue with ShadowNet  
### Lab 17: Creating an Application Gateway

---

## 🕶️ ShadowNet Appears…  
*Scene: The screen is still. The Application Gateway is running. Yet something… breathes in the silence.*

**Eks2:** I created a gateway for traffic. Clean, efficient. But is it secure?  
**ShadowNet:** You created a gateway, yes. But for whom?  
**Eks2:** I chose port 80. Everyone uses it.  
**ShadowNet:** Everyone… including me.  
**Eks2:** But there was no login screen. No passwords exposed.  
**ShadowNet:** And yet… I walk where the headers forget to encrypt.  
**Eks2:** I limited subnets. I assigned rules.  
**ShadowNet:** But did you _observe_ them? Or did you _trust_ defaults?  
**Eks2:** My backend pool was internal. No public exposure.  
**ShadowNet:** And yet, every RDP you allow… echoes across misconfigured NSGs.  
**Eks2:** Then teach me.  
**ShadowNet:** I do not teach. I appear… in what you forget to question.  
**Eks2:** I will remember next time.  
**ShadowNet:** Good. Because I never left. I just waited in the quiet.

---

## 🛡️ Eks2's Threat Modelling Notes

| 🔍 Security Element        | 💭 Eks2’s Reflection                                          |
|---------------------------|---------------------------------------------------------------|
| 🔓 What was exposed        | Public-facing HTTP port via **Application Gateway**          |
| ❗ Dangerous assumption     | “Only HTTPS matters for sensitive apps”                      |
| 🛠️ How I’ll improve        | Use **HTTPS with certificates**, enable **WAF**, monitor logs |
| 🕶️ ShadowNet’s silent lesson | “Your cloud listens. So does the enemy.”                    |

---

> 🕶️ **ShadowNet whispers:**  
> “I do not crash your system. I drift through its comfort zones.”

---

### ✒️ Closing Signature
✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
