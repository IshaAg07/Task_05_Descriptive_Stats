# Task_05_Descriptive_Stats

## 📊 Project Overview

This project explores descriptive statistics and prompt engineering using the 2025 Syracuse University Women’s Lacrosse team dataset. The objective is to generate statistical insights from the dataset and then craft natural language prompts to query the same insights from a large language model (LLM) in the next phase.

## 📁 Dataset

The dataset includes individual-level performance statistics for players such as:
- Goals (G), Assists (A), Points (PTS)
- Shots (SH), Shot % (SH%)
- Shots on Goal (SOG), SOG%
- Ground Balls (GB), Draw Controls (DC)
- Turnovers (TO), Caused Turnovers (CT)
- Fouls, Cards, Games Played–Started (GP–GS)

⚠️ Note: The dataset file (`WOMENS_2025_TEAM.csv`) is not included in the repository per instructions.

## 🔧 Methodology

All analysis was performed in a Google Colab notebook and included:
- Data cleaning and feature preparation
- Numeric conversion of relevant fields
- Splitting `GP-GS` into two new columns: `GP` and `GS`
- Calculation of key statistics (totals, averages, top performers)
- Creation of a custom `impact_score` metric to proxy "most improved player"

## ✅ Completed Questions

Descriptive statistics were calculated to answer the following:

1. How many games did this team play?
2. What was the team’s average goals per game?
3. What was the team’s average assists per game?
4. Which player had the highest shot accuracy?
5. Which player committed the most turnovers?
6. Which player had the most ground balls?
7. Who scored the most goals this season?
8. Who was the most improved player (using custom metric)?

## ✏️ Prompt Engineering

A separate document (`LLM_Prompts_Task_5.docx`) outlines the natural language prompts corresponding to each of the above statistics. These prompts are designed to be used with an LLM in the next phase of this research project.

## 📌 Next Steps

In the upcoming reporting period:
- Integrate the cleaned dataset and prompts into an LLM (e.g., ChatGPT, Claude)
- Validate the model’s answers against the descriptive statistics
- Document performance, reasoning quality, and failure cases
