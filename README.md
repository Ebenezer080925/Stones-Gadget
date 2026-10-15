# 🤖 AI-Powered Telegram Sales Agent (Stones Gadget)

An intelligent, fully automated virtual sales assistant built with **n8n**. This bot interacts with customers on Telegram, answers questions about tech gadgets, checks real-time stock and pricing from Google Sheets, and seamlessly closes sales by generating unique order codes.

## 🌟 Project Overview
This workflow operates as a smart retail assistant. Instead of relying on static menus, the bot uses the **Google Gemini 3.6 Flash** model to understand natural language. It dynamically queries multiple Google Sheets tabs (Direct UK, Also in store, Good deal) to find exactly what the customer is looking for and applies persuasive sales tactics to convert inquiries into purchases.

## 🏗️ Workflow Architecture
![n8n Workflow](https://github.com/Ebenezer080925/Stones-Gadget/blob/main/Screenshot%202026-10-15%20142710.png)

### ⚙️ Tech Stack & Integrations
* **Automation Engine:** n8n
* **AI Model:** Google Gemini Chat Model (gemini-3.6-flash) via LangChain
* **Database/Inventory:** Google Sheets (Real-time read/write)
* **User Interface:** Telegram Bot API
* **Memory:** Simple Memory (Buffer Window) for maintaining conversational context per user.

## ✨ Key Features
* **Conversational AI:** Warm, friendly, and emoji-rich interactions tailored to a premium tech store persona.
* **Dynamic Inventory Search:** AI Agent automatically decides which Google Sheet tab to search based on the user's prompt.
* **Fuzzy Matching:** Capable of understanding variations in product names (e.g., matching "S22 Ultra" from the chat to "Samsung S22 U" in the database).
* **Context-Aware Memory:** Remembers the user's chat history within the session to provide natural, multi-turn conversations.
* **Automated Order Processing:** Once a customer confirms an intent to buy, the bot generates a unique 6-character order code (e.g., STONES-9A2Z) and hands off the payment instructions. 

### Telegram Conversation 
![](https://github.com/Ebenezer080925/Stones-Gadget/blob/main/telegram%20chatbot.png)

### Google sheet for Workflow to get prices
![](https://github.com/Ebenezer080925/Stones-Gadget/blob/main/Screenshot%202026-10-15%20143213.png)
![](https://github.com/Ebenezer080925/Stones-Gadget/blob/main/Screenshot%202026-10-15%20143236.png)
![](https://github.com/Ebenezer080925/Stones-Gadget/blob/main/Screenshot%202026-10-15%20143258.png)
