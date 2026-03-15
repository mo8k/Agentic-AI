# 24/7 Autonomous Financial Agent: Hybrid RAG & Multi-Agent System

This project is a self-sustaining AI ecosystem deployed on a private server, designed to perform professional-grade market analysis, real-time data synthesis, and autonomous research without human intervention. By combining local Large Language Models (LLMs) with real-time financial APIs and a vector-based "memory," this system bridges the gap between static AI knowledge and the volatile nature of global markets.

## 1. Intelligent Data Acquisition & Semantic Memory
The Knowledge Layer acts as the agent's "senses" and "long-term memory," ensuring all analysis is grounded in verified, real-time facts rather than LLM training data.

Hard Data Integration (Ground Truth): The system interfaces directly with the Polygon.io API to fetch high-precision technical data, including previous closes, price aggregates, and trading volume. This provides a "hard data" foundation that prevents the AI from hallucinating numerical values.

Soft Data Acquisition (Scraping): An autonomous scraping engine monitors global financial sentiment by parsing RSS feeds and HTML content from premier sources, including CNBC, Yahoo Finance, and Bloomberg.

Semantic Memory & RAG: Using ChromaDB (a vector database), the agent converts raw text into mathematical Embeddings using the nomic-embed-text model. This allows the agent to perform Retrieval-Augmented Generation (RAG), enabling it to compare current headlines with historical events stored in its 32GB RAM-backed database for deep contextual analysis.

## 2. The Intelligence Layer: Local Reasoning via NVIDIA GPU

Instead of relying on cloud-based APIs, all computational "thinking" is performed locally on an NVIDIA GTX 1660 Super, ensuring total data privacy and zero subscription costs.

Logic & Analysis: The system utilizes Llama 3.2 (3B) as its primary reasoning engine to determine market sentiment and identify correlations between news and price action.

Quant Analysis: Specialized models like DeepSeek-R1 or Qwen-Coder are utilized for "Chain of Thought" reasoning when deep logical debugging or complex financial calculations are required.

## 3. The Automation Layer: 24/7 Autonomous Operations

Designed for "set and forget" reliability, the system is deployed as a Linux Systemd Service to ensure the workforce never sleeps.

Always-On Execution: The agent operates on a scheduled loop (e.g., hourly), performing research and analysis cycles independently.

Fault Tolerance: The service architecture includes automatic recovery protocols; if a process crashes or the server reboots, the system restarts the AI agents immediately to maintain continuity.

## 4. The Visibility Layer: Monitoring & Real-Time Alerts

Despite being autonomous, the system provides full transparency through two primary channels:

Live Web Dashboard: A custom FastAPI dashboard (hosted on Port 8000) provides a real-time visual of the agent's current "thoughts," the number of items in its vector memory, and a log of recent analysis reports.

Push Notifications: A direct integration with Ntfy.sh delivers high-priority market alerts and "Bullish/Bearish" sentiment summaries directly to your mobile devices the moment the agent completes a cycle.

## Hardware Optimization

This project is specifically optimized for consumer-grade hardware with high memory capacity:

32GB System RAM: Utilized to keep the entire ChromaDB vector index in "hot" memory, allowing for near-instant semantic searches across thousands of archived articles.

6GB VRAM (GTX 1660 Super): Optimized to run quantized models that balance high-speed inference with stable 24/7 thermal performance.
