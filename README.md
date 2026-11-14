# SBM Assignment 2 – Expansions as a Signal of Board Game Success

Analysis code for the group research report of the course *Strategy and Business Models* (JADS).

## Research question

> How is receiving expansions (and the number of expansions), as a signal that a publisher
> considered a game successful enough to build on, related to the installed base of the base
> game, and how does this relationship differ across game categories and mechanics?

The data are a single snapshot, so results are interpreted as associations, not causal effects.

## Data

Source: [TidyTuesday 2022-01-25 – Board Games](https://github.com/rfordatascience/tidytuesday/tree/main/data/2022/2022-01-25),
originally scraped from [BoardGameGeek](https://boardgamegeek.com/).

Place the two files in `data/raw/`:

| File | Contents |
|---|---|
| `details.csv` | Per game: categories, mechanics, family, expansions, implementations, designers, publishers, and the number of users who own, trade, want or wish for it |
| `ratings.csv` | Per game: rank, average rating, Bayes average, number of ratings, year |

## Project structure

```
data/raw/          raw TidyTuesday files
data/processed/    analysis dataset, one row per game (created by notebook 01)
notebooks/         01_data, 02_descriptives, 03_models (run in this order)
output/figures/    exported figures (PNG)
output/tables/     exported tables (CSV)
```

| Notebook | What it does | Output |
|---|---|---|
| `01_data` | Merge, clean, select the sample (1950–2019) and build all variables | `games_clean.csv`, `sample_filters.csv` |
| `02_descriptives` | Summary statistics, correlations, raw comparisons | Tables 1–3, Figures 1–3 |
| `03_models` | H1–H3, exploratory category/mechanic analysis, robustness, assumption checks | Tables 4–11, Figures 4–8 |

## Setup

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

Then run the notebooks in `notebooks/` in numerical order, from top to bottom.

## Group 1

Thijs Bischoff, Teun Voesenek, Shan Oomes, Dave Sigon, Menno van der Sijpt
