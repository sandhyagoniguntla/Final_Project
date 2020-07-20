# DATA Section:

The Data required for the  cities  Newyork and Toronto is extracted and Processed.
###  New York city crime data  
 **NYPD Complaint Data Historic** is loaded from [NYC open data](https://opendata.cityofnewyork.us).
This dataset includes all valid felony, misdemeanour, and violation crimes reported to the
New York City Police Department (NYPD) from 2006 to the end of year 2019. 
The data is  based on Report Date ( the date the incident was actually reported to the NYPD) and the nearest Precinct.

Data fields of interest in this data set are as follows.
- *ADDR_PCT_CD*  : The precinct in which the incident occurred 
- *BORO*  : The name of the borough in which the incident occurred 
- *LAW_CAT_CD* :  Level of offense: felony, misdemeanor, violation 
- *RPT_DT*  : Date event was reported to police 
-  *X_COORD, Y_COORD_CD*  : coordinates for New York State Plane Coordinate System
- *Longitude ,Longitude* :  coordinates for Global Coordinate System

The dataset is loaded and processed for Visulization .The  crime statistics based on year,
precinct and borough wise are visualized using matplotlib.

The actual Coordinates of Precinct House are extracted using Foursquare API  using search query .
The dataset **newyork_data.json** which contains the 5 boroughs and the neighborhoods that exist in 
each borough as well as the the latitude and longitude coordinates of each neighbourhood is used for the search query.
 
 To  get the Police precincts  geographical location in the neighborhoods, within a radius of 1000 meters a search Query is formed.
After  examining  the results, the  information of interest is processed  and dataframe is filtered.
The actual Precinct locations are shown using the   **geojson file of Newyork  city precinct boundaries**  using Chloropleth maps.
(boundaries data is loaded from NYC Open Data)


### Toronto city crime data 

**Toronto crime Dataset Major Crime Indicators(MCI) 2014 to 2019** occurrences by reported date is used for the Visulization. 
*Toronto crime data is available at [Toronto Public safety Dta Portal](https://data.torontopolice.on.ca/search?q=crime)

Data fields of interest in this data set are as follows.

- *ReportedDate* : Date the incident reported to Police
- *MCI* : The Major Crime Indicators categories are Assault, Break and Enter, Auto Theft, Robbery and Theft Over
- *Division* : Police Division in which the incident occured
- *Neighbourhood* : Neighbourhood in which the incident occured
- *Lat,Long* : coordinates for Global Coordinate System

The data is loaded, Analysed and processed for the visulization .Visulization is performed using matplotlib and chlopleth maps.
The crime statistics based on year,month and Division are visualized using matplotlib.

The **geojson file of Toronto city divisions boundaries** is used and crimecount is visualized using Chloropleth maps.
To compare the crimes , years 2014 to 2019 are considered for both the cities.
