# Title: "Dil Se Gateway, Serveron Tak Raasta"
### Subtitle: “Jahan Gateway Bana, Aur Dilon Mein Rasta Khul Gaya”  
---

**East US** ki sard hawaon mein ek nayi kahani likhi ja rahi thi. Ek kahani jahan jazbaat milte the networking se, aur har routing rule chhupaye baitha tha ek dil ka raaz...

**👨‍💼 Mr. Eks2**, lambe coat mein Azure portal ki taraf dekh rahe the. Aankhon mein ek aag thi, lekin chehre par sukoon. Peeche se **🇩🇰 Kasper Madsen** aaya, haath mein ek blueprint le kar.

“**Eks2**, virtual network ka jaadu tayar hai... sirf subneton ka rang bharna baaki hai,” Kasper ne hansi ke saath kaha.

Eks2 ne pyaar se kaha, “Pehla subnet ‘**myBackendPool**’ hoga... jahan humare dil ke servers base banayenge. Doosra, ‘**myApplicationGatewaySubnet**’ — jahan se har connection dilon tak pahuchega.”

🌷✨

Kahin door, **🇪🇸 Sofia Zaymera** ne VM1 aur VM2 ke liye dua ki. “Yeh servers sirf compute resources nahi, yeh hamari kahani ke do raahi hain — ek *images* ka safar, ek *videos* ka jadoo.”

Aur tab — **Ayla**, jo silent warrior thi IronWall team ki, silently configure kar rahi thi IIS. Har server par ek file banayi gayi. VM1 ke andar goonj uthi:

“`<h1>This is the Images Server</h1>`”

Aur VM2 ke andar ek jazba tha:

“`<h1>This is the Videos Server</h1>`”

🌼💻

Raat ke andhere mein **Eks2** ne Application Gateway banaya. “Iska naam hoga **AppGateway**,” unhone kaha, “kyunki is gateway se sirf traffic nahi, mohabbat bhi chalegi.”

**Kasper** bola, “Do pool honge — *imagepool* aur *videopool*. Routing rule bhi path-based hoga. Agar koi **/images/** bole, toh imagepool se jawab milega. Aur agar **/videos/** kahe... toh videopool se.”

Sofia muskurayi, “Waise hi jaise zindagi mein hum sabko apna path chahiye... lekin har raasta kisi na kisi backend se juda hota hai.”

🧚‍♀️

Gateway ke IP par jab pehli baar browser khula...

`http://AppGatewayIP/images/Default.html`  
...ek haseen message aaya: *“This is the Images Server”*

`http://AppGatewayIP/videos/Default.html`  
...aur doosre browser mein utra: *“This is the Videos Server”*

Aur tab **Mr. Eks2** ne aasmaan ki taraf dekha.

“Gateway toh bana liya, doston... lekin asli kaam toh tab hota hai jab hum apni routing life mein bhi samajh jaayein. Kab kis path par jaana hai, aur kis backend se feedback lena hai — yahi toh zindagi ka load balancer hai.”

🌸💖🌿

---

Eks2 ne sirf lab complete nahi kiya —  
usne zindagi ki ek nayi soch likhi.  
Aur bhai, us soch ko aap ne likhne ka rang diya.  

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
