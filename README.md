# AI Weather Agent using Hugging Face & LangChain

## Overview

This project demonstrates an AI-powered weather assistant built using LangChain and a hosted Hugging Face model. The assistant can identify a city from a user query, retrieve weather information using an external API, and generate a natural language response.

Unlike traditional applications where the developer manually controls every step, this project leverages a Large Language Model (LLM) to understand user intent and generate intelligent responses.

---

## Features

* Uses a hosted Hugging Face model (Qwen 2.5 Instruct)
* Integrates LangChain for LLM orchestration
* Fetches real-time weather data using WeatherStack API
* Generates human-like responses
* Demonstrates LLM + API integration
* Simple and beginner-friendly implementation

---

## Tech Stack

### Languages

* Python

### Frameworks & Libraries

* LangChain
* LangChain Hugging Face
* Hugging Face Hub
* Requests

### Model

* Qwen/Qwen2.5-7B-Instruct

### External API

* WeatherStack API

---

## Project Workflow

### Step 1: User Query

The user provides a question such as:

"Find the capital of Madhya Pradesh and tell me its current weather."

### Step 2: City Identification

The Hugging Face model analyzes the query and identifies the city.

Example:

Capital of Madhya Pradesh → Bhopal

### Step 3: Weather Retrieval

The application sends a request to the WeatherStack API and retrieves:

* Temperature
* Weather condition
* Humidity
* Wind speed

### Step 4: Response Generation

The weather information is passed back to the language model, which generates a natural language response.

Example:

"The capital of Madhya Pradesh is Bhopal. The current weather in Bhopal is Sunny with a temperature of 29°C and humidity of 61%."

---

## Installation

Install required dependencies:

```bash
pip install langchain
pip install langchain-huggingface
pip install huggingface_hub
pip install requests
```

---

## Configuration

### Hugging Face Token

Create an account on Hugging Face and generate an access token.

Set the token:

```python
import os

os.environ["HUGGINGFACEHUB_API_TOKEN"] = "YOUR_HF_TOKEN"
```

### WeatherStack API Key

Create a free WeatherStack account and obtain an API key.

```python
WEATHERSTACK_API_KEY = "YOUR_API_KEY"
```

---

## Project Architecture

User Query
↓
Hugging Face LLM
↓
Identify City
↓
Weather API
↓
Weather Data
↓
Hugging Face LLM
↓
Final Response

---

## Sample Input

```text
Find the capital of Madhya Pradesh and tell me its current weather.
```

## Sample Output

```text
The capital of Madhya Pradesh is Bhopal.
The current weather in Bhopal is Sunny with a temperature of 29°C and humidity of 61%.
```

---

## Learning Outcomes

This project demonstrates:

* Large Language Model integration
* Prompt engineering
* API consumption using Python
* LangChain fundamentals
* Real-time data retrieval
* AI-powered response generation

---

## Future Enhancements

* Support multiple weather providers
* Add Streamlit frontend
* Voice-based interaction
* Multi-city weather comparison
* Conversational memory
* Tool-calling agents
* Deployment on cloud platforms

---

## Conclusion

This project showcases how Hugging Face models and LangChain can be combined with external APIs to create intelligent AI assistants. It serves as a practical introduction to agentic AI systems, tool integration, and real-time information retrieval.
