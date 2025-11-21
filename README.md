# Homelessness in the United States (2007–2024)

This project analyzes trends in homelessness across U.S. states from 2007–2024 using federal Point-in-Time (PIT) counts and state-level population estimates. I focus on how the *proportion* of people experiencing homelessness has changed over time, and how sheltered vs. unsheltered homelessness differ across states.

## Project Overview

- Combines HUD Point-in-Time (PIT) homelessness counts with state population data.
- Cleans and merges datasets by **state** and **year**.
- Creates proportional measures (e.g., homelessness per resident, percent sheltered vs. unsheltered) to make fair comparisons across states and over time. :contentReference[oaicite:0]{index=0}  
- Explores trends in:
  - Overall homelessness rates
  - Proportion of sheltered vs. unsheltered homelessness
  - Differences between selected states and the national pattern

## Data Sources

- **HUD Point-in-Time (PIT) Counts, 2007–2024**  
  Annual state-level estimates of people experiencing homelessness on a single night in January.

- **State Population by Year (U.S. Census-based)**  
  Publicly available dataset with historical state populations by year (used to calculate homelessness *rates* instead of just raw counts).

## Methods

All analysis is done in **R** using an **R Markdown** workflow:

- Imported and cleaned raw PIT and population data.
- Converted key homelessness variables from strings to numeric types.
- Removed rows with missing or unusable data (e.g., territories with no homelessness or population values).
- Created derived variables:
  - `prop_homeless`: total homelessness ÷ state population  
  - `prop_sheltered_of_total`: sheltered ÷ total homelessness  
  - `prop_unsheltered_of_total`: unsheltered ÷ total homelessness
- Generated tables and visualizations to compare states and track changes over time.

## Files in This Repository

- `Project2.Rmd` – Main R Markdown file with full analysis, code, and narrative.
- `Project2.html` – Knitted HTML report generated from the R Markdown file.
- `data/` – (Optional) Folder containing the raw or cleaned datasets, or scripts to download them.

## How to Reproduce

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
