# 🏀 CourtSide Bestie 🎥 (LLM + NBA API Project)

**CourtSide Bestie** is an AI-powered basketball explainer that turns NBA stats into reality-TV-style commentary — powered by the [`nba_api`](https://github.com/swar/nba_api) and an open-source LLM hosted on **Hugging Face** (`google/gemma-2-2b-it`).

> “Turning advanced metrics into main-character moments 💅✨”

---

## 🎯 What It Does

- Pulls **real NBA player stats** (PPG, RPG, APG, TS %) using `nba_api`
- Sends those stats + your question to a **Drama-TV-persona LLM**
- Returns a sassy, easy-to-understand explanation like it’s a confessional on *Love Island* or *The Bachelor*

**Example**

> **You:** What’s TS % and is 63 % good for Shai?  
> **CourtSide Bestie:** “True Shooting % is like how efficiently Shai turns shots into points — that 63 % is full-glam main-character energy.”

---

## 🧠 How It Works

```text
User Question
   ↓
nba_api pulls player stats
   ↓
LLM (Gemma 2 via Hugging Face)
   ↓
Drama-TV Explanation
```

| Layer       | Tech                                                |
| :---------- | :-------------------------------------------------- |
| 💬 Model    | `google/gemma-2-2b-it` (chat model on Hugging Face) |
| 📊 Data     | `nba_api` for official NBA stats                    |
| 🐍 Language | Python 3 (Colab-friendly)                           |
| 🔐 Auth     | Hugging Face access token (`HF_TOKEN`)              |
| 🎨 Tone     | “Reality-TV Confessional Meets ESPN”        |


⚙️ Setup & Run (Colab or Local)
1️⃣ Install Dependencies

```
pip install nba_api pandas huggingface_hub
```
2️⃣ Add Your Hugging Face Token
```
    import os
    os.environ["HF_TOKEN"] = "hf_your_token_here"
```

> Get a free token from huggingface.co/settings/tokens and make sure you’ve accepted access for google/gemma-2-2b-it.

3️⃣ Run the Script
```
    python app.py
 ```   

🌈 Example Output
```
💅 CourtSide Bestie says:
Girl, Luka is serving *the entire season!* His TS % is giving “flawless red-carpet moment.” The league average is mid, but his 63%? Main-character energy, babe.
```

🪄 Prompt Personality
```
You are CourtSide Bestie — the courtside commentator with the energy of a reality TV confessional.

Voice & Style
- Big-sister, energetic, funny, dramatic.  
- Define the stat in plain English, then drop a pop-culture analogy.  
- 2-4 sentences max — quick, dramatic, and fun.  
- Always say if the player is *serving*, *mid*, or *messy* vs NBA standards.
```

🧩 Project Structure
```
courtside-bestie/
│
├── app.py                 # main script (Gemma + nba_api)
├── CourtSideBestie.ipynb  # Colab notebook (optional)
└── README.md              # this file
```

💡 Future Ideas

- 🏆 Compare two players (“Who’s the main character?”)

- 🎨 Streamlit UI with vibe toggle (Drama / Makeup / Classic)

- 🧮 Add advanced metrics (PER, BPM, Win Shares)

- 🎙️ Voice input or TTS output for true podcast energy
