🧠📐 Math Tutor with Simulated BCI Feedback

An adaptive AI-powered math practice tool using OpenRouter API and simulated Brain-Computer Interface (BCI) engagement levels.
📌 Overview

This project is an interactive math tutor powered by a large language model (LLM) via OpenRouter.
It simulates a full adaptive learning workflow where the system:

    Receives a math topic from the user.

    Generates a first-level question using LLM.

    Takes user’s answer and a simulated engagement/focus level (1–5).

    Adapts the next problem’s difficulty based on:

        The correctness of the user’s previous answer.

        Their focus level (simulating BCI team input).

Each response includes structured feedback and a new math problem:

[Feedback]: (Your performance review)
[Next Problem]: (A new question adapted to your focus)

🧠 Simulated BCI Integration

To simulate BCI-driven personalization, the user manually inputs a focus level from 1 (low) to 5 (high). The LLM uses this along with the previous problem and answer to dynamically adjust the next task:

    Low focus → easier problem

    Medium focus → same level

    High focus → harder problem

This simulates real-time cognitive feedback as if it were received from a brain-computer interface system.
🚀 Quick Start
1. Clone the repository

git clone https://github.com/your-username/math-bci-tutor.git
cd math-bci-tutor

2. Install dependencies

pip install openai python-dotenv

3. Add your API Key

    Copy .env.example → .env

    Add your OpenRouter API key to .env:

OPENROUTER_API_KEY=sk-xxxxxxxxxxxxxxxxxxxx

4. Run the app

python math_tutor.py

💡 Example Interaction

Enter the math topic you want to practice: Algebra

[Feedback]: First question. No feedback needed yet.
[Next Problem]: Solve for x: 2x + 3 = 9

Your Answer: x = 3
Enter focus level (1-5): 4

[Feedback]: Correct! Your answer shows good understanding.
[Next Problem]: Now try this: Solve for x: 3x - 5 = 16
