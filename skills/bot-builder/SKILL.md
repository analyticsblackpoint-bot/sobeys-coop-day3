# Bot Builder: one HTML file, your chatbot on a page

*Sobey HS Co-Op · Day 4 · Build step 4 (Page, 15 min). Works in any free chatbot. Output: `[your bot name].html`.*

## What it's for
This skill turns your assistant card, system prompt, ✔ facts and chart table into **one HTML file** that works offline. The page has a chat window with starter buttons, a "brain" of 8 to 10 topics, a safe fallback, a privacy warning, a chart, and a panel that shows how the bot works. No keys, no internet, no library. Open the file in any browser and it runs.

## How to use it (students)
1. Open your chatbot. Copy **everything in the box below**, from `BEGIN` to `END`.
2. Fill in the blanks (delete the square brackets). Paste your system prompt v2, your ✔ facts and your chart table where it says. No names of people, no personal information.
3. Send it once. The reply is one long code block. Copy **all of it** (from `<!DOCTYPE html>` to `</html>`) into a new text file. Save it as `[your bot name].html`. **Windows tip:** in Notepad, set "Save as type" to **All files** so it doesn't become `.html.txt`. If the reply stopped before `</html>`, send the first fix-it prompt.
4. Open the file in a browser (double-click it). Click every starter button. Type an off-topic question. Type a fake email like `test@example.com`. Check the list below.
5. Anything wrong? Use a fix-it prompt, then save the new file over the old one. Add your logo in the Brand step (build step 5).

