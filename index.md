---
layout: default
title: Homework 5.1
---

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

## Plot 1: Most Common UFO Shapes Reported
<div id="vis1"></div>

<script>
  vegaEmbed('#vis1', 'ufo_shapes.json');
</script>

**Description & Design Choices:**
This bar chart visualizes the total UFO sightings by shape. I used a Nominal encoding for the x-axis (shape) and a Quantitative encoding for the y-axis (count). I colored the bars by shape (Nominal) to help visually distinguish the categories. In Python, I transformed the data by dropping null values and disabling the max rows limit.

---

## Plot 2: UFO Sightings Over Time
<div id="vis2"></div>

<script>
  vegaEmbed('#vis2', 'ufo_timeline.json');
</script>

**Description & Interactivity:**
This line chart displays the number of UFO sightings over time. I used an Ordinal encoding for the x-axis (year) and a Quantitative encoding for the y-axis (count). I did not use a colormap because a single trend line does not require one. In Python, I transformed the data by extracting the year from the datetime column. For interactivity, I added a country dropdown filter, which makes the visualization more interesting by letting users compare historical trends between different nations.

---

## Links
[The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)
[The Analysis](https://github.com/morgan47illi/morgan47illi.github.io/blob/main/IS_445_hw.ipynb)