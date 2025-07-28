
# 🌐 Lab 19: Deploying a Web App with Azure SQL — A Journey into the Cloud Garden ☁️🌸

---

## ☁️ A Gentle Morning at NordicVault

It was a soft and foggy Monday morning in Copenhagen. The kind of morning where the sky feels like a watercolor painting, and the air hums gently with possibility. 🌦️

**Mr. Eks2**, carrying his well-worn sketchbook of cloud questions, arrived at the lab — cheeks a little red from the bike ride, heart wide open for learning.

At the door stood **Kasper Madsen**, steaming coffee in one hand, CLI commands in the other, and **Sofia Zaymera**, calm and bright like morning sunlight through a library window. 🌞

> **Kasper (grinning):** “Velkommen, Eks2! Today we’re going to build something magical — a real web app! Not just on your machine, but in the sky. A whole *todo-list universe* on Azure!”

> **Sofia (softly):** “And we will guide every step, gently. This will help you learn how apps live, talk to databases, and grow safely in the cloud.”

> **Mr. Eks2 (smiling shyly):** “So… we make an app, give it a home in Azure, and teach it how to speak to its brain — the database?”

> **Sofia:** “Yes. And we teach you how to protect it, monitor it, and someday — scale it.”

---

## 🛠️ Step 1: Download and Run the Sample App

> **Kasper:** “Let’s begin with the basics. We’re downloading a ready-made **ASP.NET App**. Think of it like receiving a cozy wooden cabin you’ll soon lift into the clouds.”

1. Download the **sample project ZIP file**.
2. Extract it into a local folder like `C:\NordicProjects\CloudGarden`.
3. Open the `.sln` file in **Visual Studio**.
4. Press **F5** to build and run locally.
5. In the browser, click **Create New** to add sample todo items. 📝

> **Sofia (tip):** “Make sure Visual Studio can find the necessary packages. If things feel slow, it’s just the app waking up from its digital slumber.”

> **Mr. Eks2 (reflecting):** “The todo app is simple… but it holds logic, interaction, and storage — the full cycle of an idea becoming data.”

---

## 🌐 Step 2: Publish the App to Azure

> **Kasper:** “Now, we gently lift your app into Azure’s arms.”

1. Right-click the project → **Publish**.
2. Select **Azure** > **Azure App Service (Windows)**.
3. Sign in with Azure credentials.
4. Click **+** to create a new **App Service**:
   - Name: `NordicVault-App`
   - Use existing **Resource Group (ressourcegruppe)**: `DKSec-Infra`
   - Create new **Hosting Plan**:  
     - Name: `DKWebPlan`  
     - Region: East US 2  
     - Size: B1
5. Click **Create** and then **Finish**.

> **Sofia:** “Azure App Service is like a green garden where your app can live peacefully, auto-watered and sunlit with compute power.”

> **Mr. Eks2:** “So App Service is like the greenhouse… and we’re planting the todo app inside it?”

---

## 🗄️ Step 3: Create Azure SQL Database

> **Kasper:** “Now your app needs a mind — a place to store memories.”

1. In the Publish dialog → **Service Dependencies**.
2. Next to **SQL Server Database**, click `...` > **Connect**.
3. Select **Azure SQL Database** > **+ Create new**.
4. For **SQL Server**:
   - Name: `nordicvault-dbserver`
   - Admin: `dbadmin`
   - Password: `••••••••`
5. Click **Create**.

> **Sofia:** “Think of this as building a calm, structured library where your app’s thoughts — its to-do items — can be stored and retrieved.”

---

## 🔌 Step 4: Configure Database Connection

1. Click **Next** in the Publish dialog.
2. Enter:
   - **Connection string name**: `MyDbConnection`
   - Use the admin username/password created earlier.
   - Check **Azure App Settings** to securely store credentials.
3. Click **Finish**.

> **Sofia:** “A connection string is like a private key to the library. Guard it gently.”

> **Mr. Eks2 (pensively):** “So... the app now knows where to find its database, like a writer finding their journal.”

---

## 🚀 Step 5: Deploy the App

1. In the **Publish** tab, click **Publish**.
2. The browser will open your app’s live URL.
3. Test by creating new to-do items.

> **Kasper (raising mug):** “Skål! Your app is live! You’ve made something that lives in the cloud. ❤️”

> **Sofia:** “It’s a sacred moment — the digital meets the human.”

---

## 🏡 Step 6: Access the Database Locally

1. Open **SQL Server Object Explorer** in Visual Studio.
2. Click **Add SQL Server**.
3. Expand **Azure**, select your database.
4. Enter credentials > **Connect**.
5. If prompted, allow your client IP in **SQL firewall**.
6. View data in **Todoes** table.

> **Mr. Eks2:** “Like peeking inside the mind of the app… to see what it remembers.”

---

## 🧠 Step 7: Update App with Code First Migrations

> **Elina Petrova (joining quietly):** “Now we’ll evolve the app’s brain. Gently.”

1. In `Models/Todo.cs`, add:
   ```csharp
   public bool Done { get; set; }
   ```
2. In **Package Manager Console**:
   ```
   Enable-Migrations
   Add-Migration AddProperty
   Update-Database
   ```
3. In `TodosController.cs`, update:
   ```csharp
   public ActionResult Create([Bind(Include = "Description,CreatedDate,Done")] Todo todo)
   ```
4. Update `Create.cshtml` and `Index.cshtml` to include **Done** checkbox.

> **Sofia:** “This is evolution — the app grows by reflecting new truths in its structure.”

---

## 🌍 Step 8: Publish Code First Changes to Azure

1. Right-click project > **Publish** > **More Actions** > **Edit**.
2. Under **Database context settings**:
   - Select **Azure connection**
   - Check **Execute Code First Migrations**
3. Save and **Publish** again.
4. Test in browser — Done checkbox should appear.

> **Mr. Eks2 (excited):** “It remembers more now! Our app… it’s learning. 🧠”

---

## 🔍 Step 9: Enable Log Streaming

1. In the Publish window > **Hosting** > `...` > **View Streaming Logs**.
2. Watch live logs in Visual Studio Output.
3. Click **Stop Monitoring** to stop.

> **Kasper:** “Logs are like heartbeat monitors. They show us the soul’s rhythm of the app.”

---

## 🧹 Step 10: Clean Up Resources

> **Isabella Konti:** “Always leave the cloud cleaner than you found it.”

- Delete all resources in Azure to avoid costs.

---

## 🔐 Real-World Reflection: A 158-Year Legacy Lost to One Weak Password

In 2023, a 158-year-old company collapsed because of a single compromised password. [Read the BBC story](https://www.bbc.com/news/articles/cx2gx28815wo).  
This lab teaches you how to set up secure cloud apps with **connection strings**, **firewall rules**, and **Azure App Settings** — the small doors through which big attacks can sneak in if left unlocked.  
By practicing good design and secure deployment, you help protect not just apps — but legacies.

---

✍️ Created & Curated by  
**Muhammad Naveed Ishaque**  
_Content Creator | AI Writer | Narrative Simplifier_  
_With the inner voice of Eks2 — the whisper behind the work._

**Siraat AI Academy**  
_“The Straight Path — Empowering minds with clarity, illuminating paths with purpose.”_
