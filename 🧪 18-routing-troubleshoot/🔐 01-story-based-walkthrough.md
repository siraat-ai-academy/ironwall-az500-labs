# 🛰️ Troubleshoot & Triumph: Azure Load Balancer Tale  
### Subtitle: “Where Traffic Found Its Way, and VMs Found Their Voices”  

---

### 🌟 Meet the Minds Behind the Mission:

🛸 **Mr. Eks2** — the curious whisper of Muhammad Naveed Ishaque, now a beginner Azure Security trainee at a Danish firm, always asking, “Can this be simpler?”  
🇩🇰 **Kasper Madsen** — a timeless cyber-sufi — a guardian of digital wisdom across centuries.  
🇪🇸 **Sofia Zaymera** — a soft-spoken security expert from Spain who explains complexity with clarity  
✍️ **Muhammad Naveed Ishaque** — a content creator whose words help beginners feel brave and seen  
🔎 See full character bios in the README file.

---

## 🔮 Scenario Setup

It was a rainy Thursday morning in West Europe. **Mr. Eks2** arrived, holding his warm tea with both hands. “Today we help traffic find its way,” said **Kasper**, entering in his forest-green cloak. **Sofia** smiled and waved from her workstation. “We’re going to troubleshoot Azure Load Balancer,” she said kindly, “and make sure everything flows correctly.”

**Mr. Eks2** blinked. “Traffic? Like… cars?”  
Everyone laughed gently. Kasper nodded, “Almost, Eks2. But this traffic flows through light and cables — and sometimes, it gets lost. Today, we become its guide.”

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🧱 Task 1: Create a Virtual Network

**Kasper:** “We start by building the city — a **Virtual Network**. We call it **NordicBridgeNet**, a quiet digital village.”  
**Sofia:** “And we make space for two main roads — **myBackendSubnet** and **AzureBastionSubnet** — to help our machines talk securely.”  
**Mr. Eks2:** “So… it’s like building neighborhoods before inviting guests?”  
**Kasper:** “Yes! And every address must be known, every door counted.”

---

### 🌐 Task 2: Create a NAT Gateway

**Kasper:** “Now we create a **NAT Gateway** — like a shared exit for all the people in one building.”  
**Sofia:** “We name it **NorthLightNAT** and connect it to the backend subnet. This helps the VMs go outside safely, but no one can enter unless allowed.”  
**Mr. Eks2:** “Like a one-way mirror?”  
**Sofia:** “Exactly.”

---

### ⚖️ Task 3: Create a Load Balancer

**Kasper:** “Ah, now we craft balance — the **Load Balancer**, our digital traffic officer.”  
**Sofia:** “We create **SilkBalancer**, with two lanes: one for entering (frontend IP) and one for assigning the requests (backend pool).”  
**Mr. Eks2:** “And the rule? What does it do?”  
**Kasper:** “It decides how each whisper of the internet is heard… and by whom.”

---

### 🧍 Task 4: Create Virtual Machines

**Kasper:** “Now we invite the workers — two **Virtual Machines**, named **NordicVault-VM1** and **NordicVault-VM2**.”  
**Sofia:** “No public IPs — we connect using **Azure Bastion**, our secure bridge.”  
**Mr. Eks2:** “Do they get uniforms?”  
**Sofia:** “Yes — a **Network Security Group** called **SafeDoorsNSG**, with a rule to allow only **HTTP (port 80)**.”

---

### 💻 Task 5: Install IIS on Both VMs

**Kasper:** “Time to give them voices. We install **IIS** so they can say: ‘Hello World’.”  
**Sofia:** “Each says it slightly differently — because each VM is unique.”  
**Mr. Eks2:** “So when someone knocks on the Load Balancer, one VM says Hello?”  
**Sofia:** “Yes. And soon, they will take turns.”

---

### 🔄 Task 6: Test Load Balancer

**Mr. Eks2** opened his browser. “Hmm, it’s always **NordicVault-VM1** replying…”  
**Kasper:** “Because the session remembers you — it’s set to **Client IP and protocol**.”  
**Mr. Eks2:** “That feels a little clingy.”  
**Everyone laughs.**

---

### 🧪 Task 7–8: Troubleshoot and Fix Load Balancer Rule

**Sofia:** “We change **Session Persistence** to **None**. That way, the traffic is balanced freely.”  
**Mr. Eks2:** “So now, every refresh might bring a new voice?”  
**Kasper:** “Yes. Like walking through a hallway of kind greetings.”

---

### 🧪 Task 9: Retest Load Balancer

**Eks2** refreshed. One time **VM1**, next time **VM2**.  
He smiled, wide-eyed. “They’re alive. And they’re taking turns. Like two hearts sharing one beat.”

---

## 🌍 Real-World Reflection

This lab teaches how to create safe, balanced, and scalable web applications. Load Balancers keep systems healthy and responsive. NAT helps protect internal resources. NSGs ensure that only what should be open is open. These lessons help beginners become the guardians of uptime and digital trust — even with simple steps.

---

### 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In a heartbreaking real-world incident, a 158-year-old company collapsed after a single stolen password gave attackers access. This lab — with its focus on secure access, correct traffic control, and precise rules — reminds us that even the smallest configuration matters. We don't just set ports and IPs; we protect history.  
Read more: [BBC Report](https://www.bbc.com/news/articles/cx2gx28815wo)

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
