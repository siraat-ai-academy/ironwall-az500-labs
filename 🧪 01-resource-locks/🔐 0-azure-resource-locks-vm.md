# 🛡️ Create a Virtual Machine & Add Azure Resource Locks

This lab demonstrates how to create an Azure Virtual Machine and protect it from accidental deletion or modification using Azure Resource Locks.  
The steps follow a clean, practical approach suitable for beginners and certification preparation (AZ-500 / Security fundamentals).

---

## 🎯 Lab Objectives

By the end of this lab, you will be able to:

- ✅ Create a Virtual Machine in Azure
- 🔐 Apply a **Delete lock** to a Virtual Machine
- 👁️ Apply a **Read-only lock** to a Resource Group
- 🧹 Safely remove locks and clean up resources

---

## 🧰 Prerequisites

- Azure subscription (Free or Paid)
- Access to the Azure Portal  
  👉 https://portal.azure.com

---

## 🔧 Task 1: Create a Virtual Machine

1. Sign in to the **Azure Portal**
2. Select **Create a resource**
3. Choose **Virtual Machine**

### 📁 Basic Configuration

- **Subscription**: Select your active subscription
- **Resource Group**:  
  - Click **Create new**
  - Name: `NordicVault-Resources`
- **Virtual Machine name**: `NordicVault-VM`
- **Region**: Choose any available region

### ⚙️ Availability & Security

- **Availability options**: No infrastructure redundancy required
- **Security type**: Trusted Launch

### 💿 Image & Size

- **Image**: Ubuntu Server 20.04 LTS (Gen2)
- **Size**: B2s

### 🔑 Administrator Account

- **Authentication type**: Password
- **Username**: `NordicUser`
- **Password**: Create a strong password

### 💾 Disk Settings

- **OS Disk Type**: Standard SSD

4. Select **Review + Create**
5. After validation passes, select **Create**

⏳ Wait for deployment to complete.

---

## 🔐 Task 2: Add a Delete Lock to the Virtual Machine

1. Open the **NordicVault-VM**
2. In the left menu, select **Locks** (under Settings)
3. Select **Add**

### 🔒 Lock Configuration

- **Lock name**: `VMDeleteLock`
- **Lock type**: Delete
- **Notes (optional)**: Prevent accidental deletion

4. Select **OK**

✅ The Virtual Machine is now protected from deletion.

---

## 🛑 Task 3: Add a Read-Only Lock to the Resource Group

1. Open the **NordicVault-Resources** Resource Group
2. Select **Locks** from the left menu
3. Select **Add**

### 👁️ Lock Configuration

- **Lock name**: `RGReadOnly`
- **Lock type**: Read-only
- **Notes (optional)**: Prevent changes to all resources

4. Select **OK**

✅ All resources in the Resource Group are now protected from modification.

---

## 🧪 Validation Test (Optional)

- Attempt to delete the Virtual Machine  
- Azure will block the action due to the lock

---

## 🧹 Clean-Up (Important)

To delete resources successfully:

1. Remove the **VMDeleteLock** from the Virtual Machine
2. Remove the **RGReadOnly** lock from the Resource Group
3. Delete the Virtual Machine
4. Delete the Resource Group

⚠️ Locks must be removed before deletion is allowed.

---

## 🌍 Real-World Importance

- Resource locks prevent accidental damage
- Commonly used in production and enterprise environments
- Essential knowledge for:
  - Cloud administrators
  - Security engineers
  - AZ-500 & security certification candidates

---

## ✍️ Author

**Muhammad Naveed Ishaque**  
Content Creator | AI-Assisted Educator | Concept Simplifier  

**Siraat AI Academy**  
_The Straight Path — Empowering minds with clarity, illuminating paths with purpose._
