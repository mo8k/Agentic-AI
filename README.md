# 24/7 Autonomous Financial Agent

## 1. Scraping & Memory
The agent acts as a digital librarian. It constantly monitors:

Hard Data: Precise prices and volume from the Polygon.io API.

Soft Data: Global financial news from Yahoo Finance, CNBC, and Bloomberg.

Long-Term Memory: It uses a Vector Database (ChromaDB) to "embed" news. This means it doesn't just read headlines; it understands the math behind the text, allowing it to compare today's news to events from weeks ago.

## Local LLMs

Analysis: The agent uses models like Llama 3.2 to determine if news is "Bullish" or "Bearish."

Reasoning: It combines the hard price numbers with the news context to provide a grounded, hallucination-free outlook.

## 24/7 Services

By deploying this as a Linux System Service, the project becomes "set and forget."

Always-On: The agent runs every hour (or at your preferred interval) even if you are logged out.

Resilience: If the script crashes or the power blinks, the server automatically restarts the agent.

# Monitoring

A Live Dashboard: A private website hosted on your server (Port 8000) where you can see the agent's latest "thoughts" and memory status from any device.

Push Notifications: Instant alerts via Ntfy.sh to your phone when the agent spots high-priority market movements.


