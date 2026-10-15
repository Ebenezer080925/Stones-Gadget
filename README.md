# 🤖 AI-Powered Telegram Sales Agent (Stones Gadget)

An intelligent, fully automated virtual sales assistant built with **n8n**. This bot interacts with customers on Telegram, answers questions about tech gadgets, checks real-time stock and pricing from Google Sheets, and seamlessly closes sales by generating unique order codes.

## 🌟 Project Overview
This workflow operates as a smart retail assistant. Instead of relying on static menus, the bot uses the **Google Gemini 3.6 Flash** model to understand natural language. It dynamically queries multiple Google Sheets tabs (Direct UK, Also in store, Good deal) to find exactly what the customer is looking for and applies persuasive sales tactics to convert inquiries into purchases.

## 🏗️ Workflow Architecture
![n8n Workflow](image_e36570.png)

### ⚙️ Tech Stack & Integrations
* **Automation Engine:** [n8n](https://n8n.io/)
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

## 🚀 How to Use / Import
1. Clone this repository.
2. Open your n8n instance.
3. Go to **Workflows** -> **Add Workflow** -> **Import from File**.
4. Select the `workflow.json` file included in this repository.
5. **Configure Credentials:**
   * Add your Telegram Bot Token.
   * Add your Google Sheets OAuth2 API credentials.
   * Add your Google Gemini API key.
6. Update the Google Sheets node with your specific Spreadsheet ID.
7. Activate the workflow!

## 💡 Prompt Engineering Highlight
The AI Agent is guided by a robust system prompt that dictates its persona ("Stones Gadget"), rules for formatting Nigerian Naira (₦), handling out-of-stock scenarios gracefully, and strict instructions to *never* hallucinate prices.
