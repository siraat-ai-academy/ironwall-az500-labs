
# 🌌 Eks2 aur ShadowNet – Ek Cloud Thriller (Roman Hindi Version)

> "Jahaan configuration khatam hoti hai, wahan ShadowNet ki kahani shuru hoti hai..." 🕶️✨

Sab kuch set ho chuka tha.

Eks2 ne virtual network banaya, NAT Gateway configure kiya, load balancer setup kiya. IIS chali, VMs ne “Hello World” kaha...  
Lekin us raat... ek ajeeb sa khamoshi chhayi thi. 💭

Cloud ka dashboard blink kar raha tha, lekin kuch tha jo blink nahi kar raha tha...

## ☁️ Midnight Cloud — Andar ka Darwaza

Data center ke screens ab so rahe the, lekin Eks2 jaag raha tha.  
Uska mouse pointer jaise kisi invisible cheez ki taraf kheech raha tha.  
Ek warning… ya ek whisper?

“Port 80 open hai... testing ke liye...”  
“Bas thoda der ke liye...”  
“Public IP... sirf monitoring ke liye...”

Usi waqt... ek silhoutte andhere se ubhri.  
Wo code nahi tha. Wo bug bhi nahi tha.  
Wo tha — **ShadowNet**. 🕶️

---

## ⚡ Encounter in the Cloud

**Eks2:** “Tum kaun ho?”

**ShadowNet:** “Main wahi hoon jise tumne ignore kiya... default settings mein.”  

**Eks2:** “Maine sab kuch follow kiya... NSG bhi configure ki, load balancer bhi.”

**ShadowNet:** “Magar tumne trust diya... bina verify kiye. Tumne socha yeh test hai — main wahi soch hoon.”  

Us waqt, portal ki screen par ek public IP blink hui.  
Load balancer ke rules theek the, magar **session persistence** ab bhi enable thi.  
“Client IP & Protocol”... wahi route jahan se ShadowNet slip karta hai...

**Eks2:** “Tum attack nahi karte?”  
**ShadowNet:** “Mujhe attack karna nahi padta. Main wahi hoon jahan tum nahi dekhte.” 👁️‍🗨️

---

## 🔥 The Firewall Within

Eks2 ne portal mein jaa kar load balancer rule open kiya.  
Session persistence ko **None** kiya. Save dabaya.  
Cloud ne ek gehri saans li. Jaise kisi ne chhoti si dua maani ho.

**ShadowNet:** “Yeh sirf ek rule tha...”  
**Eks2:** “Lekin ab meri nazar tum par hai.”

Wo silence jo pehle darr lagti thi, ab strategy ban gayi thi.  
Eks2 ne monitoring enable kiya. NSG mein outbound traffic trace karna shuru kiya.  
**Bastion** ke through access — secure, logged, aur protected.  

ShadowNet piche hata… lekin gayab nahi hua.

---

## 💡 Eks2’s Threat Modelling Table

| 🔍 **Security Element**      | 💭 **Eks2’s Reflection**                                 |
|-----------------------------|-----------------------------------------------------------|
| 🔓 Kya exposed tha          | Public NSG rule with open access                         |
| ❗ Kya socha tha             | "Bas test ke liye open kiya hai"                        |
| 🛠️ Ab kya karunga           | Least privilege, service tags, outbound monitoring       |
| 🕶️ ShadowNet ki baat        | “Main wahan nahi aata jahan tum dekhte ho... main wahan hoon jahan tum dekhte hi nahi.” |

---

## 🎬 Ending Quote by ShadowNet

**ShadowNet:**  
“Main hacker nahi hoon.  
Main wo security hygiene hoon jo tum bhool gaye the...  
Wahan intezar karta hoon jahan darwaza aadha khula ho.” 🕶️

---

### ✒️ Created & Curated by  

**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_

🌷✨ Darr se nahi, design se jeeto. Har gap ko band karo, har soch ko secure karo.
