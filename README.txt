# Adaptive NPC Framework - Chess Testbed

Hello Sam,

This repository contains the JavaScript/HTML5 prototype referenced in our application. It serves as the controlled testbed for the adaptive AI framework.

## How to Run
No dependencies or build steps required. 
Download the repository and open `index.html` in any web browser.

## Key Components to Review

1. Bot Configuration (Left panel):
- Select different "Styles" (e.g., CAPTURE, ATTACK) and "Levels" (Unrated to Grandmaster).
- Competence is modeled via a line-misread probability based on the level, rather than artificially reducing search depth. This allows the bot to make human-like tactical errors while retaining its strategic focus.

2. Benchmark Suite (Right panel):
- Run the "Quick" benchmark to compare 7 AI configurations (Random, Scripted, Adaptive, etc.) across multiple opponents in parallel background workers.
- Review the "Effect of Adaptation" (Forest Plot). It calculates 95% confidence intervals to isolate and measure the actual contribution of each algorithm component.
- Review the "Learning Curve" to see how the bot adapts over repeated games.

3. Algorithm Architecture:
- The AI uses a 24-state meta-policy to select from 5 interpretable skills (CAPTURE, DEVELOP, SAFETY, GUARD, ATTACK) instead of selecting raw moves. 
- The system works out-of-the-box using "priors" without requiring a heavy training pipeline. Q-learning is applied optionally to refine skill selection.

Please let me know if you have any questions or require a code walk-through.