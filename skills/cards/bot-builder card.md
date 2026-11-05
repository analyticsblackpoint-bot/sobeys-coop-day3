# Bot Builder card
*Sobey HS Co-Op · Day 4 · Build step 4 · Page · 15 min · paste into any free chatbot*

**How to use it:** 1. Copy everything in the box, BEGIN to END. 2. Fill in the blanks: name, emoji, tagline, team + date, contact, colours, system prompt v2, ✔ facts, chart table. **No names, no personal information.** 3. Send it once. 4. Copy the whole code block into a new text file. Save as [bot name].html. Open it in a browser.

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

**Check it (3 ticks):**
- [ ] Opens offline. Every starter button answers, with a source under it.
- [ ] Off-topic question → fallback line. test@example.com → privacy warning.
- [ ] Chart numbers exact; drawer opens; footer says "Prototype made with AI, checked by us. It can be wrong."

*The full skill (with the Snack Bar example, fix-it prompts and why the rules exist): `skills\bot-builder\SKILL.md`.*
