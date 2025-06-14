# Multi-Agent Travel Planner ✈️

## Project Overview

The **Multi-Agent Travel Planner** is an intelligent application designed to generate personalized 3-day travel itineraries based on user-specified cities and interests. Leveraging a locally hosted Large Language Model (LLM) and orchestrated by a multi-agent system built with LangGraph, this tool automates the travel planning process, offering structured and detailed suggestions instantly.

## Features ✨

* **Personalized Itineraries:** Generates custom 3-day travel plans based on user-defined cities and interests.
* **Structured Output:** Itineraries are presented in a clear, time-based format (Morning, Afternoon, Evening) with specific activity, attraction, and food suggestions.
* **Local LLM Integration:** Utilizes Ollama to run powerful LLMs (e.g., Llama3) locally, ensuring privacy and reducing reliance on external APIs.
* **Multi-Agent Workflow:** Implements a LangGraph-based workflow to manage the sequential steps of input collection and itinerary generation.
* **Interactive User Interface:** A user-friendly web interface built with Gradio for easy input and output display.

## Technologies Used 💻

* **Python** 🐍
* **Ollama:** For running local Large Language Models. 🐳
* **Llama3:** The specific LLM model used for content generation. 🧠
* **LangChain:** For interacting with the LLM and prompt engineering. 🔗
* **LangGraph:** For building and orchestrating the multi-agent workflow. ⚙️
* **Gradio:** For creating the interactive web-based user interface. 🌐

## Setup Instructions 🛠️

Follow these steps to get the project running on your local machine.

### 1. Install Ollama and Download the LLM

First, ensure you have Ollama installed and running.

* **Download Ollama:** Visit [ollama.com](https://ollama.com/) and follow the instructions to download and install Ollama for your operating system.
* **Start Ollama Server:** Open your terminal or command prompt and run:
    ```bash
    ollama serve
    ```
    Keep this terminal window open while using the application.
* **Pull Llama3 Model:** In a new terminal, download the Llama3 model:
    ```bash
    ollama pull llama3
    ```
    (If you prefer a different model, remember to update `llm = ChatOllama(model="llama3", ...)` in your `app.ipynb` file.)

### 2. Clone the Repository (Optional, if you are working from a local copy)

If you are setting this up from a fresh clone:

```bash
git clone https://github.com/Mominashaik/Multi_Agent_Travel_Planner
cd Multi_Agent_Travel_Planner
