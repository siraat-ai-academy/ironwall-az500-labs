# 🗺️ AZ-500 Diagram + Friendly Breakdown  
_Lab 3: Region Restriction with Azure Policy_

---

## 🖼️ Text-Based Azure Diagram

```
+------------------------------+
|      Resource Group          |
|     DKCloudSecure-RG         |
+--------------+---------------+
               |
               v
+------------------------------+
|       Azure Policy           |
|  'Allowed locations' policy  |
|    Location: UK South only   |
+--------------+---------------+
               |
               v
+------------------------------+
|      Policy Assignment       |
|  Applies to: DKCloudSecure-RG|
+--------------+---------------+
               |
               v
+------------------------------+
|      Virtual Network         |
|     NordicNet-VNet (Test)    |
+--------------+---------------+
               |
         Region: ❌ East US (Fails)
               |
         Region: ✅ UK South (Passes)
```

---

## 🎭 Diagram Walkthrough — A Friendly Chat

### 🧑‍🏫 Kasper’s Kickoff

"Okay eks2, let’s imagine you’re the mayor of a digital city — **DKCloudSecure-RG**. You don’t want buildings (cloud stuff) popping up in the wrong parts of town, right?"

“So we make a **Policy** that says: ‘Only build in **UK South**, please!’”

---

### 🛡️ Sofia’s Security Tip

“That’s what the **Allowed Locations Policy** does — it protects your cloud by limiting where people can deploy resources. Very helpful for staying in line with legal or company rules.”

---

### 🤔 eks2’s Wondering

“So it’s like zoning laws… but for the cloud! And the **Policy Assignment** tells Azure exactly where that rule applies?”

---

### 🌐 Kasper Continues

“Exactly! We applied the **Policy Assignment** to the **Resource Group** — so anything built inside that group must follow the rule.”

“Then we tested it by trying to create a **Virtual Network** in the wrong place — **East US** — and Azure politely said ‘nope!’”

---

### 🔁 Sofia Smiles

“When we changed the **region** to **UK South**, the validation passed and the network was allowed. That’s policy in action — not just theory.”

---

### 🧠 eks2’s Realization

“It’s like a friendly border guard saying, ‘Sorry, not here. Please use the UK gate.’ Very polite, very precise.”

---

## 🌍 Final Takeaway

This diagram shows how **Azure Policy** helps enforce rules across the cloud. By applying location restrictions to **Resource Groups**, we control where resources can be deployed — making the environment safer, more compliant, and more predictable. It’s cloud governance… with a smile.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term           | Danish Word            |
|------------------------|------------------------|
| Policy                 | Politikker             |
| Resource Group         | Ressourcegruppe        |
| Virtual Network        | Virtuelt netværk       |
| Region                 | Region                 |
| Location               | Placering              |
| Assignment             | Tildeling              |
| Validation             | Validering             |
| Test                   | Test                   |
| Allowed                | Tilladt                |
| Create                 | Opret                  |

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
Content Creator | AI Writer | Narrative Simplifier  
_With the inner voice of eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
