**read README.md before or after**


This is the **workflow I personally use**, but I can’t reveal company code, so I’m sharing the methodology only.  
If you find it useful, please ⭐️ Star the repo!

## Limitations
- When VS Code + GitHub Copilot can use **only** the LLMs approved by your company
- Or when you want a lightweight setup for a personal project

## How to use
1. **Clone** the repository or copy just `prompt.md`.  
2. **Recommended models**  
   - Simple questions → GPT-4.1 or higher  
   - Complex, context-heavy tasks → Claude 4 or higher (premium)
3. Initial setup  
   - Put all relevant code in the `repos/` folder.  
   - Instruct the agent to read `prompt.md` and analyze the codebase.  
   - Make it identify company-specific terms, acronyms, and coding patterns for its answers.  
   - Add design docs and team docs to `raw/`, then run the **update knowledge** command to populate `knowledge/`.

### Optional features
- **dailylog**  
  - Run this before you clock out; the day’s Q&A and work summary is saved in `/personal/dailylog/` by date.  
  - Handy for performance reviews and picking up work quickly the next day.
- **Automatic PR descriptions**  
  - Place several well-written past PRs in `raw/`; instruct the agent to use them as references.
- **Task management**  
  1. Enter a task and the agent creates a step-by-step plan.  
  2. It saves the result to `personal/jira/JIRA-<task-number>.md`.  
  3. Subsequent questions automatically reference this file, keeping context consistent.
