# 3 skill templates from the video

These are the three real SKILL.md files used in Run 2 of the test.

## Install (2 minutes)
1. Copy the `.claude/skills/` folder into the root of your project. (Most tools also read `.agents/skills/`; copy it there if yours does.)
2. **Edit the rules to match your own project.** These are written for a FastAPI app: change the folder names (`app/schemas/`, `app/routers/`), the error format and the logger path to yours. A skill that describes someone else's project does more harm than good.
3. Start a fresh session and give the agent a task. It should open the matching skill on its own, because of the `description:` line.

## The three skills
| Folder | Use it for |
|---|---|
| `project-conventions` | where files go, naming, error format |
| `write-tests` | write pytest tests and run them before saying "done" |
| `pre-commit-check` | lint, scan for hard-coded secrets, 3-line summary |

## The test prompt and scorecard (to repeat the test yourself)
Same model, same tool, same prompt, a fresh session each run, one git branch per run from the same commit.

```
Add a POST /expenses endpoint to this app. It should accept amount, category and date, validate the input, store the expense, and include tests. Follow this project's conventions.
```

Score each run: tests pass (run pytest yourself), rules followed out of 5 (model in schemas/, router in routers/, error format, snake_case, no print()), follow-up prompts needed, time to done, cost or tokens.

## Safety
Read every line of any skill you download before installing it, especially if it comes with scripts. These three are plain text, with no scripts.

Made for the IneffebleBeast channel. Use and change freely.
