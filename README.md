# Day 3 · The Haunted Snack Bar and the Seasonal Workbook 🎃

**Sobey High School Co-Op · Business Analytics & AI · Friday, October 30, 2026**

Everything you need for today is in this repo. Two ways to get it:

## Fastest: open the notebooks straight in Colab (no upload)

| Notebook | Open it | What it is |
|---|---|---|
| **Haunted Snack Bar Notebook** | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/analyticsblackpoint-bot/sobeys-coop-day3/blob/main/notebooks/Haunted%20Snack%20Bar%20Notebook.ipynb) | Notebook 1: eight empty cells you type into with Gavin |
| **Seasonal Workbook** | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/analyticsblackpoint-bot/sobeys-coop-day3/blob/main/notebooks/Seasonal%20Workbook.ipynb) | Notebook 2: five years of seasonal data, the chart gallery, season maths, your lane |

After it opens: **File → Save a copy in Drive** so your work is yours. Run a cell with **Shift + Enter**. Stuck? **Runtime → Run all**.

Cell 8 of the Haunted Snack Bar needs `Snack Bar Data.csv`. Run this in a new cell first and it appears in the Files panel:

```python
!wget -q "https://raw.githubusercontent.com/analyticsblackpoint-bot/sobeys-coop-day3/main/data/Snack%20Bar%20Data.csv" -O "Snack Bar Data.csv"
```

(or download it below and upload it with the 📁 folder icon on the left edge of Colab; it disappears when Colab restarts).

## Or download the files

| File | For |
|---|---|
| [Day 3 Everything.zip](Day%203%20Everything.zip) | all of the below in one zip |
| [notebooks/Haunted Snack Bar Notebook.ipynb](notebooks/Haunted%20Snack%20Bar%20Notebook.ipynb) | Notebook 1 (File → Upload notebook in Colab) |
| [notebooks/Seasonal Workbook.ipynb](notebooks/Seasonal%20Workbook.ipynb) | Notebook 2 (data is built in) |
| [data/Snack Bar Data.csv](data/Snack%20Bar%20Data.csv) | the 10 most popular Halloween candies, with the snack bar's prices and stock |
| [data/Seasonal Trends Canada.csv](data/Seasonal%20Trends%20Canada.csv) | 2,096 rows: weekly Google Trends interest for eight lanes, Oct 2021 to Oct 2026 |
| [data/Halloween Spending.csv](data/Halloween%20Spending.csv) | NRF Halloween spending, 2005 to 2026 |
| [slides/Day 3 Slides.pdf](slides/Day%203%20Slides.pdf) · [.pptx](slides/Day%203%20Slides.pptx) | the slides |
| [activity/Activity Brief and Rubric.pdf](activity/Activity%20Brief%20and%20Rubric.pdf) | Pitch the season: your lane, the decision, the three slides, the rubric |
| [activity/Results Pack.pdf](activity/Results%20Pack.pdf) | every chart and table from the teacher's run, if you fall behind |
| [activity/Dashboard Skill.md](activity/Dashboard%20Skill.md) | paste into a chatbot with your small table to get an AI-built dashboard |

To download a single file on GitHub: click it, then the **Download raw file** button (the ⬇ icon at the top right of the file view).

## The activity in one line
Teams of 2 or 3, one lane each (halloween costume, candy, pumpkin spice, christmas gifts, valentines day, sunscreen, snow tires, back to school). Find the peak week, the stock-up week and the season length; decide the stock date, ad start and markdown date; back it with 2 or 3 charts (at least one box plot, heatmap, histogram or scatter) and one honest limit. Title + 3 slides, emailed by 12:10.

## Sources
- Google Trends: Canada, web search, weekly, "past 5 years", read October 29, 2026. Relative search interest, 0 to 100 per term; not counts, not sales; Canada-wide.
- NRF Halloween Data Center: the National Retail Federation's annual Halloween consumer survey by Prosper Insights & Analytics, 2005 to 2026. US consumers, US dollars; each year's figure is that September's forecast.
- Candy ranking: CandyStore.com, most popular Halloween candy 2026 (national top 10). Prices and stock counts are practice numbers.

No student data is in this repo.
