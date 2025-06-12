# 🤖 Reddit → Gemini AI → Google Sheets → Slack Automation using n8n

![Stars](https://img.shields.io/github/stars/rishikannaaa/n8n-ai-slack-workflow?style=social)
![Forks](https://img.shields.io/github/forks/rishikannaaa/n8n-ai-slack-workflow?style=social)
![License](https://img.shields.io/github/license/rishikannaaa/n8n-ai-slack-workflow)

This repository contains a powerful automation built using [n8n.io](https://n8n.io). It connects Reddit, Google Gemini (AI model), Google Sheets, and Slack to automate social listening, generate AI responses, and log actionable insights for your team.

---

## 🚀 What It Does

- 🔍 Monitors Reddit and Slack for posts with specific keywords or problems
- 🧠 Sends content to Google Gemini (chat model) for summarization or solutions
- 📄 Saves the problem & AI-generated solution into **Google Sheets (`Sheet1`)**
- 💬 Posts the output to Slack channels (optional or fully automated)
- 🔄 Fully customizable and extendable!

---

## 🖼️ Workflow Overview

This screenshot shows the n8n workflow that:

1. Fetches user queries from Reddit or Slack
2. Processes them through Gemini AI
3. Logs the final output in Google Sheets

<p align="center">
  <img src="./workflow-preview.png" alt="n8n Reddit to Gemini to Google Sheets and Slack workflow" width="800"/>
</p>

---

## 📘 Google Sheets: `problems_in_slack`

All final output is saved in a Google Sheet titled: `Sheet1`, with a worksheet named: **problems_in_slack**.

This sheet contains:

| Timestamp         | Platform | Original Problem                     | Gemini AI Response                                  |
|-------------------|----------|--------------------------------------|-----------------------------------------------------|
| 2025-06-12 12:47  | Slack    | Slack messages not syncing           | Try clearing cache and checking workspace status    |
| ...               | ...      | ...                                  | ...                                                 |

🧠 This helps track community-reported Slack problems and logs AI-generated solutions automatically.

---

## 📂 Files

| File                         | Description                                                  |
|------------------------------|--------------------------------------------------------------|
| `workflow.json`              | Importable n8n workflow file                                 |
| `workflow-preview.png`       | Screenshot of the workflow for visual reference              |
| `problems_in_slack (Sheet1)` | Google Sheet where all extracted problems & solutions are logged |
| `.gitignore`                 | Common ignore rules for GitHub repo                         |
| `README.md`                  | Full documentation and usage guide                          |

---

## 📥 How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/rishikannaaa/n8n-ai-slack-workflow.git
cd n8n-ai-slack-workflow
