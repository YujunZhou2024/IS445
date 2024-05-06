---
name: Visualization 2 Bar Chart
tools: [Python, Altair, Vega-Lite]
image: assets/pngs/cars.png
description: This project showcases interactive visualizations using Vega-Lite.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
# My Interactive Visualizations

Below are the interactive charts that I created using Python, Altair and vega-lite:

## Bar Chart

<vegachart schema-url="{{ site.baseurl }}/assets/json/interactive_bar_chart.json" style="width: 100%"></vegachart>


## Bar Chart Visualization:

*Description:*
This bar chart presents the distribution of various license types alongside their respective statuses, such as active, canceled, or expired. Each bar represents a different license type, and the colors within each bar denote the count of records for each status category for that license type. The goal is to compare the status distributions across different license types, which can indicate patterns like which licenses are most commonly active or subject to certain changes like ownership or cancellation.

*Design Choices:*
I encoded the 'License Type' on the x-axis, as this is the nominal data we are examining. The 'License Status' is represented by the color, with each color indicating a different status. This color coding is essential to differentiate the status types at a glance within each license category. The y-axis quantitatively encodes the count of records, allowing for easy comparison of magnitude across license types and statuses. 

*Data Transformations:*
No additional transformations, such as formatting or restructuring of the original data fields, were required for this visualization task. Internally, the chart aggregates the data by counting the number of records for each combination of 'License Type' and 'License Status' category. No further data manipulation was necessary since Altair handles these operations during the rendering process. The code’s transform_filter function then responds to the user’s selection, updating the chart to reflect only the data for the chosen license type.

*Interactivity:*
Interactivity is introduced with a dropdown menu that allows users to select a specific 'License Type' to filter the chart and display only the statuses for that type. This interactivity turns the chart into a dynamic tool, allowing a user to focus on the information that is most relevant to them and potentially revealing more detailed insights when viewing one license type at a time.

*Comparisons to Homework #7:*
Unlike Homework #7, the current assignment utilizes a completely different dataset, which means there is no direct overlap in the data visualized. 


<div class="left">
{% include elements/button.html link="https://github.com/YujunZhou2024/YujunZhou2024.github.io/blob/main/assets/json/interactive_bar_chart.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/YujunZhou2024/YujunZhou2024.github.io/blob/main/python_notebooks/HW8.ipynb" text="The Analysis" %}
</div>

