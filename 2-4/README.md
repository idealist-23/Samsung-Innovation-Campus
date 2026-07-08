# Lab 4: General Prompt vs. Step-by-Step Instructions

## Project Overview
This repository contains the results of an A/B test designed to compare the AI's performance when handling complex mathematical and logical constraints. It evaluates a single "General Prompt" (Prompt A) against logically sequenced "Step-by-Step Instructions" (Prompt B).

## Lab 4-4: Performance Comparison (The Control Gap)
* **The biggest difference was** in the AI's ability to handle mathematical calculations and constraints simultaneously. 
* While **Prompt A (General Prompt)** resulted in an information overload where the AI struggled to calculate the exact subject percentages and distribute them smoothly without violating the 4-hour daily limit, **Prompt B (Step-by-Step Prompt)** provided a highly reliable and flawless schedule. 
* Prompt B succeeded because it forced the AI to calculate the exact required hours first (Step 1) before attempting to build the schedule across the 5 days (Step 2), effectively eliminating reasoning errors.

## Lab 4-5: Execution Rule (My Golden Rule)
Based on this A/B testing and the observed control gap, I have established the following rule for my future AI workflows:
* **I will use Prompt A (General Prompt) when** the task is simple, flexible, or for quick brainstorming where strict mathematical accuracy and formatting do not matter.
* **I will use Prompt B (Step-by-Step Prompt) when** the task requires multi-stage logic, exact data calculations, or professional-grade constraints. By breaking the task into milestones, I can ensure my AI outcomes are always reliable and free of hallucinated logic.
