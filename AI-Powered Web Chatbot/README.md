# 🤖 ChatWithMe – AI Powered Chatbot  
A modern, interactive AI chatbot built using **Streamlit**, **n8n automation**, and **Google Gemini AI**.  
ChatWithMe delivers real-time responses, typing animations, feedback learning, and smooth conversational flow—designed to feel natural and intuitive.

---

## 🚀 Features

### 💬 Real-Time AI Chat
- Send any message and get an instant AI-generated response.
- Clean and minimal chat interface for the best user experience.

### ✨ Typing Animation (ChatGPT-like)
- Assistant messages appear with a smooth typing effect for a natural, engaging chat feeling.

### 👍👎 Feedback System
- Rate responses with **Good** or **Bad**.
- Feedback is sent to n8n for processing.
- The AI improves and responds with acknowledgement automatically.

### 🔄 Regenerate Response
- Request an alternative answer anytime.
- Calls the n8n workflow again to generate a better response.

### 🧠 Memory-Enabled Conversations
- Uses an n8n memory buffer to maintain context across messages.
- Allows deeper, more meaningful multi-turn conversations.

### ⚙️ Powered by Modern Tech
- **Streamlit** for frontend chat interface  
- **n8n** as backend workflow automation  
- **Google Gemini (LLM)** for generating responses  
- **Python** for full control and customization  

---

## 🛠 Tech Stack

- **Python**
- **Streamlit**
- **n8n Workflows**
- **Google Gemini LLM**
- **REST APIs**
- **Session State Management**

---

## 📌 How It Works

1. User enters a message in the Streamlit chat box.  
2. The message is sent to the n8n webhook.  
3. n8n processes the text using Gemini AI and returns a response.  
4. Response appears with a typing animation.  
5. User can rate the message or request regeneration.  
6. Feedback is sent back to n8n to adjust or improve replies.  

---



                    ┌──────────────────────┐
                    │      User Input       │
                    │  (Streamlit Chat UI)  │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │   Streamlit Frontend │
                    │  - Displays messages │
                    │  - Typing animation  │
                    │  - Feedback buttons  │
                    └───────────┬───────────┘
                                │  HTTP POST (JSON)
                                ▼
                    ┌──────────────────────┐
                    │      n8n Webhook     │
                    │ Receives user prompt │
                    └───────────┬───────────┘
                                │
                                ▼
                   ┌────────────────────────┐
                   │       AI Agent Node     │
                   │ - Handles prompt logic  │
                   │ - Checks feedback flag  │
                   │ - Routes to Gemini      │
                   └───────────┬────────────┘
                               │
                               ▼
                 ┌────────────────────────────┐
                 │  Google Gemini AI (LLM)     │
                 │ Generates intelligent reply │
                 └───────────┬────────────────┘
                               │
                               ▼
                   ┌────────────────────────┐
                   │  Memory Buffer (optional)│
                   │ Maintains chat context   │
                   └───────────┬─────────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Send response to UI  │
                    └───────────┬──────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │ Streamlit Chat UI    │
                    │  - Typing animation  │
                    │  - Show regenerate   │
                    │  - Show feedback     │
                    └──────────────────────┘



  🧠 Explanation (Simple & Clear)
1. User → Streamlit

User sends a message through the chat UI.

2. Streamlit → n8n Webhook

Request is converted into JSON and sent to your n8n webhook.

3. Webhook → AI Agent

AI Agent:

Reads the prompt

Checks if "feedback" exists

Sends query to Gemini

4. Gemini → AI Agent

Google Gemini generates the reply.

5. AI Agent → Streamlit

Response is sent back to Streamlit.

6. Streamlit:

Shows typing animation

Displays the answer

Shows feedback buttons

Hides buttons after feedback


## 📸 UI Preview  
  <img width="1919" height="873" alt="Screenshot 2025-11-26 222308" src="https://github.com/user-attachments/assets/1810a11a-f245-4881-9705-a654cf776455" />

 ---

 ## ChatWthME Architecture Diagram

 <img width="1024" height="1536" alt="ChatGPT Image Nov 26, 2025, 11_57_25 PM" src="https://github.com/user-attachments/assets/0b5c4194-2d36-4500-8f0f-90b794a2f596" />


 ---


 






