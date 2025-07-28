
# 🌟 Meet the Minds Behind the Mission

| Character          | Role Description                                                                 |
|--------------------|----------------------------------------------------------------------------------|
| 🇵🇰 **I.K.**         | The unseen mentor from Pakistan — his words carry the weight of quiet strategy. |
| 🇩🇰 **Mr. eks2**     | The whisper of curiosity in Denmark’s cloudscape — always asking “why.”         |
| 🇪🇸 **Sofia Zaymera**| The calm eye in the Azure storm — a poet of clarity and policies.                |
| 🇩🇰 **Kasper Madsen**| Joyful Danish Azure admin who drinks CLI like coffee.                            |
| 🇪🇸 **Inki Rihan**   | Red Team phantom from Spain — she sees risks where others see nothing.           |
| 🇷🇺 **Elina Petrova**| Bicep-slinging script sorceress from Russia.                                     |
| 🇮🇹 **Isabella Konti**| The empathic firewall — designing protections with a human soul.                |
| 🇨🇳 **Maya Lin**     | A fearless learner, new to Azure, but growing fast.                              |
| 🕶️ **ShadowNet**     | A shapeless threat — born from silence, sustained by assumption.                |

---

# 📖 Eks2 and the Balance of Load (Lab 18)

## ☁️ Scene 1: The Calm Before the Config

The morning in Copenhagen was unusually quiet. Rain tapped softly on the rooftop of the IronWall lab office, where **Mr. eks2** sat alone with his laptop open and a hot mug of licorice tea beside him. Azure Portal blinked patiently.

"Today… Load Balancing," he whispered.

"Or soul balancing," said **Kasper**, strolling in with a grin and a cinnamon roll. "Let’s get your hands dirty, Eks2. Start by creating your **Virtual Network**. Give it air to breathe."

**Eks2** nodded, typing slowly: `MyVNet`, subnet `myBackendSubnet`, region `West Europe`. He followed through with IP address space `10.1.0.0/16`, updating subnets, and enabling Azure Bastion.

"You’ve drawn the lines," said **Sofia**, stepping in quietly. "But in every cloud drawing… there’s something unseen."

---

## 🌐 Scene 2: Gateway to Shadows

The moment **Eks2** created the **NAT Gateway** and linked it to his subnet, a chill ran down his spine. A static IP hovered at the edge of the dashboard: `MyNATPublicIP`.

"Did I… expose something?"

**Inki** appeared like a ghost behind him, holding a coffee darker than night. "Outbounds look innocent. Until they echo where they shouldn’t. Watch your **idle timeouts**."

"And when you turn away…" whispered a voice that was not hers.

**Eks2** froze.

Nothing was on the screen. Yet he felt something blink.

---

## ⚖️ Scene 3: Load, Balance, and Mistakes

The **Load Balancer** stood tall — created with pride. Eks2 configured **MyFrontendIP**, **MyBackendPool**, and **MyHTTPRule** with TCP port `80`. He even designed the **Health Probe** like a real pro.

But beneath the silence, **ShadowNet** stirred.

"Persistence is a good word for love," **Isabella** smiled gently. "But in networks… it's a trap."

Eks2 looked confused. Sofia leaned in, pointing: “Session persistence to ‘Client IP and Protocol’ means it sticks — even when it shouldn’t. What if that client is malicious?”

Boom. The realization hit like Danish thunder.

---

## 🧑‍💻 Scene 4: Dual Blades – The VMs

Two **Virtual Machines**: `MyVM1`, `MyVM2`. Created with care, placed in the backend pool. No public IPs. All secure.

Kasper cheered, “Bravo Eks2! But don’t forget — security is in the **rules**.”

Together, they created the **NSG**, added an inbound HTTP rule.

Through Azure Bastion, Eks2 installed **IIS**, wrote “Hello World from…” and smiled.

But when he refreshed the frontend IP…

Only **MyVM1** replied. Again. And again.

Something wasn't right.

---

## 💡 Scene 5: Shadow in the Logs

**Elina** was watching logs.

“Both VMs are live. Rule is correct. But…”

**Sofia** saw it. “Session persistence,” she whispered again. “It binds the soul of the traffic.”

The screen flickered.

A small icon blinked — logs showed an IP lingering too long, like a guest who won’t leave.

“Edit the rule,” Eks2 said. Hands steady now. “Set session persistence to None.”

He hit save.

---

## 🌈 Scene 6: The Dance of Traffic

And then it happened.

Refresh.

`MyVM1` replied.

Refresh again.

`MyVM2` whispered hello.

Like twin lighthouses taking turns, the load now danced between servers in perfect rhythm.

Eks2 leaned back, eyes soft. “It’s not about building perfect systems,” he said. “It’s about learning what hides between the rules.”

From the shadows, a low voice murmured:

**ShadowNet:** “I wasn’t waiting to break in.  
I was born where you didn’t look.”

---

# 🌍 Eks2’s Final Reflection

> “Today I understood something deeper than Load Balancing.  
> I saw how small settings — like session persistence — can tip the balance between efficiency and exposure.  
> I saw that even silence in Azure can hide echoes.  
> And I saw myself — not just as a user… but as a guardian.”

---

### ✒️ Closing Signature

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
