
# 🚀 Lab 14: Create and Manage a Virtual Machine Scale Set Using Azure CLI

## 🔮 Scenario Setup

It was a bright morning in Denmark. 🌤️ **Mr. eks2** had just arrived at the cozy Azure lab room, holding a warm cup of coffee and a head full of questions.

“Godmorgen!” said **Kasper Madsen**, waving cheerfully. “Today, we’re diving into **Virtual Machine Scale Sets** — but don’t worry, we’ll make it feel like a story.”

“Hola, everyone,” added **Sofia Zaymera**, gently adjusting her glasses. “By the end of this lab, you’ll know how to create, manage, and control lots of VMs… like a conductor guiding an orchestra.” 🎻

> 💡 This lab teaches you how to create and manage **VM Scale Sets (VMSS)** using the **Azure CLI**. It’s a key skill for running secure, scalable apps — especially when you need many virtual machines working together!

---

## 🛠️ Step-by-Step with Story & Dialogues

### 🌀 Task 1: Launch the Azure Cloud Shell

👨‍💼 **Mr. eks2:** “Where do we begin, Kasper?”

🇩🇰 **Kasper:** “We click the little terminal icon on the Azure Portal — that’s the **Cloud Shell**. It’s like your magic wand for Azure.” 🪄

🇪🇸 **Sofia:** “Select **Bash** as your shell. And when it asks about storage, just say ‘No storage account required’. Then select your **subscription** and hit ‘Apply’.”

👨‍💼 **Mr. eks2:** “So the **Cloud Shell** is like my Azure toolbox?”

🇪🇸 **Sofia:** “Exactly, amigo. And it speaks Bash fluently.” 😄

---

### 🏗️ Task 2: Create a Virtual Machine Scale Set

🇩🇰 **Kasper:** “Now, let’s build a **Virtual Machine Scale Set**. We’ll name ours `NordicOps-ScaleSet`. Think of it as a group of identical VMs ready to work together.”

```bash
az vmss create \
  --resource-group NordicSecure-RG \
  --name NordicOps-ScaleSet \
  --orchestration-mode flexible \
  --image Ubuntu2204 \
  --vm-sku Standard_B2s \
  --admin-username azurebruger \
  --generate-ssh-keys \
  --storage-sku Standard_LRS
```

🇪🇸 **Sofia:** “Remember, we’re using the **flexible orchestration mode** — this gives you more control over each VM.”

👨‍💼 **Mr. eks2:** “So each **VM** inside the scale set can be treated like its own tiny machine?”

🇩🇰 **Kasper:** “Yes! And to see them, run this:”

```bash
az vm list --resource-group NordicSecure-RG --output table
```

---

### 📈 Task 3: Change the Capacity of the Scale Set

🇩🇰 **Kasper:** “Need more hands on deck? Let’s scale up to 3 VMs!”

```bash
az vmss scale --resource-group NordicSecure-RG --name NordicOps-ScaleSet --new-capacity 3
```

🇪🇸 **Sofia:** “You can confirm with the same list command. It’s like checking your team roster.”

👨‍💼 **Mr. eks2:** “It feels like I’m building a virtual factory… with three happy workers.” 😄

---

### 🛑 Task 4: Stop and Deallocate VM Instances

🇩🇰 **Kasper:** “Time for a break? Let’s stop the VMs.”

```bash
az vmss stop --resource-group NordicSecure-RG --name NordicOps-ScaleSet
```

🇪🇸 **Sofia:** “To stop or deallocate just one VM, you can use these:”

```bash
az vm stop --resource-group NordicSecure-RG --name NordicVault-VM1
az vm deallocate --resource-group NordicSecure-RG --name NordicVault-VM1
```

👨‍💼 **Mr. eks2:** “So I can pause the whole team… or just one person. That’s very kind.” 😊

---

### 🔁 Task 5: Start and Restart VM Instances

🇩🇰 **Kasper:** “Ready to get back to work? Let’s start the machines again.”

```bash
az vm start --resource-group NordicSecure-RG --name NordicVault-VM1
az vmss start --resource-group NordicSecure-RG --name NordicOps-ScaleSet
```

🇪🇸 **Sofia:** “And if a machine needs a little shake-up, restart it!”

```bash
az vm restart --resource-group NordicSecure-RG --name NordicVault-VM1
az vmss restart --resource-group NordicSecure-RG --name NordicOps-ScaleSet
```

👨‍💼 **Mr. eks2:** “It feels like I’m managing a digital city!” 🏙️

---

### 🧹 Final Step: Clean Up

🇪🇸 **Sofia:** “To avoid extra charges, don’t forget to delete everything when done.”

```bash
az group delete --name NordicSecure-RG
```

👨‍💼 **Mr. eks2:** “Tidy cloud, tidy mind.” 🧘‍♂️

---

## 🌍 Real-World Reflection

In the real world, many companies need multiple servers to handle customers, apps, or security tools. This lab shows how **Virtual Machine Scale Sets** let you manage those servers **together**, saving time and avoiding chaos. It’s like hiring and managing staff — but digitally. Perfect for future security engineers, DevOps heroes, or IT teams.

---

## 📘 Bonus: Learn 10 Danish Tech Words

| English Term          | Danish Word           |
|-----------------------|------------------------|
| Resource Group        | Ressourcegruppe        |
| Virtual Machine       | Virtuel Maskine        |
| Scale Set             | Skaleringssæt          |
| Subscription          | Abonnement             |
| Cloud Shell           | Skykonsol              |
| Bash Shell            | Bash-skallen           |
| Storage Account       | Lagerkonto             |
| Admin Username        | Administratorbrugernavn|
| Deallocate            | Frigør                 |
| Restart               | Genstart               |

---

## 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

When the British firm **Kroll** investigated the attack that destroyed a **158-year-old company**, they found the root cause was heartbreakingly simple — **one weak password**.

This lab — where we manage **access**, **capacity**, and **VM orchestration** — teaches us that every small setting, every secure login, every cleanup… matters. These are not just commands. They are shields. They are the invisible guardians of data, identity, and history.

📰 Read the full BBC story: [BBC Article](https://www.bbc.com/news/business-66301653)

---

🧾 Guided by:
**🛸 Mr. eks2** — the curious whisper of Muhammad Naveed Ishaque, always asking, “Can this be simpler?”  
**🇩🇰 Kasper Madsen** — your cheerful Danish cloud guide  
**🇪🇸 Sofia Zaymera** — your soft-spoken Spanish security sensei  

✍️ Created by **Muhammad Naveed Ishaque** for **Siraat AI Academy**  
_"Empowering minds with clarity, illuminating paths with purpose."_ 🌟
