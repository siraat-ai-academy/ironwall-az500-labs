[Pause 1s]
It was a fresh morning in Copenhagen. ☁️

[Pause 1s]
The sun peeked through the clouds as Mr. eks2 stepped into the office — excited, notebook in hand, and a warm coffee in the other.

[Pause 0.5s]
“Godmorgen, eks2!” said Eye Kay with a grin. “Ready to build some bridges in the cloud?”

[Pause 0.5s]
Inky Rihan, already setting up her dashboard, smiled. “We’re learning about Virtual Network Peering — it's how we let different networks talk to each other, securely and privately.”

[Pause 0.5s]
“This is like setting up roads between small towns,” Eye Kay added. “Each Virtual Network is a town, and peering is the friendly road that connects them!”

[Pause 0.5s]
Mr. eks2 chuckled. “Let’s begin this magical road trip in the cloud.”

[Pause 1s]
💠 Step 1: Create the First Virtual Network
- Go to "Create a Resource"
- Search "Virtual Network"
- Name: NordNet-1
- Region: West Europe
- IP Range: 10.1.0.0/16
- Subnet: Subnet-A, Range: 10.1.0.0/24

[Pause 1s]
💠 Step 2: Create the Second Virtual Network
- Same steps as before
- Name: NordNet-2
- IP Range: 10.2.0.0/16
- Subnet: Subnet-B, Range: 10.2.0.0/24

[Pause 0.5s]
Mr. eks2: “These towns are far apart now. When do we build the road?”

[Pause 0.5s]
Eye Kay: “Ah, good question! That’s our next step.” 🚗

[Pause 1s]
💠 Step 3: Peer the Two Virtual Networks
- Go to NordNet-1 > Settings > Peerings
- Click Add
- From NordNet-1 to NordNet-2: Net1-Net2
- From NordNet-2 to NordNet-1: Net2-Net1
- Make peering bidirectional

[Pause 0.5s]
Mr. eks2: “So it’s like a handshake between mayors?”

[Pause 0.5s]
Eye Kay: “Exactly! Or a warm ‘hej hej’ 🤝”

[Pause 1s]
💠 Step 4: Create the First Virtual Machine
- Name: NordicVault-VM1
- Region: West Europe
- Use Subnet-A in NordNet-1
- Windows Server 2019, Standard_B2s
- Allow RDP (3389), Standard SSD

[Pause 1s]
💠 Step 5: Create the Second Virtual Machine
- Name: NordicVault-VM2
- Region: West Europe
- Use Subnet-B in NordNet-2
- No public ports for extra security

[Pause 0.5s]
Mr. eks2: “So only insiders can visit this library?”

[Pause 0.5s]
Inky: “Exactly. Good cybersecurity is like a quiet town — only welcome guests get in.”

[Pause 1s]
💠 Step 6: Enable Communication Between VMs
- Connect to VM1 via RDP
- Open PowerShell
- Run: New-NetFirewallRule –DisplayName "Allow ICMPv4-In" –Protocol ICMPv4
- Connect to VM2’s private IP (e.g., mstsc /v:10.2.0.4)

[Pause 0.5s]
Sofia: “This lets VM1 ping or reach VM2 — like driving over that private road.”

[Pause 0.5s]
Mr. eks2: “So, if VM1 can reach VM2, the peering is successful?”

[Pause 0.5s]
Eye Kay: “Yes! Cloud networking magic confirmed.” ✨

[Pause 1s]
💠 Clean-Up Time
- Delete Virtual Networks, VMs, and Resource Groups
- Keep your environment clean and budget safe 💸

[Pause 1s]
🌍 Real-World Reflection:
In real jobs, teams work across networks. Virtual Network Peering lets them collaborate securely. You now hold the key to private communication between Azure resources.

[Pause 1s]
🔐 Real-World Reminder:
A 158-year-old company was destroyed due to one weak password.
This lab shows how private networking and secure access can prevent such disasters.

[Pause 1s]
Link: https://www.bbc.com/news/articles/cx2gx28815wo
