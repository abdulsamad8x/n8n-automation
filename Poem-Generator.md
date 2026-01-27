# 🎯 n8n Form Automation with AI Poem Generator
### 🎥 Demo Video

You can watch the demo video at the following link:

[ https://drive.google.com/file/d/1qi2d0l9d0E_vpuq22-WIxRgZfwqRYhGk/view?usp=sharing ](https://drive.google.com/file/d/1qi2d0l9d0E_vpuq22-WIxRgZfwqRYhGk/view?usp=sharing)

## 📌 Project Overview

This project is an **n8n automation workflow** that processes form submissions, categorizes users based on their profession, assigns ratings, generates a personalized AI poem, and stores all data in Airtable.

The workflow is triggered when a user submits a form containing:
- Name
- Looks (text input)
- Profession (dropdown: AI Master, Video Editor, Graphic Designer)

The system then:
1. Saves the raw form data.
2. Filters and categorizes users based on profession.
3. Assigns star ratings.
4. Generates a personalized poem using Google Gemini AI.
5. Saves the final structured data into Airtable.

---

## 🧩 Workflow Logic

### 1️⃣ Trigger: Form Submission
The workflow starts when a form is submitted with:
- `name`
- `looks`
- `profession` (dropdown: `AI Master`, `Video Editor`, `Graphic Designer`)

---

### 2️⃣ Save Raw Data
The initial form data is saved into Airtable for record keeping.

---

### 3️⃣ Switch & Filter by Profession
The workflow uses a **Switch node** to separate users based on their profession:

| Profession        | Rating |
|-------------------|---------|
| AI Master         | ⭐⭐⭐⭐⭐ (5 stars) |
| Video Editor      | ⭐⭐⭐⭐ (4 stars) |
| Graphic Designer  | ⭐⭐⭐ (3 stars) |

Each user is routed and processed based on their selected profession.

---

### 4️⃣ AI Poem Generation
The Google Gemini chat model is used to generate a customized poem based on:
- User name
- Looks
- Profession

The AI creates a short, personalized poem for each user.

---

### 5️⃣ Save Final Data
All processed data is saved into Airtable, including:
- Name  
- Looks  
- Profession  
- Rating  
- Generated poem  

---

## 🛠 Technologies Used

- **n8n** — Workflow automation  
- **Airtable** — Database storage  
- **Google Gemini AI** — Poem generation  
- **Form Trigger** — User input  

---

## 📋 Data Structure (Airtable)

| Field Name  | Type        | Description |
|------------|-------------|-------------|
| Name       | Text        | User's name |
| Looks      | Text        | Description of user's looks |
| Profession | Select      | AI Master / Video Editor / Graphic Designer |
| Rating     | Number      | 3, 4, or 5 |
| Poem       | Long Text   | AI-generated poem |

---

## ⚙️ Setup Instructions

1. Clone or download the workflow.
2. Import the workflow into n8n.
3. Configure:
   - Airtable API Key
   - Base ID and Table names
   - Google Gemini API credentials
4. Connect the form trigger.
5. Activate the workflow.

---

## 🚀 Usage

1. User submits the form.
2. Workflow runs automatically.
3. User is categorized and rated.
4. A personalized poem is generated.
5. Data is stored in Airtable.

---

## 🎯 Purpose

This project demonstrates:
- Automation with n8n
- Smart data routing
- AI integration
- Real-world workflow design

It can be used for:
- Lead categorization
- Smart CRM automation
- Personalized user experiences

---

## 📄 License

This project is open-source and available for learning and demonstration purposes.

---

## 👤 Author

**Abdul Samad**  
n8n Automation Developer  
