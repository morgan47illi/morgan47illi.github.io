---
layout: default
title: Homework 5.1
---

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

## Plot 1: Sightings by Day of the Week
<div id="vis1"></div>

<script>
  vegaEmbed('#vis1', 'ufo_day_of_week.json');
</script>

**Description & Design Choices:**
This bar chart visualizes the total number of UFO sightings based on the day of the week they occurred. I used a Nominal encoding for the x-axis (day of the week) and a Quantitative encoding for the y-axis (total count). I colored the bars by the day of the week (Nominal) to help visually separate the categories. In my Python notebook, I transformed the data by converting the datetime column into pandas datetime objects, extracting the specific day names, and dropping any null values from that column.

---

## Plot 2: UFO Sightings Map by Shape
<div id="vis2"></div>

<script>
  vegaEmbed('#vis2', 'ufo_map.json');
</script>

**Description & Interactivity:**
This interactive scatter plot maps out UFO sightings geographically using latitude and longitude. I used Quantitative encodings for both the x-axis (longitude) and y-axis (latitude). I applied a Nominal colormap to the UFO shape to differentiate between the types of objects reported. In Python, I transformed the data by coercing the latitude and longitude columns to numeric values and filtering the dataset to only include the top 10 most common shapes. For interactivity, I added a dropdown menu to filter by UFO shape. This makes the visualization more interesting because it allows the user to see if certain shapes (like triangles or fireballs) are clustered in specific geographic regions.

---

## Links
[The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/ufo-scrubbed-geocoded-time-standardized-00.csv)
[The Analysis](https://github.com/morgan47illi/morgan47illi.github.io/blob/main/IS_445_hw.ipynb)