# Netflix Content Explorer

A menu-driven Python project for exploring the Netflix Movies and TV Shows dataset using Pandas and NumPy.

## Features

- Compare the number of movies and TV shows.
- Explore titles added each year.
- Find the top 10 producing countries and top five genres.
- Inspect content rating distributions and release-year ranges.
- Search titles by keyword and filter content by year added.
- Count country values and calculate release-year summary statistics.

## Technologies

Python, Pandas, NumPy, and Jupyter Notebook.

## Getting started

Use Python 3.11 or later. Open a terminal in this project folder and run:

```sh
python -m venv .venv
```

Activate the environment on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Or on macOS/Linux:

```sh
source .venv/bin/activate
```

Install dependencies and start Jupyter:

```sh
python -m pip install -r requirements.txt
jupyter notebook
```

Open `netfix_analysis.ipynb` and run the cells in order. Keep `netflix_titles.csv` beside the notebook. The interactive menu accepts options 1–10; enter 0 to exit and allow subsequent cells to run. The sample search and year-filter cells also request input.

## Project files

| File | Purpose |
| --- | --- |
| `netfix_analysis.ipynb` | Data inspection, cleaning, analysis functions, interactive menu, and discussion |
| `netflix_titles.csv` | Dataset supplied with the original project (8,807 records) |
| `requirements.txt` | Python dependencies |
| `.gitignore` | Excludes virtual environments, caches, and local settings |

## Data preparation

Missing countries, directors, cast members, and ratings receive descriptive placeholders. Records with missing dates added are removed. Dates are converted to datetime values, and a year-added column is derived for analysis. Country and genre lists are split into individual values when counting.

## Scope and limitations

This is an exploratory data analysis project. Results describe the supplied historical dataset and do not represent the current Netflix catalog. It does not train a machine learning model or provide streaming functionality. The current unique-country calculation includes the `Unknown` placeholder. Keyword searches use Pandas regular-expression matching.

The dataset is included as supplied in the original project archive. Its original source and redistribution license were not documented in that archive. Netflix names and content metadata belong to their respective owners; this project is not affiliated with Netflix.
