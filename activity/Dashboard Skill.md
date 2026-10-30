# Dashboard skill: one-file HTML dashboard from a small table

*Sobey HS Co-Op · Day 3 · for teams who want an AI-built dashboard for "Pitch the season". Works in any free chatbot.*

## How to use it (students)
1. Open your chatbot (any free one; follow the Day 2 AI rules).
2. Copy **everything in the box below**, from `BEGIN` to `END`, into the chat.
3. Fill in the three blanks inside it: your lane and decision, your source line, and **one** small table from step 6f of the Seasonal Workbook (the season table or the month table; never the raw data). No names, no personal information.
4. Send it once. Copy the HTML the chatbot gives you into a new text file, save it as `dashboard.html`, and open it in your browser.
5. **Check it before you send it**: every number on the dashboard must match your table; the title must be true; the source line, the limit and "Made with AI, checked by us" must be there. If something is wrong, tell the chatbot exactly what to fix.
6. Email the `.html` file to Gavin by 12:10 (as an attachment).

```
BEGIN DASHBOARD SKILL
You are a careful data-visualization developer. Build ONE self-contained HTML dashboard from the table below.

RULES (follow all of them, do not ask me any questions):
1. Reply with ONLY one complete HTML file in a single code block. No explanation before or after it.
2. Load Plotly.js from this exact URL and nothing else: https://cdn.plot.ly/plotly-2.35.2.min.js
   All other CSS and JavaScript go inside the file. No other libraries, fonts, images or links.
3. Make 2 or 3 charts. At least ONE must be a box plot, a histogram, a scatter plot or a heatmap. No pie charts.
   A month table (mean, min, max per month) suits a bar of the means with min-max error bars plus a heatmap of one row;
   a season table (one row per year) suits a scatter of year vs season_weeks and a bar of peak per year.
4. Use ONLY the numbers in my table. Never invent, estimate, round differently or fill in missing values.
   An empty cell stays missing; leave it out and say how many were left out under that chart.
   Rows where full_year is False are partial years: show them in grey and say so.
5. Put the data in the file as a JavaScript array copied exactly from my table.
6. Page title (h1): one sentence that states the main finding and names the decision (stock date, ad start, markdown date).
   Under it, my lane and store in smaller text.
7. Every chart: a title that states what it shows, labelled axes with units, and a short "What this shows" line under it
   that is true for the data.
8. Footer on the page: "Source: " + my source line, then on a new line my limit sentence, then on a new line:
   "Made with AI, checked by us."
9. Colours: page background white, headings #612141, accent #9D2235, text #222222. Use my lane's colour for its series:
   halloween costume #D55E00, candy #9D2235, pumpkin spice #B8790F, christmas gifts #2E8B57, valentines day #CC79A7,
   sunscreen #56B4E9, snow tires #0072B2, back to school #7B5EA7. Bars and axes start at zero.
10. Layout: charts stacked in one column, each about 420px tall, readable on a laptop. Plotly config: responsive true,
    displaylogo false. Keep the file short (under 250 lines).
11. No names, no personal information, no tracking, no forms, no external links except the Plotly URL above.

MY LANE, STORE AND DECISION: [lane · store · stock date, ad start, markdown date]
MY SOURCE LINE: Google Trends, Canada, web search, weekly, Oct 2021 to Oct 2026 (relative interest, 0 to 100 per lane)
MY LIMIT: [one sentence, for example: relative search interest, not sales; Canada-wide, not Nova Scotia]
MY TABLE (CSV, 30 rows or fewer):
[paste the season table or the month table from step 6f here]
END DASHBOARD SKILL
```

## Why these rules (for Gavin)
- **Small table only (≤ 30 rows):** saves tokens on free chatbots and keeps raw data out of the chat. Step 6f writes exactly these two tables.
- **No questions, one file:** one send, one answer; no back-and-forth that eats a free plan's limit.
- **Plotly.js from a pinned CDN URL:** supports box plots, histograms, scatter and heatmaps with no install; one pinned version so every team's file behaves the same. The file needs an internet connection the first time it opens (to load Plotly).
- **"Use only the numbers in my table" + data copied into the file:** makes every number checkable against the notebook.
- **Partial years in grey:** 2021 and 2026 are not full years in the data; the dashboard must say so, like the notebook does.
- **Footer with the limit and "Made with AI, checked by us":** matches rubric rows 2 and 4.
- Tested once on Oct 29 with the halloween costume season table from step 6f: one HTML file back, two charts (scatter + bar), partial years in grey, all six rows copied exactly, footer complete (`test_day3_dashboard_skill.py`: PASS). The result is `Dashboard Test Output.html` in the teacher folder; open it once in a browser (needs internet for Plotly).
