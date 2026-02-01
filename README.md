# Dimension Reduction on the Steam Games Dataset

An exploratory analysis of ~70 k Steam titles using PCA, correlation analysis, and DBSCAN clustering in R.

## Dataset
The dataset used in this project is the Steam Games Dataset by FronkonGames, published under a CC-BY-4.0 license. It contains information on over 110,000 games and was collected automatically using the Steam-Games-Scraper — a tool that queries the Steam Web API to retrieve the full app list and then fetches detailed metadata for each title, filtering out DLCs, soundtracks, and utilities so that only actual games are included. The resulting fields cover a wide range of signals: pricing, platform support, review counts, playtime statistics, peak concurrent users, and estimated ownership ranges.

## What's in here

| File | Description |
|---|---|
| `steam_dim_reduction_clustering.Rmd` | Main R Markdown notebook |
| `games.csv` | Raw dataset |

## How to reproduce

1. Install the required R packages (listed in the `Libraries` chunk of the notebook).
2. Open `steam_dim_reduction_clustering.Rmd` in RStudio.
3. Click **Knit** (or run `rmarkdown::render("steam_dim_reduction_clustering.Rmd")`).

## Key findings

- **PC1** captures market success & player engagement (Peak CCU, reviews, playtime, owners).
- **PC2** reflects game-design and ecosystem depth.
- **DBSCAN** identified a dominant cluster of low-engagement titles plus a handful of clear outliers.