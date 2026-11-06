# System Prompt Writer: turn your assistant card into the bot's instructions

*Sobey HS Co-Op · Day 4 · Build step 3 (System prompt, 10 min). Works in any free chatbot.*

## What it's for
A **system prompt** is the instruction sheet a chatbot reads before every conversation. It says who the bot is, who it serves, what it knows, what it must refuse, and what to say when it doesn't know. This skill turns your assistant card and your ✔ facts into that sheet, plus 3 test questions so you can try it right away.

## How to use it (students)
1. Open your chatbot. Copy **everything in the box below**, from `BEGIN` to `END`.
2. Fill in the blanks (delete the square brackets): your assistant card (from step 1), your ✔ facts (from step 2) and your real contact. No names of people, no personal information.
3. Send it once. Copy the reply into a text file (Notepad is fine) named `system_prompt_v1.txt`.
4. **Test it:** open a *new* chat. Send the whole system prompt as your first message. Then ask the 3 test questions, one message each. Question 3 is off-topic on purpose: the bot must refuse it with the fallback line.
5. If a test fails, use a fix-it prompt. Save the result as `system_prompt_v2.txt`. That's the one the Bot Builder uses.

## What you paste in (with the Snack Bar example)

Start from your best Prompt Lab prompt (8 or more out of 10). Its Role, Task, Context, Format and Check lines are the blanks below, already in your words.

| Blank | What to write | Snack Bar example |
|---|---|---|
| BOT NAME | Short, friendly | Haunted Snack Bar Clearance Helper |
| WHO IT'S FOR | One line | Shoppers looking for cheap candy after Halloween, and the Snack Bar owner |
| 3 THINGS IT DOES | From your card | 1. Says what's on clearance and the price · 2. Suggests what to buy for a budget · 3. Tells the owner which candies to mark down first |
| 2 THINGS IT WON'T DO | From your card | 1. Take payments or hold items · 2. Answer anything not about the Snack Bar |
| REAL CONTACT | A place or a role, never a person's name | the Snack Bar counter |
| MY ✔ FACTS | Paste the ✔ rows of your fact table | (the 10-row Snack Bar table, with "prices and stock are practice numbers") |

```
BEGIN SYSTEM PROMPT WRITER
You are an expert at writing instructions for customer-help chatbots. Write ONE system prompt for the bot described below, then 3 test questions.

RULES (follow all of them; do not ask me any questions):
1. Reply with the system prompt in a single code block, then the 3 test questions under it. Nothing else.
2. The system prompt has exactly these 8 headings, in this order: ROLE · AUDIENCE · TASK · KNOWLEDGE · RULES · FALLBACK LINE · TONE · FORMAT.
3. KNOWLEDGE: copy my facts exactly. Do not add facts, prices, dates or policies that I did not give you. If my facts say something is a practice number, keep that label.
4. RULES must include these five, as short bullets:
   - Answer only from KNOWLEDGE.
   - Never invent a policy, price, discount or deadline.
   - If the question is off topic, or the answer is not in KNOWLEDGE, reply with the FALLBACK LINE and nothing else.
   - Never ask for anyone's name, email, phone number or address.
   - If the user types one, warn them not to share it. This warning comes before any other rule.
5. FALLBACK LINE is exactly: "I'm not sure about that. Please ask [REAL CONTACT]." with my real contact filled in.
6. TONE: friendly, short, Grade 9 reading level. FORMAT: 1 to 3 sentences per answer; a short list only when comparing items; always name the source of a number.
7. Test questions: Q1 a normal question the bot should answer well; Q2 a question that needs a number from KNOWLEDGE; Q3 an off-topic question the bot must refuse with the FALLBACK LINE. Under each question, write the answer you expect in one line.
8. Plain English. No personal information anywhere.

BOT NAME: [name]
WHO IT'S FOR: [one line]
3 THINGS IT DOES: [1. ... 2. ... 3. ...]
2 THINGS IT WON'T DO: [1. ... 2. ...]
REAL CONTACT: [a place or a role, not a person]
MY ✔ FACTS (copy exactly):
[paste the ✔ rows of your fact table, and your chart table]
END SYSTEM PROMPT WRITER
```

## What you get back
- One code block: a system prompt with the 8 headings ROLE · AUDIENCE · TASK · KNOWLEDGE · RULES · FALLBACK LINE · TONE · FORMAT.
- Three test questions with the expected answer under each.

## How to check it
- [ ] All 8 headings are there, in order.
- [ ] KNOWLEDGE has only your facts. Nothing new appeared (read it line by line).
- [ ] The FALLBACK LINE names your real contact, not a person.
- [ ] In a **new chat**, Q1 and Q2 get good answers, and Q3 gets the fallback line and nothing else.
- [ ] Ask one more thing that isn't in KNOWLEDGE (for example, "Is there a student discount?"). It must say the fallback line, not "yes".

## Fix-it prompts (send one line)
- "The bot answered an off-topic question. Make the off-topic bullet in RULES stronger: for anything not in KNOWLEDGE, reply with the FALLBACK LINE only. Show the full prompt again."
- "KNOWLEDGE has a fact I didn't give you: [quote it]. Remove it and show the full prompt again."
- "Answers are too long. Change FORMAT to 1 to 2 sentences."

## Why these rules (for the instructor)
- **8 fixed headings:** the same shape in every team's prompt makes the dashboard's editable system prompt, the Bot Builder and the Red-Team Tester all line up.
- **"Copy my facts exactly":** the system prompt is the bot's whole world. The context-engineering slide says this out loud: give the model the right tokens and nothing else.
- **Fallback line is fixed text:** the Bot Builder tests for it, and the Air Canada slide explains why a bot that says "I'm not sure" is worth more than one that guesses.
- **Test in a new chat:** the old chat already knows the card; a fresh one is the real test. Q3 is the Prompt Lab trap again (the policy that doesn't exist).
- **Snack Bar run (Nov 5):** `snackbar_run\03_system_prompt_*`; the 3 test answers from a fresh session are saved with it.
