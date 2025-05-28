# 🚗 Roadtrip Planner Full
An intelligent and customizable road trip planner powered by CrewAI agents. This planner builds a detailed, cost-aware travel itinerary based on user preferences like:
- Starting location & destination
- Travel dates and number of days
- Number of travelers (adults & children)
- Hotel preferences and brands
- Dietary needs (e.g., Halal, Kosher, Vegetarian)
- Fuel efficiency and gas cost
- Total trip budget
## 🧠 Features
- Plans fastest route using highway data
- Recommends hotels by type, brand, and group size
- Calculates fuel cost based on MPG and tank size
- Suggests attractions and activities open during your dates
- Recommends restaurants based on dietary preferences
- Generates a markdown itinerary with daily plans and full budget breakdown
- Flags over-budget items as optional
## ⚙️ Setup & Usage
1. **Clone this Repository**
 ```bash
 git clone https://github.com/yourusername/roadtrip-planner-full.git
 cd roadtrip-planner-full
 ```
2. **Create a Virtual Environment** (optional but recommended)
 ```bash
 python -m venv venv
 source venv/bin/activate # On Windows: venv\Scripts\activate
 ```
3. **Install Required Packages**
 ```bash
 pip install -r requirements.txt
 ```
 Example `requirements.txt`:
 ```txt
 crewai==0.28.8
 crewai_tools==0.1.6
 langchain_community==0.0.29
 ```
4. **Add `utils.py`**
 Create a file named `utils.py` in the project root with:
 ```python
 import os
 def get_openai_api_key():
 key = os.getenv("OPENAI_API_KEY")
 if not key:
 raise ValueError("OPENAI_API_KEY environment variable is not set.")
 return key
 ```
5. **Configure Your OpenAI API Key**
 - **macOS/Linux:**
 ```bash
 export OPENAI_API_KEY="sk-...your-key..."
 ```
 - **Windows CMD:**
 ```cmd
 set OPENAI_API_KEY=sk-...your-key...
 ```
6. **Run the Planner**
 ```bash
 python roadtrip_planner.py
 ```
 Follow the prompts to enter:
 - Starting location and destination
 - Number of adults and children
 - Hotel type, brand, and budget
 - Dietary preference
 - Fuel efficiency and gas price
 - Trip start date and total days
 - Maximum total budget
---
7. **Author**
AliA
8. **License**
This project is licensed under the MIT License. You may replace it with another license as needed
