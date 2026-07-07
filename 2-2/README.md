# Lab 2: Designing an AI Study Coach with Structured Prompts

## Project Overview
This repository contains the progression of prompt engineering applied to design a personalized Machine Learning Study Coach for a student who struggles with focus issues and inconsistent study habits.

## Step-by-Step Evolution

### 1. The Bad Prompt (`1_Bad_Prompt.md`)
*   **Prompt:** "I struggle to stick to rigid plans. Design a machine learning study plan for me."
*   **Issue:** The AI provided a generic "Anti-Rigid ML Framework" that lacked actionable, day-by-day steps. It gave general advice rather than a structured schedule.

### 2. Structured Prompt v1 (`2_Structured_Prompt_v1.md`)
*   **Prompt Elements Used:** Role, Goal, Context, Constraints, Style, and Output Format.
*   **Improvement:** The AI successfully created a day-by-day schedule with 2-hour blocks.
*   **Instruction Drift (The Problem):** Despite the instructions, the AI scheduled a 4-hour "hyperfocus" session on Day 7 (Block 1 & Block 2). This contradicted the goal of preventing burnout for a student with focus issues.

### 3. Tuned Final Prompt v2 (`3_Tuned_Final_Prompt_v2.md`)
*   **Advanced Techniques Applied:** 
    *   **Negative Prompting:** Added explicitly: *"Do not schedule more than one 2-hour study block on any single day under any circumstances."*
    *   **Verification (Self-Check):** Added a criteria-based review asking the AI to verify if the daily limit was strictly 2 hours and to present the evaluation in a Yes/No table.
*   **Final Result:** The AI successfully respected the time constraints, completely eliminating the 4-hour blocks, and verified its own logic. The final output is highly realistic, actionable, and ready to use.

## Conclusion
This lab demonstrated that while the 6-element framework structures the output effectively, adding **Negative Prompting** and **Verification** is essential to prevent instruction drift and ensure the AI strictly adheres to critical constraints.