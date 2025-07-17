#  🤖 Smart Feedback Classifier


This n8n workflow automates the entire feedback process — from collecting user feedback via form to classifying, responding, and organizing it in Airtable. Perfect for product teams, support desks, or customer success operations.

---

## 📌 Project Overview

When a user submits a feedback form (Name, Email, Feedback):

1. 🔍 **Classification Agent**:
   - The AI agent analyzes the feedback content and classifies it into:
     - Complaint
     - Query / Suggestion
     - Feature Update / Request
     - Compliment

2. 🧠 **LLM-based Response Generator**:
   - The agent generates a **contextual email reply** based on the type of feedback.

3. 🧩 **Merge Node**:
   - Combines both the original input and the AI-generated response.

4. 🔀 **Switch Logic**:
   - Routes the entry to the appropriate Airtable view:
     - 🟡 `Complaints`
     - 🟢 `Feature Updates`
     - 🔵 `Compliments`

5. 📥 **Airtable Integration**:
   - Each entry is logged under the corresponding category.

6. 📧 **Email Node**:
   - Sends a personalized email back to the user confirming receipt and sharing the response.

---

## 🧰 Tools & Integrations Used

| Tool        | Purpose                          |
|-------------|----------------------------------|
| **n8n**     | No-code workflow automation      |
| **Airtable**| Data storage & categorization    |
| **Gmail**   | Sending response emails          |
| **LLM (Gemini)** | AI classification & reply generation |
| **Form Submission (Frontend)** | User feedback capture |

---

## 💡 Key Features

- 🤖 AI-powered feedback classification  
- 📨 Auto-personalized email replies  
- 🗂 Categorized storage in Airtable  
- 🔀 Conditional routing with Switch node  
- 💬 Real-time acknowledgment to users  

---

## 📸 Screenshots

*Add screenshots of your n8n workflow in an `/assets/` folder or directly in the repo.*

---

## 🧪 Sample Output

**Submitted Feedback**:
> *"The dark mode feature is amazing! Great job!"*

**Predicted Category**:
> Compliment

**Response Email**:
```text
Dear [John],
Thank you for your kind words and positive feedback!
It truly means a lot to us when our customers take the time to share their appreciation. Compliments like yours motivate our entire team to continue striving for excellence.
Warm regards,  
Lavish  
Customer Experience Team  
Lavish AI Agent
