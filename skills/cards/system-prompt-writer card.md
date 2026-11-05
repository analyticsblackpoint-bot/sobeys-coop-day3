# System Prompt Writer card
*Sobey HS Co-Op · Day 4 · Build step 3 · System prompt · 10 min · paste into any free chatbot*

**How to use it:** 1. Copy everything in the box, BEGIN to END. 2. Fill in the blanks: your assistant card, your real contact, your ✔ facts. **No names, no personal information.** 3. Send it once. 4. Save the reply as system_prompt_v1.txt. Test the 3 questions in a NEW chat; fix once; save v2.

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

**Check it (3 ticks):**
- [ ] All 8 headings, in order. KNOWLEDGE has only your facts.
- [ ] In a new chat: Q1 and Q2 answered well; Q3 gets the fallback line only.
- [ ] Ask about a discount that doesn't exist. It must say the fallback line, not "yes".

*The full skill (with the Snack Bar example, fix-it prompts and why the rules exist): `skills\system-prompt-writer\SKILL.md`.*
