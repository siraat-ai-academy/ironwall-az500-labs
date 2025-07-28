# 🧠 Threat Modelling Dialogue — Mr. Eks2 Meets ShadowNet
✨ *Human-centered security reflection through story, emotion, and insight*
___

## 📘 Section Title:  
**“Reflections After the Lab — Eks2’s Dialogue with ShadowNet”**

---

## 🔍 Introduction  
At the end of **Lab 17: Creating an Application Gateway**, all steps were completed successfully.  
The **Virtual Network** was crafted with care. Two **VMs** stood ready — one serving **images**, the other **videos**.  
The **Application Gateway** routed traffic, as expected.  

And yet…

As the final browser test confirmed success, the screen did not feel "done."  
There was a lingering whisper — not in logs, but in the corners between security layers.

A familiar presence.  
Not hostile. Just patient.  
Not malware. Not a breach.  
But the gap between **what was built**… and **what was assumed**.

🕶️ **ShadowNet** had arrived.

---

## 🎭 Dialogue: Mr. Eks2 vs. ShadowNet

**Eks2:** The App Gateway works. Why are you here?  
**ShadowNet:** You gave it life — and forgot its leash.  
**Eks2:** But I restricted traffic to port 80 only.  
**ShadowNet:** And left it wide open to the world. No NSG, no inspection. Just trust.  
**Eks2:** It's just for testing. A quick deployment.  
**ShadowNet:** I live in "just for testing."  
**Eks2:** I configured path-based routing. Clean and smart.  
**ShadowNet:** Smart paths... with no guards. Do you read the logs they write?  
**Eks2:** I’ll set up monitoring tomorrow.  
**ShadowNet:** Then tonight... I learn your map.  
**Eks2:** You won't stay long.  
**ShadowNet:** No. I only linger where you forget to lock.  
**Eks2:** I’ll deploy **WAF**, update **NSGs**, and review every default.  
**ShadowNet:** That’s how defenders are born.  

---

## 🛡️ Threat Modelling Reflection Table

| 🔍 Security Element       | 💭 Eks2’s Reflection |
|---------------------------|----------------------|
| 🔓 **What was exposed**    | Public-facing **VMs** via open HTTP & RDP |
| ❗ **Dangerous assumption**| “It’s just a test — nothing critical.” |
| 🛠️ **How I’ll improve**    | Apply **NSG restrictions**, implement **WAF**, audit **default configurations** |
| 🕶️ **ShadowNet’s silent lesson** | “You test in daylight. I enter at dusk — where audit trails end.” |

---

## 🧠 Bonus Whisper from ShadowNet

> “I am not your enemy. I am the quiet result of skipped steps.  
> I am born not from breach — but from **blind trust**.”

---

### ✒️ Closing Signature

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._  

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
___
