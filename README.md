# UFC Fight Analytics - Interactive Visualization Tool

(Data Visualization course - Project) 

This project was developed as part of the "Data Visualization" course at the Universidad Politécnica de Madrid (Master in Digital Innovation - EIT Digital). It presents an interactive Shiny web app for analyzing fight data from the Ultimate UFC Dataset.

[**Live App**](https://davissiemens.shinyapps.io/final/)

[**Dataset Source**](https://www.kaggle.com/datasets/mdabbert/ultimate-ufc-dataset)

## 📁 Project Structure
```
.
├── app.R                     # Shiny application source code
├── report.pdf                # Full group report structured by abstraction levels
├── data/                     # Folder containing CSV files
│   ├── ufc-master.csv        # Main UFC fight dataset from Kaggle
│   └── countries.geojson     # GeoJSON with country polygons for map rendering
│   └── us_states.geojson     # GeoJSON with US state polygons for map rendering
└── README.md                 # Project description and instructions
└── requirements.txt          # List of R package dependencies to run the app
```

## Project Overview
The goal was to build an interactive tool that assists analysts in exploring UFC fight data through multiple visual idioms. Each idiom was designed to answer specific analytical questions using visualization techniques and interactions.

This was a group project consisting of **four members**. **My contribution** focused on **Idiom 2**: "Exploring Fight Outcome Distributions Across UFC Weight Classes".

### Features
- Idiom 1 – Finish Trend Analysis Over Time (stacked area chart)
- **My Part:** Idiom 2 –  Outcome Distributions by Weight Class (interactive radar chart)
- Idiom 3 – Heatmap of Fight Rounds vs Age & Country
- Idiom 4 – Geographic Distribution of UFC Fights (choropleth maps)

## My Contribution – Idiom 2: Exploring Fight Outcomes
I was responsible for designing and implementing Idiom 2, an interactive radar chart for exploring fight outcomes across UFC weight classes. This module allows analysts to:
- Compare finish types (KO/TKO, Submission, Decisions, etc.) by weight class
- Filter data by gender and whether the fight was a title bout
- Dynamically select which finish types to include in the chart
- Use hover tooltips, legend filtering, and zoomable axes
### Features I Implemented
- Radar Chart (Plotly) to visualize multi-variable distributions
- Filter Controls:
  - Gender switch (Male/Female)
  - Title Bout toggle
  - Finish Type selector with "Select All / Deselect All"
- Interactive Legend & Tooltips for exploratory analysis
- Dynamic rendering to adjust based on selected filters

This idiom supports both discovery (e.g., identifying unexpected patterns in title fights) and comparison (e.g., contrasting male vs. female outcome trends) across weight classes.

For a full explanation of the design, data abstraction, task abstraction, and implementation, refer to the Idiom 2 section in report.pdf from page 13 to page 17.

## Requirements

Install the following R packages before running the app locally:
```
install.packages("leaflet")
install.packages("sf")
install.packages("dplyr")
install.packages("readr")
install.packages("tidyr")
install.packages("stringr")
install.packages("ggplot2")
install.packages("plotly")
install.packages("fmsb")
install.packages("shinyWidgets")
```

## Run Locally

```
# In RStudio or any R environment:
shiny::runApp("app.R")
```
