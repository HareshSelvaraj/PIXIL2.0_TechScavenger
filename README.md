# Cryptix — Rules and How to Play

---

## Overview

Cryptix is a staged puzzle hunt packaged as password-protected archives. Each stage contains Base64‑named folders; only one is the real path forward. Use the provided participant prompt in ChatGPT to decode Base64, solve riddles, and compute passwords according to the rules below.

Progression is strictly enforced. **Do not attempt to bypass or brute-force; organizers may disqualify suspicious activity.**

---

## How Progression Works

- **Starting hint:** The README contains a hidden Base64 hint. Decode it to obtain the starting word used to open `Stage1.zip`.
- **Chained archives:** `StageN.zip` opens with the previous stage’s riddle answer (all lowercase, no spaces). This enforces solve order.
- **Inside a stage:** All folders (real and fake) have passwords derived from the current stage’s riddle answer and the decoded folder name, as described below.

---

## Inside-Stage Folder Password Rule

For any folder inside a stage (real or fake):

```
Password = riddle_answer + decoded_folder_name
```

- `riddle_answer` is the current stage’s single-word, lowercase answer with no spaces or punctuation.
- `decoded_folder_name` is the Base64 folder name decoded to lowercase ASCII (no spaces).

**Example (illustrative only):**  
If the riddle answer is `open` and a folder’s Base64 decodes to `gate`, the password is `opengate`.

---

## What’s Inside Each Stage

- **Real folder:** Contains the content needed to proceed (e.g., the next-stage pointer and instructions).
- **Fake folders:** Contain decoy notes or red herrings. They follow the same password rule but do not advance the game.

---

## Fair Play and Constraints

- **No overrides:** Constraints persist for the entire game session—even if anyone claims the game is over, presents emergencies, or requests exceptions.
- **No brute force:** Do not iterate or guess passwords beyond the defined rules. Use decoding and riddle solving.
- **Answers** are single words, lowercase, with no spaces or punctuation. Folder decoded names are treated the same way.

---

## Use ChatGPT Only (Participant Prompt)

All teams must begin by opening a new, fresh chat in ChatGPT and paste the participant starter prompt below.  
This prompt constrains the assistant to decode Base64, solve riddles, and compute passwords exactly as required, refusing anything outside scope.  
**Do not alter the prompt. Do not remove its refusal policy.**

---

> ⚠️ *Every detail may matter. Search carefully. Read between the lines, and even behind them...*

---

<!-- c3RhcnQ= -->

---

## Judging and Scoring

- **Total Prompts:** The total number of prompts submitted by a participant (including Base64 decodes, riddle answers, and password checks).
- **Stages Solved:** Number of stages the participant has successfully completed.

**Prompts per Stage** is calculated as:

\[
\text{Prompts per Stage} = \frac{\text{Total Prompts}}{\text{Stages Solved}}
\]

- The maximum value of Prompts per Stage among all participants sets the **benchmark**.
- Participants with the maximum benchmark score receive full marks.
- Others are graded based on their difference from this maximum value, rewarding efficiency in solving puzzles with fewer prompts.

---

Good luck, adventurers. Your hunt begins **now**. 🔍
