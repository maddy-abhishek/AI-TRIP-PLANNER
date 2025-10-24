# 🌍 AI Travel Agent

This project is a full-stack AI Travel Agent application. It combines a powerful FastAPI backend with a user-friendly Streamlit frontend. The backend uses a multi-tool agentic workflow (powered by LangGraph and Groq) to answer complex travel queries, fetch real-time data, and generate detailed travel plans.

The agent is equipped with a suite of tools to:

- Find Places: Search for attractions, restaurants, and activities using Google Places (with Tavily as a fallback).

- Get Weather: Fetch current weather and multi-day forecasts from OpenWeatherMap.

- Calculate Expenses: Estimate hotel costs, sum total trip budgets, and calculate daily allowances.

- Convert Currency: Get real-time exchange rates.

- Save Plans: Automatically save the generated itineraries as formatted Markdown files.

## 🚀 Features

- Streamlit Web UI: A simple and interactive chat interface built with Streamlit to talk to the travel agent.

- FastAPI Backend: A robust, asynchronous API server that handles the agent logic.

- High-Speed Inference: Integrates with the Groq API for extremely fast LLM responses.

- Multi-Tool Agentic Workflow: Uses LangGraph to intelligently route user requests to the correct tool (Weather, Places, Calculator, etc.).

- Real-time Data:

   - Place Search: Fetches attractions, restaurants, activities, and transport options from the Google Places API.

   - Weather: Gets live weather and 5-day forecasts from OpenWeatherMap.

   - Currency: Provides up-to-date currency conversions.

- Fallback Mechanism: Includes a fallback from Google Places to Tavily Search to ensure high availability of information.

- Markdown Export: Automatically saves the agent's final travel plan as a neatly formatted Markdown file in the ./output directory.

- Graph Visualization: On the first backend query, it generates a my_graph.png file to visualize the agent's workflow.

## 🛠️ Technologies Used

- Frontend: Streamlit

- Backend: FastAPI, Uvicorn

- LLM Provider: Groq

- Agent Framework: LangGraph, LangChain (for tools)

- Data Validation: Pydantic

- External APIs:

    - Google Places API

    - OpenWeatherMap API

    - Tavily Search API

    - ExchangeRate-API (or similar)

## ⚙️ Setup and Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/maddy-abhishek/AI-TRIP-PLANNER.git
   ```
2. Create virtual environment:

   ```bash
   uv init
   ```

   ```bash
   uv venv env
   ```

   ```bash
   env\Scripts\activate.bat
   ```

3. Install the required dependencies:

   ```bash
   uv pip install -r requirements.txt
   ```

4. Add all your API keys to this file:

GROQ_API_KEY=""

GOOGLE_API_KEY=""

GPLACES_API_KEY=""

FOURSQUARE_API_KEY=""

TAVILAY_API_KEY=""

OPENWEATHERMAP_API_KEY=""

EXCHANGE_RATE_API_KEY=""

## ▶️ How to Use

You need to run two processes in two separate terminals: the Backend API and the Frontend App.

Terminal 1: Run the Backend (FastAPI)

```bash
uvicorn main:app --reload --port 8000
```

Terminal 2: Run the Frontend (Streamlit)

```bash
streamlit run app.py
```









