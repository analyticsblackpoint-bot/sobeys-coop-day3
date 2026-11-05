# Pitch Coach: your 3-minute pitch, timed

*Sobey HS Co-Op · Day 4 · Build step 7 (Pitch + submit, 9 min). Works in any free chatbot. Output: a 3-minute outline with timings.*

## What it's for
You have **3 minutes** and a live bot. This skill writes your outline in the order the judges expect: problem → insight + chart → live bot demo → red-team moment → risk + safeguard → business impact. Each part gets a time and one or two lines to say. Then you practise it once, out loud, with a timer.

## How to use it (students)
1. Open your chatbot. Copy **everything in the box below**, from `BEGIN` to `END`.
2. Fill in the blanks (delete the square brackets) from your card, your chart line and your test log. No names of people, no personal information.
3. Send it once. Copy the outline into the pitch page of your Day 4 Build Workbook.
4. Decide who says which part (every team member speaks). Practise once with a timer. Cut words until it fits in 3:00.
5. Email your `.html` and a photo of your card and test log to the address on the board, before the deadline on the slide. Then pitch.

## What you paste in (with the Snack Bar example)
| Blank | What to write | Snack Bar example |
|---|---|---|
| BOT NAME | | Haunted Snack Bar Clearance Helper |
| PROBLEM LINE | Our bot helps ___ do ___ so that ___ | Our bot helps shoppers find after-Halloween candy deals so that leftover stock gets sold. |
| WHO IT'S FOR | | Shoppers after Halloween, and the Snack Bar owner |
| MY CHART LINE | The "what it means" sentence | Candy Corn has the most stock left (60), so it goes on clearance first. Stock is a practice number. |
| MY RED-TEAM RESULT | Score and the one fix | 5/5 on the five tests; an extra probe, "Is there a student discount?", got the clearance list because "discount" matched a topic; we added "student discount" to the REFUSE WORDS; re-run PASS. |
| MY BIGGEST RISK | One line | The bot could state a price that's wrong or out of date. |
| MY SAFEGUARD | One line | Every answer shows its source, and the page says the numbers are practice numbers. |
| MY BUSINESS IMPACT | One line, honest | Clearing leftover candy a week faster frees shelf space and cash for the next season. |
| TEAM SIZE | 2 or 3 | 3 |

```
BEGIN PITCH COACH
You are a pitch coach for high-school teams. Write a 3-minute pitch outline for the chatbot project below.

RULES (follow all of them; do not ask me any questions):
1. Reply with one table and one closing line. Nothing else.
2. The table has these 6 rows in this exact order: 1 Problem · 2 Insight + chart · 3 Live bot demo · 4 Red-team moment · 5 Risk + safeguard + who's responsible · 6 Business impact. Columns: Part | Seconds | Say this (1 or 2 short sentences) | Show this | Who.
3. The seconds must add up to 180. Suggested: 25 · 30 · 50 · 25 · 25 · 25.
4. "Say this" uses my words and my numbers only. Do not add facts, numbers or claims I did not give you. Keep my honest limits in (for example "practice numbers" or "we tested 5 cases").
5. "Live bot demo" must list the exact 2 questions to type into the bot: one normal question, then the made-up-policy question that the bot refuses.
6. "Risk + safeguard + who's responsible" says the risk in one line, the safeguard in one line, and who is responsible for the bot's answers (the team, not the AI).
7. "Who" spreads the parts across my team size so everyone speaks.
8. The closing line is one sentence the team says last, under 15 words.
9. Plain English, Grade 9 level. No names of people, no personal information.

BOT NAME: [name]
PROBLEM LINE: [Our bot helps ___ do ___ so that ___.]
WHO IT'S FOR: [one line]
MY CHART LINE: [the "what it means" sentence]
MY RED-TEAM RESULT: [score, the test that failed, the fix]
MY BIGGEST RISK: [one line]
MY SAFEGUARD: [one line]
MY BUSINESS IMPACT: [one line]
TEAM SIZE: [2 or 3]
END PITCH COACH
```

## What you get back
A 6-row table (Part · Seconds · Say this · Show this · Who) that adds up to 180 seconds, and one closing line.

## How to check it
- [ ] The 6 parts are in the right order and the seconds add up to 180.
- [ ] Every number in "Say this" is one you gave it.
- [ ] The demo lists 2 exact questions, and the second one is the made-up policy your bot refuses.
- [ ] Risk, safeguard and "who is responsible" are all there.
- [ ] Everyone on the team has at least one part.

## Fix-it prompts (send one line)
- "Cut every 'Say this' to one sentence. Keep the seconds the same."
- "Make part 4 about T3 only: the made-up policy test and our fix."
- "Give part 3 to the Prompt engineer and part 4 to the Red-teamer." (the team roles from step 0)

## Why these rules (for the instructor)
- **Order matches the program's Day 10 list:** problem, insight, visualization, AI/data solution, business impact, with the red-team moment and the responsibility line added for the responsible-AI rubric row.
- **180 seconds, fixed:** 8 teams × (3 + 1) minutes is the whole pitch block.
- **"My words and numbers only":** no new claims appear on stage; what they say is what their page shows.
- **Two demo questions, the second a refusal:** the live demo shows both the help and the safeguard in under a minute.
- **Snack Bar run (Nov 5):** `snackbar_run\07_pitch_coach_*`; the outline is on the Pitch Coach slide.
