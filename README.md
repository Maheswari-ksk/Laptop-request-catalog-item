# 💻 Laptop Request Catalog Item

## 📂 Category
**ServiceNow System Administrator**

---

## 🧠 Skills Required
- ServiceNow Administration  
- UI Policy  
- UI Actions  
- Update Sets  
- Flow Designer / Workflow  
- UIPath RPA (Optional integration)  
- Tanzu Application Service (Optional deployment)

---

## 📝 Project Description
The **Laptop Request Catalog Item** project aims to simplify and automate the process of requesting laptops within an organization.  
Currently, the process is often manual, leading to delays, lack of standardization, and poor data tracking.  
This project addresses these challenges by creating a **Service Catalog item** that allows employees to easily request a laptop through a guided, dynamic, and automated workflow.

---

## 🧩 Problem Statement
Employees in the organization need a quick and efficient way to request laptops for work.  
The current process is manual and prone to delays, with no dynamic form behavior to guide users or ensure accurate data collection.  

To address this, a **Service Catalog item** needs to be created, allowing users to:
- Easily request a laptop  
- Use dynamic fields and clear instructions  
- Reset the form if needed  
- Ensure all changes are tracked for governance and deployment  

---

## ⚙️ Project Workflow

### **1️⃣ Update Set**
- Create a new Update Set to capture all configuration changes.  
  Path: `System Update Sets → Local Update Sets → New`

### **2️⃣ Service Catalog Item**
- Navigate to: `Service Catalog → Catalog Definitions → Maintain Items`
- Create a new catalog item:
  - **Name:** Request a Laptop  
  - **Category:** Hardware  
  - **Short Description:** Request a laptop for official use  
  - **Description:** Allows users to request laptops with customizable options  
- Add **variables** such as:
  - Laptop Model (Dell, HP, MacBook, etc.)
  - RAM Size (8GB, 16GB, 32GB)
  - Storage (256GB, 512GB, 1TB)
  - Accessories (Mouse, Bag, Headset)
  - Justification (Text Area)

---

### **3️⃣ UI Policy**
- Create UI Policies to control field visibility or mandatory conditions.
  Example:
  - Show “Accessories” field only if a laptop model is selected.
  - Make “Justification” field mandatory.

---

### **4️⃣ UI Action**
- Add a **UI Action** (like a Reset or Clear Form button).
  Example:
  - Action Name: `Reset Form`
  - Script clears all field values when clicked.

---

### **5️⃣ Export Update Set**
- Once configuration is complete:
  - Navigate to your update set → **Export to XML**
  - Save this file for deployment or sharing with another instance.

---

### **6️⃣ Login to Another Instance**
- Import the XML update set file into a different instance:
  - `System Update Sets → Retrieved Update Sets → Import XML`
  - Preview and Commit the update set.

---

### **7️⃣ Testing**
- Navigate to **Service Catalog → Hardware → Request a Laptop**
- Fill in form details and submit a request.
- Verify:
  - Approval flow triggers correctly.
  - Catalog tasks are created for IT fulfillment.
  - UI policies and UI actions work as expected.

---

## ✅ Conclusion
The **Laptop Request Catalog Item** enhances IT service delivery by automating laptop requests, ensuring accurate data entry, and improving efficiency.  
It demonstrates effective use of **ServiceNow catalog design**, **UI policies**, and **update set management**.  
This solution can be extended further with integration to **UIPath RPA** or **Tanzu** for automated provisioning and governance.

---


