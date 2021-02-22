# Bicing® 2019 Visual Analytics

> Static/Interactive visualizations to evaluate the performance of Bicing®  stations depending on their geospatial location.

The aim of this project is to develop effective, expressive, appropriate and information-rich visualizations that allow the user to identify with a glance the behaviour of the [Bicing®](https://www.bicing.barcelona/es) users of a particular Barcelona area/station, compare them attending to different criteria (time granularity, day of the week/weekends *e.g.*) and ease the exploratory and confirmative analysis of the data.

*Note: To perform such visualizations, the [Altair library](https://altair-viz.github.io/) has been used.*

---
This project is divided into two sections:

## 1. Static visualizations

In this section, three different [Bicing®](https://www.bicing.barcelona/es) stations were selected (302, 98,334) to compare their evolution among the selected month (October).

These stations were selected according to the following criteria:

> * 302 : Station located near FIB. As we previously mentioned, we found that analyzing a station near a university should be interesting, as different patterns depending on the students' schedules may be observed.
> * 98: Station located near Sants-Estació. We selected this station because it's one of the biggest public transport stations in Barcelona and has subway, bus and train connections.
> * 334: Station located in the Sarrià neighbourhood. This location was selected in order to see if a more wealthy neighbourhood behaves differently than the rest of the selected stations. Also, we found pretty interesting how its location would affect the daily use, as it's located in a high-altitude zone of Barcelona.

*Note: Fragment extracted form the [Visualizations](./Static/Visualizations.ipynb) file.*

<p align="center">
  <img src='README Images/Overview.png'/ width = 500>
</p>

### 1.1 Used visualizations 

* Superposed/Juxtaposed line charts
* Grouped bar charts
* Heatmap
* Juxtaposed bar charts

<p align="center">
  <img src='README Images/Heatmap.png'/ width = 500>
</p>


### 1.2 Architecture

The files contained in this section are:

* [`Data cleaning script`](./Static/Data Cleaning.ipynb) used to cleanse the [Open Data BCN original file](https://opendata-ajuntament.barcelona.cat/data/es/dataset/estat-estacions-bicing), as well as explanations about the decisions made during the process.
* [`Clean data`](./Static/CleanData.csv): CSV file obtained as the output of the cleaning process.
* The set of [visualitzations and their respective interpretations and comparisons](./Static/Visualizations.ipynb) about the behaviour of the three selected stations.

## 2. Interactive visualizations

In this section, the data of all [Bicing®](https://www.bicing.barcelona/es) stations was used. The objective of this unit consists of evaluating the activity by district produced in Barcelona in October 2019.

<p align="center">
  <img src='README Images/Choropleth.png'/ width = 500>
</p>


### 2.1 Used visualizations
* Choropleth
* Bubble chart
* Scatter plot
* Histogram
* Graduated symbol map
* Heatmap
* Line chart

<p align="center">
  <img src='README Images/Bubble.png'/ width = 500>
</p>


### 2.2 Used interactions
* Multi-district selection.
* Type of bike selection (*total, mechanic, electric*).
* Day of the month slider.
* Tooltip text when the user moves the mouse over the item.

*Note: All the interactive methods perform cross-selection between the different visualizations*

### 2.3 Architecture

The files contained in this section are:

* [`Data cleaning script`](./Interactive/Preprocessing.ipynb) used to cleanse and daily resume the [Open Data BCN original file](https://opendata-ajuntament.barcelona.cat/data/es/dataset/estat-estacions-bicing), as well as explanations about the decisions made during the process.
* [`Clean data`](./Interactive/CleanData.csv): CSV file obtained as the output of the cleaning process.
* An auxiliar [Bicing® geospatial info](./Interactive/bicing_station_districts.csv) .CSV file used to develop the visualitzations containing maps.
* The set of [visualitzations and their respective interpretations and comparisons](./Interactive/Visualizations.ipynb) about the behaviour of the different districts.

---
*Note: The rest of the files in the master branch are auxiliary or license related*

## Team

This bot was developed by:
| [![Vinomo4](https://avatars2.githubusercontent.com/u/49389601?s=60&v=4)](https://github.com/Vinomo4) | [![Marcfuon](https://avatars3.githubusercontent.com/u/49389563?s=88&u=95fb18db55ceae0b49215950980506783481fbbe&v=4)](https://github.com/marcfuon) |
| --- | --- |
| [Victor Novelle Moriano](https://github.com/Vinomo4) | [Marc Fuentes Oncins](https://github.com/marcfuon) |


Students of Data Science and Engineering at [UPC](https://www.upc.edu/ca).

## License

[MIT License](./LICENSE)
