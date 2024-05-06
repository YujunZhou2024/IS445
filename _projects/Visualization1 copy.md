---
name: Final Project, Part 3
tools: [Python, Altair, Vega-Lite]
image: assets/pngs/cars.png
description: This project showcases interactive visualizations using Vega-Lite.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
**Outline**

**1. Data Preparation**

1.1. Import necessary libraries.

1.2. Read the dataset and perform any initial data filtering or cleaning.

**2. Data Visualization**

Six visualizations were built.

2.1. max_aqi (2): Calculate the average maximum AQI per state and visualize it using a bar chart and a heatmap. 

2.2. good_days (1): Calculate and visualize the average number of good air quality days per state with a bar chart.

2.3. unhealthy_days (1): Calculate and visualize the average number of bad air quality days per state with a bar chart and a year selector.

2.4. air_quality_map (1): Create an interactive plot that updates based on the year selected from a dropdown, showing different kinds of day counts.

2.5. aqi_trend (1): Plot the trend of AQI over the years for a selected state using a line plot with a trend line.

**3. Building Dashboard and refresh button**

3.1. Organize the individual visualizations into a tabbed layout using ipywidgets.tab, with each tab corresponding to a different visualization of the air quality data as shown above.
3.2. Build a refresh button to update all visualizations with new data if needed.


## Area Chart

<vegachart schema-url="{{ site.baseurl }}/assets/json/interactive_area_chart.json" style="width: 100%"></vegachart>


## Area Chart Visualization

*Description:*
This area chart visualizes the trend in the total number of licenses issued over time, with data aggregated monthly. The purpose is to reveal patterns, spikes, or declines in the issuance of licenses and to understand the volume over the years.

*Design Choices:*
The chart is an interactive area chart created using Altair. I chose to encode time on the x-axis and the count of licenses on the y-axis to illustrate the trend clearly. The area under the line is filled to give a sense of volume. No color encoding is used here, as the focus is on the trend over time rather than distinctions between categories. The choice to keep it monochromatic ensures the viewer's attention is drawn to the change over time rather than being split among different colors.

*Data Transformations:*
The original 'LastModifiedDate' field was transformed to a datetime format, and the data was grouped by month to sum up the total licenses issued per month. This transformation was essential to visualize the data on a time series basis effectively.

*Interactivity:*
Interactivity is included through tooltips that display the exact number of licenses issued and the corresponding date when the user hovers over any part of the area chart. This interactive element enhances the chart by providing detailed information on demand, which aids in a more detailed analysis without cluttering the visual presentation.

*Comparisons to Homework #7:*
Unlike Homework #7, the current assignment utilizes a completely different dataset, which means there is no direct overlap in the data visualized. 

<div class="left">
{% include elements/button.html link="https://github.com/YujunZhou2024/YujunZhou2024.github.io/blob/main/assets/json/interactive_area_chart.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/YujunZhou2024/YujunZhou2024.github.io/blob/main/python_notebooks/HW8.ipynb" text="The Analysis" %}
</div>

