# ✈️ Travel Booking Agent – Microsoft Copilot Studio

---

## 🌟 Project Overview
The **Travel Booking Agent** is a no-code conversational AI built entirely in **Microsoft Copilot Studio**.  
It helps users plan and book trips efficiently by:  

- 🧑‍💼 Collecting traveler details  
- 📊 Storing itineraries in Excel  
- ✉️ Sending automated email confirmations  
- 🌍 Fetching travel info dynamically  

This project demonstrates how **Copilot Studio** automates workflows using **topics, entities, and agent flows**.

---

## 🛠️ Agent Setup in Copilot Studio

### 1️⃣ Agent Creation
- **Name:** `TripPlanningAgent` ✈️  
- **Description:** Collects name, email, destination, and dates; saves itinerary & sends confirmation  
- **Orchestration:** Classic orchestration enabled

### 2️⃣ Knowledge Source
- Source: [Travel Wiki](https://en.wikipedia.org/wiki/Travel) 🌐  
- Mode: Generative enabled → fetches live travel info

### 3️⃣ Excel Itinerary Tracker
- File: `Travel Itinerary.xlsx` 💾  
- Table headers: Name | Email | TripDestination | StartDate | EndDate | FlightPreference | HotelPreference | TravelInterests  
- Bookings added automatically via **Agent Flow** 🔄

---

## 🧩 Topics Created

### **TravellerDetails** 🧳
- **Purpose:** Collect user info & confirm  
- Prompts:
  - 🧑‍💼 Name  
  - ✉️ Email  
  - ✅ Confirm details  
- Stores responses for flow continuation

### **TravelDetails** 🌍
- **Trigger Phrases:** “plan my trip”, “register my trip planning”  
- Collects:
  - 🗺️ Destination  
  - 📅 Start & End Dates  
  - ✈️ Flight Preference  
  - 🏨 Hotel Preference  
  - 🎯 Travel Interests  
- Redirects to **TravellerDetails** for confirmation  
- Calls **TravelRegistryFlow** 🔁

---

## 🔄 Agent Flow: TravelRegistryFlow
- **Purpose:** Save travel details to Excel & send email ✉️  
- **Steps:**  
  1. ➕ Add row to Excel  
  2. ✉️ Send confirmation email

---

## ✅ Testing the Agent
- **Conversation example:**  
  1. User: “Plan my travel” 🗨️  
  2. Bot asks Name 🧑‍💼 → response  
  3. Bot asks Email ✉️ → response  
  4. Bot collects trip details 🌍 → confirmation  
  5. Bot adds row in Excel 📊 & sends email ✉️  

- **Verification:**  
  - 📊 Excel row added  
  - ✉️ Email confirmation received

---

## 🚀 Publishing the Agent
- Click **Publish** 🌟  
- Optional: enable demo website 🌐


