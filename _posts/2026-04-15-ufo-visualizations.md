<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<a href="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/ufo-scrubbed-geocoded-time-standardized-00.csv" class="btn btn-primary">The Data</a>
<a href="https://github.com/morgan47illi/morgan47illi.github.io/blob/main/ufo_analysis.ipynb" class="btn btn-primary">The Analysis</a>


<div id="vis1"></div>
<script>
  vegaEmbed('#vis1', 'ufo_shapes.json');
</script>

**Design & Transformation:** This bar chart visualizes the total count of different UFO shapes reported. I used a nominal encoding for the x-axis (shape) and a quantitative encoding for the y-axis (count). I colored the bars by shape to visually separate the categories. On the Python side, I used pandas to convert the raw string dates into actual `datetime` objects, dropping any rows with invalid dates so the data was clean before passing it to Altair.


<div id="vis2"></div>
<script>
  vegaEmbed('#vis2', 'ufo_timeline.json');
</script>

**Interactivity:** This line chart shows the volume of UFO sightings over time. Because the dataset includes sightings from all over the world, viewing everything at once can be overwhelming. I added a dropdown menu tied to an Altair `selection_point` that filters the data by country. This interactivity makes the visualization much more useful, allowing users to choose specific trends—for example, comparing historical sighting spikes in the US versus the UK.

