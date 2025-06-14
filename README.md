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
```

### 3. Create a Virtual Environment (Recommended)

It's good practice to use a virtual environment to manage project dependencies.

```bash
python -m venv venv
# On Windows:
.\venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### 4. Install Dependencies

Install all necessary Python packages using the 'requirements.txt' file:

```bash
pip install -r requirements.txt
```

### How to Run ▶️

1. Ensure Ollama server is running (as per Setup Step 1: ollama serve).

2. Open the Jupyter Notebook:

   ```bash
   jupyter notebook app.ipynb
   ```
   
3. Run all cells in the app.ipynb notebook. The last cell will automatically launch the Gradio web interface in your browser.

### Usage 💡
Once the Gradio application launches (it will open in your browser or provide a local URL):

Enter your desired City (e.g., "Tokyo", "Rome").
Enter your Interests as a comma-separated list (e.g., "food, history, art", "beaches, opera, nature").
Click the Submit button.
Your personalized 3-day travel itinerary will appear in the "Your Travel Itinerary" output area.

Example 🗺️

Input:

City: Sydney
Interests: beaches, opera, nature

Expected Output:

A detailed 3-day itinerary for Sydney focusing on beaches, the opera house, and natural attractions, structured by morning, afternoon, and evening activities.
