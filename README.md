# Overview
The purpose of this analysis is to help provide Aloha with the temperature data for specifically the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round and thus, properly assuring W. Avy of his investments to be made on your business.

# Results
Three key differences in weather between June and December;
  -The average temperature for the month June and December, which was 74.9 and 71.0 as seen in the images folder repectively.
  -The min, max for the month of June and December was 64, 85 and 56, 74 as seen in the images folder repectively.
  -The total count of the temperature records for the month of June and December was 1700 and 1517 as seen in the images folder respectively.
  
# Summary
The average temprature was higher in the month June than in December, therefore meaning, people are morely likely to surf or get ice cream in December period than in the month of June.
Two additional queries to perform to gather more weather data for June and December could include;
-The data for precipitation could be calculated for June and December respectivily using;
          results = session.query(Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
-The stations and teperature could also be considered for the month of June and December to know which stations has the min or max temperature.
          results = session.query(Measurement.tobs,Measurement.station).filter(extract('month', Measurement.date) == 12).all()
