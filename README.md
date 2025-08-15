# 🎯 CrewAI Event Planner – Multi-Agent Venue Finder

An **AI-powered multi-agent system** that automates event planning from venue search to marketing, powered by **CrewAI**, **LangChain**, **Groq LLaMA 3.1** models, and **Serper API** for real-time search.  

Simply provide your event details — topic, city, date, expected participants, and budget — and let the agents handle **venue selection, logistics coordination, and marketing strategy**.

## 🚀 Features

- **Multi-Agent Orchestration** 🤖  

  Separate AI agents for venue coordination, logistics, and marketing, working in parallel.

- **Live Web Search** 🌐  

  Real-time venue discovery with Serper API + scraping for detailed insights.

- **Smart Decision Making** 📊  

  Agents reason over budget, capacity, and theme before recommending a venue.

- **Structured Output** 📂  

  Pydantic models and JSON/Markdown reports for clean, machine-readable results.

- **Parallel Task Execution** ⚡ 

  Logistics and marketing agents execute asynchronously to save time.

## 🛠️ Tech Stack

- **[CrewAI](https://github.com/joaomdmoura/crewai)** – Multi-agent orchestration framework  

- **[LangChain](https://www.langchain.com/)** – LLM application framework  

- **[Groq](https://groq.com/)** – Ultra-fast LLaMA 3.1-8B-Instant inference  

- **Serper API** – Google Search API alternative  

- **Python 3.10+** – Backend logic

## ⚙️ How It Works:

- Venue Coordinator Agent:

    Uses SerperDevTool + ScrapeWebsiteTool to find the most suitable venue.

- Logistics Manager Agent:

    Plans catering and equipment setup.

- Marketing & Communications Agent:

    Creates a promotion plan to attract the target audience.

- CrewAI Execution:
    
    Orchestrates agent workflows in sequence and parallel, based on async_execution flags.

## Example Input:

event_details = {

    "event_topic": "Tech Innovation Conference",

    "event_description": "A gathering of tech innovators, startup founders and industry leaders to explore future technologies.",
    
    "event_city": "Hyderabad",
    
    "tentative_date": "2025-08-30",
    
    "expected_participants": 100,
    
    "budget": 20000,
    
    "venue_type": "Conference Hall"
}

## 📜 Example Output:

{

  "name": "T-Hub",

  "address": "Raidurg, Hyderabad",
  
  "capacity": 150,
  
  "booking_status": "Available"
  
}



