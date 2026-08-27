
---

# Pre-Conference-Course-EnvPE-ISPE2026

Welcome to the ISPE 2026 Environmental Pharmacoepidemiology: Overview, Methods, and Applications pre conference skill course.

**INFO**: Saturday, August 29, 2026 9:00 AM - 12:30 PM CEST **Location**: Brown 3, Level 2.

If you encounter any issues with accessing these files or have any question please email us!

[Lizbeth Gomez](liz.gomez@ifh.rutgers.edu) \| [Chloe Smit](chloe.smit@uts.edu.au) \| [Sudha Raman](sudha.raman@duke.edu)

Here you can find teaching materials for the GIS module of the **ISPE 2026 pre-conference skill course**, *"Introduction to GIS Methods for Environmental Pharmacoepidemiology."* This module is a hands-on R exercise: attendees take real CDC surveillance tables and build a complete GIS workflow, attribute joins, choropleth maps, and small-multiples panels across years and seasons, while learning to watch for the specific ways area-level analysis can mislead you in this field (MAUP, ecological fallacy, surveillance-effort bias).

## Getting started

### Cloning this repo

``` bash
git clone https://github.com/<your-username>/gis-envpharmacoepi-ispe2026.git
cd gis-envpharmacoepi-ispe2026
```

Open `exercises/GIS_Intro_Exercise_EnvPharmacoepi.Rmd` in RStudio and run the **Setup** chunk first — it installs and loads everything else needs (`sf`, `tigris`, `dplyr`, `tidyr`, `readr`, `readxl`, `janitor`, `ggplot2`, `viridis`, `scales`). `tigris` downloads U.S. state boundary files from the Census Bureau on first use and caches them locally, so you'll need an internet connection at least once.

The `.Rmd` expects the three files in `data/` to sit in its own working directory. Easiest path: copy or symlink the three files from `data/` into `exercises/` before knitting, or open the `.Rmd` from inside `data/`'s parent and adjust the `read_csv()`/`read_excel()` paths to `"../data/..."`

## Contents

| Path | What it is |
|------------------------------------|------------------------------------|
| `exercises/GIS_Intro_Exercise_EnvPharmacoepi.Rmd` | R Markdown exercise. You can open the knited HTML or work through it chunk by chunk. |
| `instructor/EXTRA-EXERCISE-AND-ANSWER-KEY.Rmd` | Worked solutions for an independent-practice section (Part 8). **Contains spoilers** — see the note below. |
| `slides/GIS_Slides_EnvPharmacoepi.qmd` | Quarto (`revealjs`) slide-deck version of the same material, for the lecture portion of the session. |
| `data/` | The three CDC datasets used throughout, `cb_2025_us_state_20m` which has the Cartographic Boundary Files from US Census Bureau, `DATA_SOURCES.md` which provides references. | 
|`resources/` | Handout and extra readings. |

## What you'll learn

- Importing and cleaning real, messy public-health surveillance data in R
- Getting U.S. state boundary polygons and understanding what a coordinate reference system (CRS) is doing for you
- The **attribute join** — attaching non-spatial tabular data to spatial geometry by a shared key
- Choropleth (thematic) mapping with `ggplot2` + `sf`
- **Small-multiples map panels** across years and seasons, and why the color scale has to be shared across panels for the comparison to be fair
- Reading **seasonality** in area-level surveillance data, both as a plain distribution and as a mapped pattern
- Naming the specific ways area-level GIS analysis can mislead you in environmental pharmacoepidemiology: the Modifiable Areal Unit Problem (MAUP), ecological fallacy, and surveillance-effort bias

## Where to go next

This module covers introductory level mapping techniques and examples. The natural next question — is a pattern you can *see* on a map actually clustered more than chance would produce? — is answered with spatial autocorrelation statistics (global and local Moran's I via the `spdep` package).

## Data & licensing

The three datasets in `data/` are U.S. federal government works (CDC) and are in the **public domain** in the United States (17 U.S.C. §105). See `data/DATA_SOURCES.md` for the original portal for each file, what it contains, and how to re-download a current extract.
