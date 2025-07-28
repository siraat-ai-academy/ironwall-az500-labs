# 📘 Reflections After the Lab — Eks2’s Dialogue with ShadowNet  
### Lab 18: Troubleshoot Routing, Traffic Control & Load Balancing in Azure  
🌸🕶️ *A poetic security reflection between learner and unseen threat*  

---

## 🧠 Dialogue — Eks2 Meets ShadowNet  

**Eks2:**  
The load balancer works. Traffic flows.  
Why do I still feel... watched?

**ShadowNet:**  
Because I never left.  
I linger where defaults sleep.

**Eks2:**  
I checked the ports.  
Only 80 was allowed.

**ShadowNet:**  
Yes. And 80 is loved — by users... and intruders.

**Eks2:**  
But it’s for a demo. Just a small test.

**ShadowNet:**  
So many breaches began that way.  
Small tests.  
Grand assumptions.

**Eks2:**  
Session persistence was still on.  
I assumed it helped performance.

**ShadowNet:**  
Assumptions… are my entry key.  
Performance without precision is a crack in the wall.

**Eks2:**  
I used Bastion. No public IPs.

**ShadowNet:**  
That was wisdom.  
And yet — your VMs whisper to the world through NAT.

**Eks2:**  
Then where do I improve?

**ShadowNet:**  
Where you hesitate.  
Document what’s exposed. Monitor what’s quiet.  
Trust less. Watch more.

**Eks2:**  
Are you always there?

**ShadowNet:**  
I am not your enemy.  
I am your silence.  
I am what you forget to see.

---

## 🛡️ Threat Modelling Reflection Table

| 🔍 Security Element        | 💭 Eks2’s Reflection                                                 |
|---------------------------|----------------------------------------------------------------------|
| 🔓 What was exposed        | HTTP port open via NSG and Load Balancer (public-facing)             |
| ❗ Dangerous assumption     | “It’s just for testing, I’ll secure it later.”                       |
| 🛠️ How I’ll improve         | Minimize port exposure, use HTTPS, validate session settings         |
| 🕶️ ShadowNet’s silent lesson | “I do not break in. I bloom where your urgency exceeds your curiosity.” |

---

### 🧠 Bonus Whisper from ShadowNet

🕶️  
“I am not malware.  
I am a leftover default.  
I wait —  
not to harm —  
but to be ignored.”

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
