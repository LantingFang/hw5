
---
layout: default
title: Homework 5.1 - Bigfoot Reports
---

## Visualization 1: Bigfoot Reports by State

This bar chart visualizes the number of Bigfoot sightings reported in each U.S. state. The `y-axis` encodes the state names, sorted by frequency of reports, and the `x-axis` encodes the total number of reports. A sequential blue colormap is used to emphasize higher-frequency states. This plot helps reveal geographic patterns in the dataset, showing where Bigfoot is most frequently "sighted."

**Encoding choices:** 
- x: `count()` (quantitative) 
- y: `state` (ordinal) 
- color: based on `count()` with a blue colormap (`blues` scale).

**Data transformation:** We used `groupby('state')` in pandas to count the number of reports per state and then sorted the result.

**Homework #5 overlap:** This chart is **entirely new** and was not used in Homework #5. The dataset and variables are both different.

---

## Visualization 2: Bigfoot Sightings Over Time

This interactive line chart shows the temporal trend of Bigfoot sightings over the years. The `x-axis` encodes the year of the report, while the `y-axis` encodes the number of reports in that year. An interactive selection (via brush/slider) allows users to zoom in on specific periods to observe changes more closely.

**Encoding choices:**
- x: `year` (ordinal)
- y: `count()` (quantitative)
- Tooltip reveals the exact count per year

**Interactivity:** A brush-based interval selector allows users to highlight a specific year range, making it easier to explore reporting trends over time.

**Data transformation:** The `date` column was converted to datetime format using pandas, and then `year` was extracted with `dt.year`. Invalid dates were dropped.

**Homework #5 overlap:** This chart is also **entirely new** and does not reuse any previous code or chart structure.

---

## Interactivity Discussion

The interactivity in the second plot (temporal line chart) allows users to select a specific range of years and focus on that subset. This adds clarity by reducing visual clutter and improving the ability to detect localized trends or spikes in the reporting frequency. It enhances user engagement and allows for exploratory analysis.

---

<div style="margin-top: 20px;">
  <a href="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" 
     target="_blank" 
     style="padding:10px 20px; background-color:#007bff; color:white; text-decoration:none; border-radius:5px;">
     The Data
  </a>

  <a href="https://github.com/LantingFang/hw5/blob/main/hw5_notebook.ipynb" 
     target="_blank" 
     style="padding:10px 20px; background-color:#28a745; color:white; text-decoration:none; border-radius:5px; margin-left: 10px;">
     The Analysis
  </a>
</div>