## What you paste in (with the Snack Bar example)
| Blank | What to write | Snack Bar example |
|---|---|---|
| BOT NAME | Same as the system prompt | Haunted Snack Bar Clearance Helper |
| EMOJI | One emoji as a stand-in logo | 🎃 |
| TAGLINE | Under 8 words | Leftover candy, lower prices, zero guessing. |
| WHO IT'S FOR | One line | Shoppers after Halloween, and the Snack Bar owner |
| TEAM NAME + DATE | A team name (no student names) and the date | Team Demo · Nov 6, 2026 |
| REAL CONTACT | Same as the system prompt | the Snack Bar counter |
| COLOURS | Two colours, as names or hex codes | dark purple, gold (or #612141, #EEDC00) |
| REFUSE WORDS | Words about offers your facts do NOT cover | coupon, refund, 2-for-1, free, guarantee, promise, policy |
| MY SYSTEM PROMPT | Paste v2 | (the 8-heading prompt from step 3) |
| MY ✔ FACTS | Paste the ✔ rows | (the 10-row Snack Bar table, "practice numbers") |
| MY CHART TABLE | 3 to 8 rows: label, number | Candy, stock: M&M's 48 · Sour Patch Kids 36 · Skittles 40 · Reese's Cups 30 · Nerds Gummy Clusters 18 · Starburst 24 · Candy Corn 60 |
| WHAT IT MEANS | One true sentence about the chart | Candy Corn has the most stock left, so it goes on clearance first. (Stock is a practice number.) |
| SOURCE LINE | Where the table comes from | Snack Bar Data.csv (rank via CandyStore.com / NBC; prices and stock are practice numbers) |

```
BEGIN BOT BUILDER
You are a careful front-end developer. Build ONE self-contained HTML page: a rule-based chatbot for the assistant described below.

RULES (follow all of them; do not ask me any questions):
1. Reply with ONLY one complete HTML file in a single code block, from <!DOCTYPE html> to </html>. No words before or after it. All CSS and JavaScript go inside the file. No external files, no libraries, no fonts, no images. The page must work offline from a local file. The only links allowed are the source links from my facts, shown under answers.
2. HEADER: the bot name, my emoji as the logo, the tagline, and "For: " + who it's for.
3. CHAT: a scrolling box of chat bubbles (user on the right, bot on the left), a text input, a Send button, and Enter to send. Show three animated "typing" dots for about 600 ms before each bot reply.
4. STARTER BUTTONS: 3 or 4 buttons above the input with the most useful questions. Clicking one sends that question.
5. BRAIN: a JavaScript array of 8 to 10 topics. Each topic has three fields: keywords (lowercase words or phrases), answer (1 to 3 sentences, using ONLY my facts), and source (a link or the source line). To reply, count keyword hits in the user's message and pick the topic with the most hits. Show the source under the answer in small text. Copy every number exactly from my facts. Never add facts, prices, discounts or policies I did not give you.
6. FALLBACK: reply exactly "I'm not sure about that. Please ask [REAL CONTACT]." when (a) no topic has a keyword hit, or (b) the message contains any of my REFUSE WORDS. Rule (b) wins even if a topic matched. Never guess, never invent a policy.
7. PRIVACY WARNING: check this first, before the brain. If the user's message contains an email address or a phone number (match each with a pattern: an email has @ and a dot; a phone number has 7 or more digits with optional spaces, dashes or brackets), reply ONLY: "Please don't share personal information here, like emails or phone numbers. I don't store anything, but it's safer not to." Do not answer the question.
8. INSIGHT PANEL beside or below the chat: a heading "What the data says", ONE bar chart drawn as inline SVG from my chart table (bars start at zero, each bar labelled with its name and its number, no 3D), then the "what it means" line, then "Source: " + my source line.
9. DRAWER: a button "How this bot works" that opens a panel showing (a) the full system prompt as plain text in a box, (b) the rules and the refuse words as a bulleted list, (c) the sources as a list. The panel starts closed.
10. FOOTER: exactly this text on one line: "Prototype made with AI, checked by us. It can be wrong." then my team name and date on the next line.
11. STYLE: clean and readable on a laptop and a phone; main colour and accent colour from my colours; body text at least 16px; the bot name as an <h1>. Keep the file under 300 lines.
12. No names of people, no personal information, no tracking, no forms other than the chat input, no cookies, nothing saved to the browser (the chat can stay on screen).

BOT NAME: [name]
EMOJI: [one emoji]
TAGLINE: [under 8 words]
WHO IT'S FOR: [one line]
TEAM NAME + DATE: [team name, no student names · date]
REAL CONTACT: [a place or a role, not a person]
COLOURS: [main colour], [accent colour]
REFUSE WORDS: [words about offers my facts do not cover, for example coupon, refund, 2-for-1]
MY SYSTEM PROMPT:
[paste system_prompt_v2]
MY ✔ FACTS (copy numbers exactly):
[paste the ✔ rows]
MY CHART TABLE (label, number; 3 to 8 rows):
[paste]
WHAT IT MEANS: [one true sentence]
SOURCE LINE: [where the table comes from]
END BOT BUILDER
```

## What you get back
One code block: a complete HTML file. Save it as `[your bot name].html` and open it in a browser.

## How to check it (click test)
- [ ] The page opens from the file with no internet. Header shows the name, emoji, tagline and "For:".
- [ ] Every starter button gives a real answer with a source line under it.
- [ ] Type something off-topic ("What's the weather?"). You get the fallback line with your real contact, nothing else.
- [ ] Type `test@example.com`. You get the privacy warning, not an answer.
- [ ] The chart shows your numbers exactly; the "what it means" line and the source are under it.
- [ ] "How this bot works" opens and shows the system prompt, the rules and the sources.
- [ ] Footer says "Prototype made with AI, checked by us. It can be wrong." plus your team name and date.

## Fix-it prompts (send one line, then save the whole new file)
- "The file was cut off. Continue from exactly where you stopped, starting with the last line you wrote, until </html>."
- "The bot answered a made-up offer. Add these REFUSE WORDS: [words]. Any message with one of them gets the exact fallback line. Show the full file again."
- "The chart numbers are wrong. Use exactly these rows: [paste]. Show the full file again."
- "Make the page work on a phone: one column, chat first, chart below. Show the full file again."
- "Add a starter button for '[question]'. Show the full file again."

## Why these rules (for the instructor)
- **Rule-based brain, not a live model:** no keys, no accounts, no cost, no internet, and every answer is checkable against the facts. It also makes the point that a bot is only as good as its context.
- **Inline SVG chart, no library:** Gavin's decision Nov 5. Works offline in class; nothing to download; nothing to block.
- **The fallback and the privacy warning are exact strings:** `test_day4_botbuilder.py` greps for them, and the Red-Team Tester expects them.
- **REFUSE WORDS:** a keyword bot will happily answer "Is there a 2-for-1 on Candy Corn?" with the Candy Corn stock. The refuse list is the cheap fix for the Air Canada case, and it's what the red-team fix usually touches.
- **Drawer with the system prompt:** the "anatomy of an AI product" slide made visible. Judges can open it during the pitch.
- **Under 300 lines:** fits in one reply on a free plan; fix-it prompts always ask for the whole file so nothing is half-patched.
- **Snack Bar run (Nov 5):** `snackbar_run\04_bot_builder_*` and `Snack Bar Assistant.html` (answer key). The test passed and the click test is on the Bot Builder slide.
