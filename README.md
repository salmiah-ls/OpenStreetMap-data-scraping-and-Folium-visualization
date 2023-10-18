# OpenStreetMap (OSM) Data Scraping and Folium Visualization
## OpenStreetMap
<p align='justify'><b>OpenStreetMap (OSM)</b> is a free, open geographic database updated and maintained by a community of volunteers via open collaboration. Contributors collect data from surveys, trace from aerial imagery and also import from other freely licensed geodata sources.</p>
Link to OpenStreetMap:
<li> Map: https://www.openstreetmap.org/</li>
<li> Wiki: https://wiki.openstreetmap.org/</li>

## Folium
`folium` builds on the data wrangling strengths of the Python ecosystem and the mapping strength of the `leaflet.js` library. Manipulate data with Python, then visualize it on a Leaflet map via `folium`.
Link to `folium`:
<li>https://python-visualization.github.io/folium/</li>
<li>https://pypi.org/project/folium/</li>

## Concept
In this repository, I collect data of medical facilities (hospital, clinic, doctor, dentist, and pharmacy) in Bali province, Indonesia. The data contains 4 atrributes: name of the medical facility, type, and coordinates in latitude and longitude. The scraped data is saved in a csv file and then displayed in simple html page.

## Area of Interest: Bali Province, Indonesia
Visualize the area of interest with library `folium`:<br />
<img src="https://github.com/salmiah-ls/OpenStreetMap-data-scraping-and-Folium-visualization/blob/master/images/Bali.png" width="800"></img><br /><br />

## Scraping data from OpenStreetMap (OSM)
If we search keyword `"hospital in Bali"` in OpenStreetMap, the result will be like this:
<img src="https://github.com/salmiah-ls/OpenStreetMap-data-scraping-and-Folium-visualization/blob/master/images/search_result.png" width="600"></img><br /><br />
Here, I will collect data of medical facilities consisting clinics, dentists, doctors, hospitals, and pharmacies.

### Libraries, API and Query
I use 3 libraries for scraping data:
- ` pandas ` for manipulating and analyzing data,
- ` requests ` to make and process HTTP requests,
- ` json ` to parse JSON into dictionary or list.

API link for OpenStreetMap: `http://overpass-api.de/api/interpreter`

Query for searching medical-facilities in Bali, Indonesia:
```
[out:json];
(area['name:id'='Provinsi Bali'];
node[amenity~'(clinic|dentist|doctors|hospital|pharmacy)'](area);
);
out;
```

### Output
There are 2 output files from this project:
1. A [CSV file](https://github.com/salmiah-ls/OpenStreetMap-data-scraping-and-Folium-visualization/blob/master/list_medical.csv) contains data of medical facilities in Bali.
2. An [HTML page](https://github.com/salmiah-ls/OpenStreetMap-data-scraping-and-Folium-visualization/blob/master/Bali_medical_facilities.html) contains map for visualizing the data.

Since **github** can't render html page correctly, I put the final output of this code in my blog [here](https://sites.google.com/view/salmiah-ls/bali).
