# LifeOS Agent

The **LifeOS Agent** is a personal AI workflow system that automates the repetitive parts of daily life.  
It captures tasks through Telegram, stores them in structured sheets, and sends a smart daily digest at 6PM summarising everything you need to do or buy — in a clean, organised format.

This is the first core module of a larger Agentic AI workflow system I’m building.

---

## 🚀 Features

### **1. Telegram Command Capture**
- `/todo <task>` → saves task into Google Sheets  
- `/buy <item>` → saves shopping item  
- All entries are timestamped and categorised  

### **2. Automatic Daily Summary (6PM)**
At 6PM every day, the agent sends a Telegram message containing:
- Today’s date (formatted cleanly)
- “Things To Do”
- “Things To Buy”
- "Notes"
- Bullet-point lists aggregated from the day
- Clean formatting using Telegram HTML/Markdown

### **3. Google Sheets Storage**
- Stores raw task inputs
- Used as a memory backend
- Organised by timestamp, type, and content

### **4. Modular, Expandable Architecture**
Designed so new agentic modules can plug in later:
- Calendar insights
- Priority ranking
- Weekly summaries
- Habit tracking
- Auto-planning workflows
- Full agent loop with retrieval + memory

---

## 🔧 Tech Stack

- **Make.com**
  - Telegram Watch Messages
  - Google Sheets Search Rows / Add Rows
  - Router-based flow design
  - Text Aggregators
  - Scheduled triggers
- **Google Sheets** (task memory)
- **Telegram Bot** (actions + delivery)
- **HTML/Markdown** (Telegram formatting)

---

## 🧠 Architecture Overview

Telegram Bot --> Make Router -->
↳ /todo branch -----> Google Sheets: Add Row
↳ /buy branch ------> Google Sheets: Add Row

Scheduler (6PM)
↳ Search Rows
↳ Router: todo vs buy
↳ Aggregators
↳ Compose Summary
↳ Telegram: Send Message


---

## 📸 Screenshots
- Task capture through Telegram  
- Make.com scenario  
- Daily summary output  
- Google Sheets storage  

---

## 📅 Roadmap (Next Versions)

### **v0.2 (Next)**
- Weekly summary (Sundays)
- Mark tasks as done
- Auto-clear completed tasks

### **v0.3**
- Calendar integration
- Smart prioritisation (LLM scoring)
- “Plan my tomorrow” agent

### **v1.0**
- Full autonomous agent loop
- Memory-backed planning
- UI dashboard (Streamlit / Vercel)
- Project Timeline UI

---

## 📍 Status
**Version:** v0.1  
**Stage:** Foundation completed — expansion in progress

---

## 👤 Author
**Varsha Ramkumar**  
Data + AI + Automation builder  
Building agentic workflows for personal productivity

