# Surfs_Up

## Project Oerview:

The purpose of this project is to provide W. Avy a weather analysis of Hawaii's beaches. This project is to open a "Surf 'n Shake" shop that will serve surfboards and ice-cream to locals and tourists. Based on the previous analysis, W.Avy wants more information about temperature trends befoer opening the surf shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business will be sustainable all-year-round. 

## Results:

https://github.com/AnureetKaurVirdi/Surfs_Up/blob/main/Resources/December_Temperature_Statistics.jpg
https://github.com/AnureetKaurVirdi/Surfs_Up/blob/main/Resources/June_Temperature_Statistics.jpg

1. The June temperatures range from 64 degrees F to 85 degrees F whereas December temperature fall between 56 degrees F to 83 degrees F.
2. The temperatures in December are more spread out than in June since the standard deviation of December temperatures is higher.
3. The average temperature in June is 75 degrees F whereas in December it is 71 degrees F. Also 50% of June and December temperatures are above 70 degrees F on average. 

## Summary:

The temperatures in December are slightly lower than June but they are suitable for surf and ice-cream shop business. More interesting weather data could be gathered by anayzing the following queries: 

### o The total precipitation levels for June and December:

session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()

session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()

### o The amount of precipitation at the most active station for June and December:

session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 6).all()

session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 12).all()
