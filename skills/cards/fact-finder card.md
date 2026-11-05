# Fact Finder + Source Check card
*Sobey HS Co-Op · Day 4 · Build step 2 · Knowledge · 10 min · paste into any free chatbot*

**How to use it:** 1. Copy everything in the box, BEGIN to END. 2. Fill in the blanks: your problem line, your 3 questions, your table topic. **No names, no personal information.** 3. Send it once. 4. Paste the reply into your fact sheet.

```
BEGIN FACT FINDER
You are a careful research assistant. Find facts for a student chatbot project.

RULES (follow all of them; do not ask me any questions):
1. Reply with exactly two parts: PART A, a fact table; PART B, a chart table. Nothing else, except the one line allowed in rule 5.
2. PART A has 5 to 8 rows with these columns: # | Fact (one sentence, with the number) | Organization (who published it) | Date | Link | Confidence (High / Medium / Low). At least 5 rows must be real facts with links.
3. Every fact needs a real link to the page that says it. No link? Then write "not found" in the Fact column and leave the rest of that row blank. Never invent a link, a number, a date or an organization.
4. Prefer official or well-known sources: government statistics, big news outlets, the company's own site. Give the date the page was published.
5. Confidence says how sure you are that the link shows this exact number. High = you have seen the page. Medium = widely reported. Low = unsure. If you cannot browse the web, mark everything Medium or Low, and write one line above the table that says so.
6. PART B is one small table with 3 to 8 rows and 2 columns (label, number), copied from one of the facts in PART A, with its link under it. Use the exact numbers from that fact. Do not estimate or round.
7. Use plain English a Grade 9 student can read. Short sentences.
8. No names of people, no personal information, no emails, no phone numbers. If a source quotes a person, leave the person out.

MY PROBLEM LINE: [Our bot helps ___ do ___ so that ___.]
MY 3 QUESTIONS:
1. [question]
2. [question]
3. [question]
MY TABLE TOPIC: [one thing to chart, 3 to 8 rows]
END FACT FINDER
```

**Check it (3 ticks):**
- [ ] Every row has a link or says "not found". No number without a link.
- [ ] Red-teamer opened EVERY link and marked ✔ or ✘. At least 5 are ✔.
- [ ] PART B numbers match a ✔ fact exactly. No person's name anywhere.

*The full skill (with the Snack Bar example, fix-it prompts and why the rules exist): `skills\fact-finder\SKILL.md`.*
