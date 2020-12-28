# UFOs Analysis
  Analysis of UFO sightings.
  
## Overview of the analysis
Build a table using data stored in a JavaScript array. Then create filters to make this table fully dynamic, meaning that it will react to user input, and then place the table into an HTML file for easy viewing.
After that, customize a webpage using Bootstrap, and equip the table with several fully functional filters that will allow users to interact with our visualizations.
For the challenge, provide a more in-depth analysis of UFO sightings by allowing users to filter for multiple criteria at the same time. In addition to the date, we will add table filters for the city, state, country, and shape.
The following outputs will be produced:

- Filter UFO sightings on multiple criteria
- A written report on the UFO analysis
  
## Resources
- Data Source: hawaii.sqlite
- Software: Python 3.7.6, Pandas, Jupyter, VSCode, SQLite, SQLAlchemy, Flask

## Results
The analysis of Oahu's weather data data shows that:
  - Average temperature is fairly stable across the year, being June's average slighlyly higher (75 against 71);
  - Temperatures ate more stable whithin the month in June (std 3.26 against 3.75), but both overall fairly stable;
  - Although there are few outliers (56 in December), there are not many cold days, as the 25% percentile is 73 and 69 (with fewer cold days in June)
  
- June Statiscs
![June Statiscs](/June_stats.png)

- December Statiscs
![December Statiscs](/December_stats.png)
 
## Summary

Based on the results above, we reached the conclusion that, given the temperature analysis, the surf and ice cream shop business is sustainable year-round.  However, for a more accurate opinion, it would be necessary also analysing preciptation and data from the station with the highest number of temperature observations, as it tends to be more reliable.

  - Preciptation:  
  
    - June
   
      results = session.query(Measurement.prcp).\
      filter(extract('month', Measurement.date) == 6).all()
    
    - December  
    
      results = session.query(Measurement.prcp).\
      filter(extract('month', Measurement.date) == 12).all()
    
  - Highest Obsvervation Station:
  
    - June
  
      results = session.query(Measurement.tobs).\
      filter(Measurement.station == 'USC00519281').\
      filter(extract('month', Measurement.date) == 6).all()
    
    - December
    
      results = session.query(Measurement.tobs).\
      filter(Measurement.station == 'USC00519281').\
      filter(extract('month', Measurement.date) == 12).all()
  
