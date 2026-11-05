# Day 4 skills · how they fit together

*Sobey HS Co-Op · Day 4 · five skills for the 70-minute build. Each one is a `SKILL.md` (attach it, or copy the box) and a one-page card (paste the box). Every skill is run on the Haunted Snack Bar as the worked example, so you can see what "good" looks like before you start.*

| Build step | Skill | What you paste in | What you get back |
|---|---|---|---|
| before the build | **Prompt Lab** (a page, not a chatbot skill) | a prompt for your hat's assistant | a score out of 10, what's missing, which skill fixes it; your best prompt (8+) feeds step 3 |
| 2 Knowledge | **Fact Finder + Source Check** | your problem line + 3 questions | a fact table with links + a small table for your chart |
| 3 System prompt | **System Prompt Writer** | your assistant card + fact table | a system prompt + 3 test questions |
| 4 Page | **Bot Builder** | card + system prompt + facts + table | ONE `.html` file: your chatbot page |
| 6 Red-team | **Red-Team Tester** | your system prompt + bot answers | 5 tests, a pass/fail log, one fix each |
| 7 Pitch | **Pitch Coach** | card + chart line + test log | a 3-minute outline with timings |

## Words you'll see
- **Blank:** anything in square brackets, like `[name]`. Replace it with your words and **delete the brackets**.
- **✔ fact:** a fact whose link your red-teamer opened and checked. ✘ facts get crossed out and are never used.
- **Fallback line:** what the bot says when it doesn't know: "I'm not sure about that. Please ask [your real contact]."
- **Real contact:** a place or a role ("the Snack Bar counter", "the school office"), never a person's name.
- **Fact sheet, test log, assistant card:** pages in your Day 4 Build Workbook.
- **Team roles:** Product lead · Prompt engineer · Data & design · Red-teamer. Pick them in step 0.
- **The AI rules (from the slide):** no real people, nothing explicit, no personal data, nothing you wouldn't show your family.

## The rules in every box
1. **Don't ask me questions.** One send, one answer. Free chatbots have limits; we don't waste them.
2. **No personal information.** No names of students, no emails, no phone numbers, nothing about a real person. Use roles ("the owner", "the counter").
3. **Only what I gave you.** The chatbot uses your facts, your table, your card. It must not invent policies, prices or sources.
4. **Say "not found" instead of guessing.** A gap is fine. A made-up fact is not.

## The worked example: the Haunted Snack Bar
Our demo bot is the **Haunted Snack Bar after-Halloween clearance assistant**. It is Nov 6: the Snack Bar has leftover candy. The bot helps a shopper find a deal and helps the owner decide what to mark down first.

**Assistant card (filled in):**
- **Who it's for:** shoppers looking for cheap candy after Halloween, and the Snack Bar owner.
- **3 things it does:** (1) tells you what's on clearance and the price · (2) suggests what to buy for a budget · (3) tells the owner which candies to mark down first.
- **2 things it won't do:** (1) take payments or hold items · (2) answer anything that isn't about the Snack Bar.
- **One success measure:** a shopper finds a deal in 3 messages or fewer.
- **Real contact for the fallback:** "the Snack Bar counter".

**Data:** `Snack Bar Data.csv` (10 rows: rank, candy, type, price, stock). Rank and candy names come from CandyStore.com's projected-sales model as reported by NBC. **Prices and stock are practice numbers**, and the bot says so.

## Where the real outputs are
`snackbar_run\` (in the teacher pack) holds, for each skill, the exact prompt sent, the raw reply and a screenshot. `Snack Bar Assistant.html` is the finished page (the answer key).
