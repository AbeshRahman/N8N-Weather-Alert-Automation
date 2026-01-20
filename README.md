# N8N-Weather-Alert-Automation

This repository contains an **n8n workflow** that automates the delivery of personalized weather reports. It fetches real-time meteorological data, processes it through an **AI Agent** powered by **Google Gemini**, and sends a natural language summary to **Telegram**.

## 🚀 Workflow Visualization

![Weather Alert Automation Workflow](https://github.com/AbeshRahman/N8N-Weather-Alert-Automation/blob/main/Weather%20Alert%20Automation%20Workflow.png)
*The complete n8n canvas: Scheduled trigger → Weather API request → AI processing → Telegram notification.*

---

## 🛠️ How it Works

1.  **Schedule Trigger**: Automatically initiates the workflow at defined intervals.
2.  **HTTP Request**: Fetches live weather data for **Dhaka** from the WeatherAPI (e.g., temperature, humidity, wind).
3.  **AI Agent (Google Gemini)**: 
    * Receives raw JSON data via the **Aggregate** node.
    * Acts as a weather information agent to transform technical data into human-readable reports.
    * Strictly avoids technical jargon or assumptions, focusing on a professional, concise summary.
4.  **Telegram Bot**: Delivers the final AI-generated report directly to the user.

---

## 📊 AI Processing & Telegram Output

### AI Input & Output
![AI Agent Logs](https://github.com/AbeshRahman/N8N-Weather-Alert-Automation/blob/main/Logs%2C%20AI%20Agent%20Input%20%26%20Output.png)
*Left: Raw location and current weather data. Right: The AI-refined output in a clear sentence format.*

### Final Telegram Notification
![Telegram Delivery](https://github.com/AbeshRahman/N8N-Weather-Alert-Automation/blob/main/Weather%20Info%20Sent%20to%20Telegram.png)
*Real-time weather alerts as they appear in the Telegram app, including temperature, humidity, and wind speed.*

---

## 📥 Setup Instructions

1.  **Import Workflow**: Copy the content of `Weather Alert Automation.json` and paste it into your n8n canvas.
2.  **API Credentials**:
    * **WeatherAPI**: Sign up at [WeatherAPI.com](https://www.weatherapi.com/) and replace the "Key" value in the HTTP Request node.
    * **Google Gemini**: Connect your Google Palm/Gemini API key.
    * **Telegram**: Create a bot via [@BotFather](https://t.me/botfather) and enter your Bot Token and `chatId`.
3.  **Customize Location**: Change the `q` parameter in the HTTP Request node to your desired city.

---
