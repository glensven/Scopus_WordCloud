# Scopus API Search for WordCloud Generator

![Word Clouds](https://raw.githubusercontent.com/glensven/Scopus_WordCloud/main/Pictures/WordCloud_Titles_Nanosafety_2005_2021.png)

### _Figure 1: Word Cloud of "Nanosfety" related articles from 2005 to 2021_

---

## Executive Summary
This is the main repository for a Scopus Application Programming Interface (API) Search Request of published literature from the Scopus database. The aim of this function is to filter through this database, based on an inputted search term and year range to produce a dataframe and downloadable excel file.  These files contain columns of the published date, titles, and abstracts that are used to produce a graph of publications per year and custom Word CLouds. These graphs and WordClouds can be used for academic purposes to qualitatively understand if interest in this topic is changing, the current sentiment surrounding this topic, and what is the field of research is associated with this search. 

## Introduction
This project was first initiated at Northwestern University in the Office  of Research Safety (RS) to determine the current direction and sentiment of research invovling "Nanosafety" in a quanitative and qualitative methodology. Nanosafety refers to all of the safety issues associated with nanotechnology. This readme will walk the user through how to properly query the API and produce a desired graphical and WordCloud images by using the search term "Nanosafety" as an academic example.

## Methodology
This program utilizes the Elsevier Scopus API on the Elsevier Delevvoper Portal [1]. Scopus allows a researcher to track analyze and visualize research data from 5000 different publishers, covering 78 million items. Elsevier grants full Scopus APIs access to clients with Scopus subscriptions; thus, to use this function a research must have a subscriptions. RS obtained its subscription through Northwestern University. 

Once the code has initiated, the user will be brought to the first page screen with "Nanosafety" as the default search term as seen in Figure 2. This panel will have an input for the search query term and a year range slider. After the desired parameters are inputed, clicked the "Generate Data" button to initiated the search. Depending on the size of the search dataset, this can take several minutes so be patients. Once complete, the graph will update and the user can write a desired filename to download the excel file.

![Search Panel](https://raw.githubusercontent.com/glensven/Scopus_WordCloud/main/Pictures/Search%20Panel.png)

### _Figure 2: Search panel for generating dataframes and graphs._

Once the excel file is saved, go to the wordcloud tab and click on the "Browse" button to upload the file. This will generate two Word Clouds for the Titles and Abstracts. These Word CLouds are generated using the Natural Language Toolkit Library [2]. 

![Word Cloud Panel](https://raw.githubusercontent.com/glensven/Scopus_WordCloud/main/Pictures/WordCloud_Panel.png)

### _Figure 3: Word Cloud panel._

## Dependencies
1) API libraries: requests & json
2) Dataframe libraries: pandas, & numpy
3) Natural Language Processing libraries: nltk & wordcloud
4) Visualization libraries: panel, plotly, hvplot, & param
5) Other libraries: time, datetime, pathlib, re, & io

## References
1) Elsevier Developer Portal, https://dev.elsevier.com/sc_apis.html
2) NLTK 3.6.2 Documentation, https://www.nltk.org/