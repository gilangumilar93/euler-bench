# Euler Bench

A Project Euler trainer. You solve each problem yourself. The app checks your answer and then gives you a professor-style review that tells you where you went wrong, teaches the missing idea, and never hands you the answer.

## Files

| File | What it is |
|---|---|
| `euler-bench-app.html` | The whole app in one file. Open it in Chrome, Edge or Firefox. |
| `euler-bench-README.md` | This guide. |

## Setup

1. Double-click `euler-bench-app.html` to open it in your browser.
2. Open **Claude connection** at the top and paste your Anthropic API key (from console.anthropic.com).
3. Pick a model. Sonnet 5.5 is the default and is good enough for reviews. Opus 5.5 is sharper but costs more.

Your key is stored only in your browser's local storage. It is sent only to `api.anthropic.com`.

If you open the app on claude.ai, it uses Claude there and does not need a key.

Without a key, the app still tells you whether your answer is right or wrong. You just don't get the written review.

## How a round works

1. **Pick a problem** from the list on the left. On a phone, use the dropdown.
2. **Fill in your work:**
   - **Your reasoning:** your plan in plain words.
   - **Your code or working:** optional, but the review is much better with it. The Tab key indents.
   - **Language:** what you wrote it in.
   - **Your answer:** the number you got.
3. **Submit for review.** Your answer is checked straight away, and the review appears below on its own. There's no extra button to press.

## What the professor gives you

| Section | If you're wrong | If you're right |
|---|---|---|
| **Verdict** | Wrong answer, in a sentence or two | Correct, confirmed |
| **Where your path breaks** | Quotes the exact line or assumption that's wrong and says why | The weak spots in your method: how fast it is and what breaks if the input is 1000× bigger |
| **Quick lesson** | The one concept you're missing, shown on small numbers | A better or more elegant approach |
| **Your next move** | One concrete next step | One concrete next step |

**Rules the professor follows:**

- It never gives the final number and never writes a full solution.
- Code examples are short (about 6 lines at most) and only illustrate the concept.
- It points out bugs even when they didn't change your answer.
- If you submit an answer with no reasoning, it asks you to show your work.

## Problems included

Problems 1–30, minus 8, 11, 13, 18 and 22 (those need large data grids or files). That leaves 25 problems:

1, 2, 3, 4, 5, 6, 7, 9, 10, 12, 14, 15, 16, 17, 19, 20, 21, 23, 24, 25, 26, 27, 28, 29, 30

**Answer checking:** answers are stored as scrambled codes (SHA-256 hashes), so you can't find them by reading the page source. Commas and spaces in your answer are ignored, so `233,168` and `233168` both work.

## Progress

These are saved in your browser:

- Solved problems (green dot)
- Problems you've tried but not solved (red ring)
- Your drafts
- Every answer you tried, with ✓ / ✗
- The last review for each problem

**Your progress is tied to one browser.** It won't follow you to a different browser or computer. If you clear your site data, your progress resets.

## Tips from the professor

- Solve the small example in the problem first. If your method can't produce 23 for Problem 1, it won't produce the real answer.
- Write the reasoning before the code. Most wrong answers come from a wrong idea, not a typo.
- Watch "below" vs "not exceeding", and inclusive vs exclusive ranges. That's where off-by-one errors hide.
- After you solve a problem, read the efficiency notes. Later problems punish brute force.
