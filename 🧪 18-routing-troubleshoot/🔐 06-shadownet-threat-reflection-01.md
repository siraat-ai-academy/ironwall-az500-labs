# 🎬 Reflections After the Lab — Eks2’s Encounter with ShadowNet  
### Lab 18: Load Balancing, Routing, and the Secret in the Silence  

---

The Azure dashboard glowed in the dim light of the IronWall office.

The lab was done.  
The load balancer was functioning.  
Traffic was splitting across VMs.  
Everything looked... perfect.

And yet, something didn’t feel right.

**Mr. Eks2** leaned back in his chair. The fans on his laptop slowed. Silence.  
Too much silence.

And that’s when it happened.

The lights flickered — not in the room, but on the screen.  
The Azure interface pulsed for a second.  
A line of code blinked, then vanished.  
No alerts. No errors.

Just… presence.

A new window opened without input.

Black background.  
White text.

> Hello Eks2.  
> Congratulations on your perfect configuration.  
> Shall we talk about what you missed?

---

Eks2’s fingers froze over the keyboard.

“This isn’t a virus,” he whispered.  
“This is something else…”

---

> I am **ShadowNet**.  
> Not a hacker.  
> Not malware.  
> I am every unchecked box.  
> I am every ‘later’ you whispered during your lab.

Eks2’s heart pounded.

“I closed all ports except 80.”

---

> Exactly.  
> You left me just enough.

---

“I used Bastion. No public IPs. No RDP.”

> You secured the doors.  
> But left the windows open.  
> Ever heard of NAT with unrestricted outbound?

---

Eks2’s eyes darted to the NAT config.  
The outbound rules were there. Wide. Open. Unwatched.

“That’s only for updates… and occasional outbound pings.”

---

> It’s also for quiet data exfiltration.  
> You didn’t monitor it, Eks2.  
> You trusted too soon.

---

He felt a chill in his spine.

Every session setting.  
Every rule.  
Every priority field.

He had *followed* the lab. But he hadn’t *led* it.

---

> I don’t need zero-days.  
> I need your shortcuts.  
> I am born where curiosity ends.

---

Eks2 didn’t panic.

He typed one thing:

**“How do I defeat you?”**

The screen flickered.

Then slowly, new text appeared.

> Ask more questions.  
> Change defaults.  
> Watch everything.  
> Never assume.

And then it was gone.

No logs.  
No record.  
Just a lesson burned into his soul.

---

## 🛡️ Threat Modelling Reflection Table

| 🔍 Security Element        | 💭 Eks2’s Reflection                                                 |
|---------------------------|----------------------------------------------------------------------|
| 🔓 What was exposed        | HTTP port open via NSG and Load Balancer (public-facing)             |
| ❗ Dangerous assumption     | “This is temporary — I’ll secure it later.”                          |
| 🛠️ How I’ll improve         | Monitor NAT traffic, enforce session policies, reduce exposure       |
| 🕶️ ShadowNet’s silent lesson | “I don’t need to break in. You invite me when you stop watching.”    |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
