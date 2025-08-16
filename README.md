# Task_05_Descriptive_Stats

## 📊 Project Overview

This project explores descriptive statistics and prompt engineering using the 2025 Syracuse University Women’s Lacrosse team dataset. The objective is to generate statistical insights from the dataset using Python, then craft natural language prompts to query the same insights from a large language model (LLM) and evaluate its performance.

## 📁 Dataset

The dataset includes individual-level performance statistics for players such as:
- Goals (G), Assists (A), Points (PTS)
- Shots (SH), Shot % (SH%)
- Shots on Goal (SOG), SOG%
- Ground Balls (GB), Draw Controls (DC)
- Turnovers (TO), Caused Turnovers (CT)
- Fouls, Cards, Games Played–Started (GP–GS)

⚠️ Note: The dataset file (`WOMENS_2025_TEAM.csv`) is **not** included in the repository per instructions.

## 🔧 Methodology

All analysis was performed in a Google Colab notebook and included:
- Data cleaning and feature preparation
- Splitting `GP-GS` into two new columns: `GP` and `GS`
- Numeric conversion of relevant fields
- Calculation of key statistics (totals, averages, top performers)
- Creation of a custom `impact_score` metric to estimate the "most improved player"

## ✅ Completed Questions

Descriptive statistics were calculated to answer the following:

1. How many games did this team play?
2. What was the team’s average goals per game?
3. What was the team’s average assists per game?
4. Which player had the highest shot accuracy?
5. Which player committed the most turnovers?
6. Which player had the most ground balls?
7. Who scored the most goals this season?
8. Who was the most improved player (using custom metric)

These were also cross-checked using LLM-generated responses.

## ✏️ Prompt Engineering

A separate document (`LLM_Prompts_Task_5.pdf`) outlines the natural language prompts corresponding to each of the above statistics. These prompts were submitted to an LLM via API for evaluation.

## 🤖 LLM Integration

In the second phase, we used the Groq API with the LLaMA 3 (70B) model to answer each of the 8 prompts. Since raw CSV input is too large for LLMs, the dataset was summarized into a readable format and provided as context.

For each prompt:
- The model’s answers were printed and stored.
- Answers were compared against the Python results.
- Minor discrepancies were documented in assists per game and goals per game.

A reflection summary and failure analysis have been added to document the LLM’s accuracy, reasoning quality, and limitations.

## 📊 Visualizations

Two basic visualizations were added:
- Goals scored vs. Player Names
- Custom Impact Score vs. Turnovers

These visualizations helped verify outlier performance and interpretation accuracy.

## 📌 Reflection Summary

This project combined basic statistical analysis with LLM reasoning evaluation. The LLM performed well on simple factual prompts but struggled slightly with derived or aggregate metrics. Despite minor discrepancies, this approach shows strong potential for using LLMs in sports analytics.

## 🗂️ Files in Repository

- `LLM.ipynb`: Full Google Colab notebook with cleaned data, Python stats, prompts, and LLM API calls
- `README.md`: Project description (this file)
- `LLM_Prompts_Task_5.pdf`: All 8 prompts used for LLM testing

🚫 The actual dataset (`WOMENS_2025_TEAM.csv`) is excluded from this repo per instruction.

## 🧪 Future Exploration

- Try alternate models (Claude, ChatGPT-4o) for answer accuracy
- Introduce ambiguous judgment prompts (e.g. which player could help win more games)
- Visualize LLM accuracy vs. ground truth for all questions

