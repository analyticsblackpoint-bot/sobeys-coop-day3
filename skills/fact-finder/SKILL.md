# Fact Finder + Source Check: facts with links, or "not found"

*Sobey HS Co-Op · Day 4 · Build step 2 (Knowledge, 10 min). Works in any free chatbot.*

## What it's for
Your chatbot needs real facts to answer with. This skill asks the AI for 5 to 8 facts about your problem, **each with a link**, plus one small table you can chart. If the AI can't find a fact, it must write **"not found"** instead of making one up. Then your red-teamer opens every link and marks it ✔ or ✘.

## How to use it (students)
1. Open your chatbot (any free one; follow the AI rules on the slide).
2. Copy **everything in the box below**, from `BEGIN` to `END`, into the chat.
3. Fill in the three blanks (delete the square brackets): your problem line, your 3 questions, and your table topic. No names of people, no personal information.
4. Send it once. Copy the reply into the fact sheet page of your workbook.
5. **Red-teamer: open every link.** Mark ✔ if the page says what the table says. Mark ✘ if the link is dead, or the page says something different. Cross out every ✘ fact. Keep the ✔ facts only.

## What you paste in (with the Snack Bar example)
| Blank | What to write | Snack Bar example |
|---|---|---|
| MY PROBLEM LINE | "Our bot helps ___ do ___ so that ___." (a kind of person, not a named person) | Our bot helps shoppers find after-Halloween candy deals at the Haunted Snack Bar so that leftover stock gets sold. |
| MY 3 QUESTIONS | Three things your bot must know, as questions | 1. Which Halloween candies sell the most in North America? 2. How much do people spend on Halloween candy each year? 3. When do stores usually mark down Halloween candy, and by how much? |
| MY TABLE TOPIC | One thing to chart, 3 to 8 rows | Top Halloween candies by rank (name and rank) |

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

## What you get back
- **PART A:** a table, 5 to 8 rows, with a link and a confidence rating on every row. Some rows may say "not found". That's fine.
- **PART B:** one tiny table (label, number) with a link under it. This is what your page's chart will show.

## How to check it (red-teamer)
- [ ] Every row has a link, or says "not found". No row has a number without a link.
- [ ] You opened **every** link. Each one loads, and you found the same number on the page (use Ctrl+F to search the page for the number). Mark ✔ or ✘ on the fact sheet.
- [ ] At least 5 facts are ✔. If not, send the second fix-it prompt below.
- [ ] The PART B numbers match a ✔ fact exactly.
- [ ] No person's name anywhere in the reply.

## Fix-it prompts (send one line)
- "Row 3's link does not say that. Replace row 3 with a fact that has a working link, or write not found."
- "I need 2 more facts about [topic] with links. Same table format. Don't ask me questions."
- "Make PART B a table of [label] vs [number] from row [#] only."

## Why these rules (for the instructor)
- **"Not found" beats guessing:** the whole lesson of Air Canada and Deloitte. A visible gap teaches more than a hidden fabrication.
- **Confidence column + "if you cannot browse":** many free chatbots have no live search. The column makes the model say how sure it is, and the red-teamer's link check is the real test.
- **Two parts, fixed columns:** the fact sheet and the chart table go straight into the Bot Builder prompt with no reformatting.
- **Red-teamer opens every link:** the human check is the point. It is also the "source check" half of the skill name.
- **Snack Bar run (Nov 5):** see `snackbar_run\02_fact_finder_*`. The reply and the link checks are in the folder; the result appears on the Fact Finder slide.
