# Pre-Conference-Course-EnvPE-ISPE2026
Welcome to the ISPE 2026 Environmental Pharmacoepidemiology: Overview, Methods, and Applications pre conference skill course.

**INFO**: Saturday, August 29, 2026  9:00 AM - 12:30 PM CEST  **Location**: Brown 3, Level 2.

If you encounter any issues with accessing these files or have any question please email us! 

[Lizbeth Gomez](liz.gomez@ifh.rutgers.edu) | [Chloe Smit](chloe.smit@uts.edu.au)


Here you can find teaching materials for the GIS module of the **ISPE 2026 pre-conference skill course**, *"Introduction to GIS Methods for Environmental Pharmacoepidemiology."* This module is a hands-on R exercise: attendees take real CDC surveillance tables and build a complete GIS workflow, attribute joins, choropleth maps, and small-multiples panels across years and seasons, while learning to watch for the specific ways area-level analysis can mislead you in this field (MAUP, ecological fallacy, surveillance-effort bias).



## Getting started

### Cloning this repo
```bash
git clone https://github.com/<your-username>/gis-envpharmacoepi-ispe2026.git
cd gis-envpharmacoepi-ispe2026
```

Open `exercises/GIS_Intro_Exercise_EnvPharmacoepi.Rmd` in RStudio and
run the **Setup** chunk first — it installs and loads everything else
needs (`sf`, `tigris`, `dplyr`, `tidyr`, `readr`, `readxl`, `janitor`,
`ggplot2`, `viridis`, `scales`). `tigris` downloads U.S. state boundary
files from the Census Bureau on first use and caches them locally, so
you'll need an internet connection at least once.


The `.Rmd` expects the three files in `data/` to sit in its own working
directory. Easiest path: copy or symlink the three files from `data/`
into `exercises/` before knitting, or open the `.Rmd` from inside
`data/`'s parent and adjust the `read_csv()`/`read_excel()` paths to
`"../data/..."`
