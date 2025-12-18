# 🛡️ Create an Azure Virtual Machine and Protect It with Resource Locks

This lab demonstrates how to create an Azure Virtual Machine and secure it using **Azure Resource Locks** to prevent accidental deletion or modification.  
This is a core skill for Azure security, governance, and AZ-500 exam preparation.

---

## 🎯 Lab Objectives

By the end of this lab, you will be able to:

- Create an Azure Virtual Machine
- Apply a **Delete lock** to a Virtual Machine
- Apply a **Read-only lock** to a Resource Group
- Verify lock behavior
- Safely remove locks and clean up resources

---

## 🧩 Prerequisites

- Active Azure subscription
- Access to the Azure Portal
- Basic familiarity with Azure resources

---

## 🖥️ Task 1: Create a Virtual Machine

1. Sign in to the **Azure Portal**
2. Select **Create a resource**
3. Choose **Virtual Machine**

### 📁 Basics

4. Subscription: Select your subscription  
5. Resource Group:  
   - Click **Create new**
   - Name: `NordicVault-Resources`
6. Virtual machine name: `NordicVault-VM`
7. Region: Choose any preferred region
8. Availability options: **No infrastructure redundancy required**
9. Security type: **Trusted launch**
10. Image: **Ubuntu Server 20.04 LTS (Gen2)**
11. Size: **B2s**

### 🔐 Administrator Account

12. Authentication type: Password
13. Username: `NordicUser`
14. Password: Use a strong password

### 💽 Disks

15. OS disk type: **Standard SSD**

### 🚀 Create

16. Select **Review + Create**
17. Validate settings
18. Click **Create**
19. Wait for deployment to complete

---

## 🔒 Task 2: Add a Delete Lock to the Virtual Machine

1. Open the **NordicVault-VM**
2. In the left menu, select **Locks**
3. Click **Add**
4. Lock name: `VMDeleteLock`
5. Lock type: **Delete**
6. Click **OK**

### ✅ Result

- The Virtual Machine **cannot be deleted**
- All other operations continue to function normally

---

## 🛑 Task 3: Add a Read-Only Lock to the Resource Group

1. Open **NordicVault-Resources**
2. Navigate to **Locks**
3. Click **Add**
4. Lock name: `RGReadOnly`
5. Lock type: **Read-only**
6. Click **OK**

### ✅ Result

- All resources can be viewed
- No modifications are allowed

---

## 🧪 Task 4: Verify Lock Behavior

1. Attempt to delete the Virtual Machine  
   - Operation fails due to **Delete lock**
2. Attempt to modify a resource in the Resource Group  
   - Operation fails due to **Read-only lock**

This confirms that the locks are active and enforced.

---

## 🧹 Task 5: Clean Up Resources

To delete resources safely:

1. Remove **RGReadOnly** lock from the Resource Group
2. Remove **VMDeleteLock** from the Virtual Machine
3. Delete the Virtual Machine
4. Delete the Resource Group

---

## 🌍 Real-World Relevance

- Prevents accidental deletion in production environments
- Enforces governance and change control
- Commonly used in enterprise Azure environments
- Frequently tested in **AZ-500** and security interviews

---

## 🧠 Key Takeaways

- **Delete locks** protect critical resources
- **Read-only locks** protect entire environments
- Locks enforce intention, not restriction
- Security begins with simple safeguards

---

## ✍️ Maintained By

**Muhammad Naveed Ishaque**  
Content Creator | AI Writer | Learning Experience Designer  

Siraat AI Academy  
*Empowering minds with clarity, one lab at a time.*
