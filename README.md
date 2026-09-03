# 🎥 AI YouTube Video Analyzer

An AI-powered YouTube Video Analyzer built using **Agno**, **Groq**, **Qwen**, and **Streamlit**.

The application takes a YouTube video URL from the user and uses an AI agent with YouTube tools to analyze the video's metadata, structure, major topics, important moments, and timestamps. The generated analysis is displayed through a simple Streamlit web interface.

---

## 📌 Project Overview

This project demonstrates how an **AI Agent can interact with an external tool to analyze YouTube content** instead of simply generating an answer from the LLM's internal knowledge.

The user provides a YouTube video URL through the Streamlit interface.

The application then:

1. Receives the YouTube URL.
2. Passes the URL to an Agno AI Agent.
3. The agent uses `YouTubeTools` to gather information from the video.
4. The Qwen LLM running through Groq processes the available video information.
5. The agent follows a predefined analysis workflow.
6. A structured analysis report is generated.
7. The report is displayed in the Streamlit application.

---

## 🧠 How the Project Works

The overall workflow is :

```text
                    User
                     │
                     ▼
             Streamlit Interface
                     │
                     │ YouTube URL
                     ▼
             YouTube Video Agent
                     │
                     ▼
                Qwen LLM
               via Groq API
                     │
                     ▼
               YouTubeTools
                     │
                     ▼
          YouTube Video Information
                     │
                     ▼
             AI Analysis
                     │
                     ▼
              Analysis Report
                     │
                     ▼
             Streamlit UI
