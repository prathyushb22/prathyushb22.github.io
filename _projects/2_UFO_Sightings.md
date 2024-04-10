---
name: UFO Sightings Exporation
tools: [Python, HTML, vega-lite]
description: This post delves into the intriguing world of Unidentified Flying Object (UFO) sightings, showcasing two distinct visualizations derived from analysis of reported sightings across the globe. Our investigation utilizes a comprehensive dataset, revealing patterns and insights into the frequency and nature of these occurrences.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# UFO Sightings by Country

This bar chart visualizes the frequency of UFO sightings reported across different countries. The primary goal is to highlight geographic trends in UFO reporting, showcasing which countries have the highest number of sightings. In designing this visualization, I chose a nominal encoding for the country variable on the x-axis, with each country represented as a separate category. The y-axis quantitatively encodes the number of sightings, using a linear scale to reflect the count of reports in each country. For the color scheme, each bar is uniformly colored to maintain focus on the number of sightings rather than the countries themselves, ensuring readability and avoiding unnecessary complexity. This design choice simplifies the visualization, directing attention to the comparative heights of the bars. During the analysis phase, the data was filtered to exclude any records with missing or ambiguous country information, ensuring accuracy in the depiction of geographic distribution. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart_country.json" style="width: 100%"></vegachart>

# UFO Sightings by Shape and Country

The second visualization is an interactive bar chart depicting the distribution of UFO sightings by shape, offering insights into the most commonly reported forms. This interactive element allows users to filter sightings by country, adding a layer of engagement and specificity to the analysis. For this plot, the shape variable is encoded nominally on the y-axis, showcasing the variety of reported UFO shapes, while the x-axis quantitatively represents the count of sightings for each shape. The use of distinct colors for different shapes enhances the visualization's readability and aesthetic appeal, making it easier for viewers to distinguish between shapes. In preparing the data, records with unspecified shapes were filtered out to ensure the clarity and relevance of the information presented. The interactivity component was introduced by enabling a dropdown selection for countries. This allows users to explore the data more deeply, examining how the prevalence of different UFO shapes varies across countries.

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart_shape.json" style="width: 100%"></vegachart>

## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/prathyushb22/prathyushb22.github.io/blob/main/python_notebooks/ufo_sightings.ipynb" text="The Analysis" %}
</div>
