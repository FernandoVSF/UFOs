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
- Data Source: data JavaScripy file
- Software: JavaScript, HTML, Bootstrap, CSS, VSCode

## Results
This page provides fully functional filters, using multiple criteria, that allows user's interaction as shown in the example below:

  - Initial Page
  
![initial](/initial.png)

   - Filtering by Shape = light
  
![f1](/f1_shape.png)
  
   - Adding filter by State = ca
  
![f2](/f2_state.png)

   - Adding filter by City = el cajon
  
![f3](/f3_city.png)

   - Adding filter by Date = 1/1/2010
  
![f4](/f4_date.png)



 
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
  
