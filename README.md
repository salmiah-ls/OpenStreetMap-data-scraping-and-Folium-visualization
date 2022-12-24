## OpenStreetMap (OSM) Data Scraping and Folium Visualization

This repository contains tutorial how to collect (scrap) data from OpenStreetMap (OSM) and visualize the data using Folium in Jupyter Notebook (Python).

I collect data of medical facilities (hospital, clinic, doctors, dentist, and pharmacy) in Bali province, Indonesia. The data contains name of the medical facility, type, and coordinates in latitude and longitude. The scraped data is saved in a csv file and then displayed in simple html page. All the code was done in Jupyter Notebook (Python).

### Area of Interest: Bali Province, Indonesia
<img src=Bali.png>

### List of doctors in Bali in OpenStreetMap (OSM)
Example of query searching [**'doctors in Bali'** in OpenStreetMap](https://www.openstreetmap.org/search?query=doctors%20in%20Bali#map=10/-8.4479/115.1216).

### Output
There are 2 output files from this project:
1. A [CSV file](https://github.com/salmiah-ls/OpenStreetMap-data-scraping-and-Folium-visualization/blob/master/list_medical.csv) contains data of medical faciluties in Bali.
2. An [HTML page](https://github.com/salmiah-ls/OpenStreetMap-data-scraping-and-Folium-visualization/blob/master/Bali_medical_facilities.html) contains map for visualizing the data.

Since **github** can't render html page correctly, I put the final output of this code in my blog [here](https://sites.google.com/view/salmiah-ls/bali).
