🌍 Beautiful Travel Itinerary Planner

📌 Overview
The Beautiful Travel Itinerary Planner is an AI-powered application that generates personalized day trip itineraries for any city based on user-provided interests.
It uses Multi-Agent architecture with LangGraph, LangChain, and Gradio to create a smooth, interactive experience for travel planning.

This project demonstrates:

StateGraph for defining the flow

PlannerState for storing context

Node functions for modular steps

LLM integration for natural language itinerary generation

🚀 Features
🏙 City-specific itinerary generation

🗺 Interest-based customization (temples, beaches, malls, markets, etc.)

🕒 Time-slotted schedules for the day

🔄 Multi-Agent flow for input handling, processing, and generation

🎨 Beautiful UI built with Gradio

⚡ Powered by Groq’s LLaMA 3.3 70B model for fast and high-quality text generation

🛠 Tech Stack
Python 3.10+

LangChain – For building LLM applications

LangGraph – For state-based agent workflows

Groq API – LLaMA 3.3-70B model for fast, accurate itinerary generation

Gradio – For interactive web UI

🧩 Key Components
1. StateGraph
Defines the workflow of the planner using nodes and edges:

Entry point → input_city → input_interest → create_itinerary → END

2. PlannerState
Stores the current state of the planning process:
class PlannerState(TypedDict):
  messages : Annotated[List[HumanMessage | AIMessage], "Conversation history"]
  city : str
  interests : List[str]
  itinerary : str
3. Node Functions
Each node in the workflow is a function:

input_city → Get the city name

input_interest → Get the user's interests

create_itinerary → Call LLM to generate the itinerary

4. LLM Integration
Uses Groq LLaMA 3.3-70B model with a custom prompt to produce structured, bulleted itineraries.

📂 Project Structure
├── app.py                # Main application code
├── requirements.txt      # Dependencies
├── README.md             # Documentation

🖼 Example Output
Input:

City: Chennai

Interests: vadapalani temple, t nagar, mall, marina beach

Generated Itinerary:
* 8:00 AM - 9:00 AM: Visit the Vadapalani Temple, a famous shrine dedicated to Lord Murugan  
* 10:00 AM - 12:00 PM: Explore T. Nagar, a bustling shopping district, and shop for souvenirs or try some local street food  
* 12:30 PM - 2:30 PM: Head to a nearby mall, such as the Phoenix MarketCity or Express Avenue, for lunch and some retail therapy  
* 3:30 PM - 5:30 PM: Relax and unwind at Marina Beach, one of the longest urban beaches in the country, and enjoy the sunset  
* 6:00 PM: End the day with a delicious dinner at a local restaurant, trying some of Chennai’s famous

  <img width="1366" height="768" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/a7df73f2-6e6c-4422-9f1f-d133bb4d8bfa" />


  Video Explanation Link:
  https://drive.google.com/file/d/1bUimAEggk57hkJ0VlCIHwggKp7Z4R9iz/view?usp=drivesdk
  

