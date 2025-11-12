# 🏀 CourtSide Bestie

**CourtSide Bestie** is an AI-powered basketball explainer that breaks down NBA stats in a fun, friendly, and approachable way — powered by the `nba_api` and an open-source LLM hosted on Hugging Face.

> “Turning advanced metrics into bestie talk 💅”

---

## 🎯 What It Does

- Fetches **live NBA player stats** (points, rebounds, assists, TS%) using [`nba_api`](https://github.com/swar/nba_api)  
- Sends them, along with your natural-language question, to a **conversational LLM** (`google/gemma-2-2b-it`)  
- Returns an **easy-to-understand, hype explanation** aimed at newer fans

Example:
> **You:** What’s TS% and is 63% good for Shai?  
> **CourtSide Bestie:** “True Shooting % is like how efficiently a player turns shots into points...”

---

## 🧠 How It Works

```text
User Question ➜ nba_api pulls player stats ➜
LLM (Gemma 2) explains stats ➜
Output = Friendly Explanation
🧩 Model: google/gemma-2-2b-it

⚙️ Libraries: nba_api, huggingface_hub, pandas

💻 Environment: Google Colab / Python 3.10+

🔐 API: Hugging Face token (no paid keys required)
