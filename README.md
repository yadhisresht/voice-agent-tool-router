# voice-agent-tool-router
This project implements an intelligent tool selection and execution system for a voice assistant, designed mainly for automotive and infotainment use cases.

It combines:

Text embeddings

Cosine similarity

Learning-to-Rank (LTR) scoring

Rule-based NER parsing

to identify the best tool and generate an execution plan from natural language commands.

📌 Features

Embedding-based semantic matching of user queries

Learning-to-Rank (LTR) scoring (XGBoost or mock fallback)

Rule-based NER for entity extraction

Sequential multi-task planning (e.g., navigate → weather → call)

Expandable tool database

Persistent local storage using JSON

🛠 Tools Supported (Examples)

Navigation routing

Weather forecasting

Hands-free calling

Music playback

Vehicle diagnostics

Traffic information

Climate control

Emergency services

(You can easily add more tools.)

🧠 System Architecture (High Level)

User Query

Embedding Generation

Cosine Similarity Matching

LTR-Based Tool Ranking

NER-Based Task Planning

Executable Tool Plan Output

🚀 How to Run
1️⃣ Install Dependencies
pip install numpy requests
pip install xgboost   # optional

2️⃣ Set API Key

Update the following variable in the code:

API_KEY = "YOUR_GOOGLE_GEMINI_API_KEY"

3️⃣ Run the Script
python main.py

💬 Example Queries
Navigate to Chennai and check the weather there
Call Rahul and play some music
Play Arijit Singh songs
What’s the weather when I reach Bangalore?

➕ Add a New Tool

In interactive mode, type:

add


Then enter the tool name and description.
The embedding will be generated and saved automatically.

📁 Data Storage

Tool descriptions and embeddings are stored in:

tools_db_simulated_final.json


This avoids recomputing embeddings on every run.

⚠ Notes

If XGBoost is not available, a mock LTR model is used automatically.

NER is rule-based and may not handle very complex sentences.

Designed for experimentation and research purposes.
