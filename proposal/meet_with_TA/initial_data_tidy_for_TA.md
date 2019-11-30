Initial Data Tidy
================
Xun Wang
11/18/2019

#### Sampling some datasets for the first meeting with the TA.

The codechunk below generates a dataset with 100,000 samples randomly
sampled from the [TLC TriP Record
Data](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page),
January 2018.

yellow\_tripdata\_2018\_01 = read\_csv(file = “/Users/Kasza
Lab/Desktop/yellow\_tripdata\_2018-01.csv”) %\>% janitor::clean\_names()
%\>% sample\_n(10000) %\>% arrange(tpep\_pickup\_datetime)

write.csv(yellow\_tripdata\_2018\_01,
“./tmp/yellow\_tripdata\_2018\_01\_sampled.csv”, row.names = FALSE)

green\_tripdata\_2018\_01 = read\_csv(file = “/Users/Kasza
Lab/Desktop/green\_tripdata\_2018-01.csv”) %\>% janitor::clean\_names()
%\>% sample\_n(10000) %\>% arrange(lpep\_pickup\_datetime)

write.csv(green\_tripdata\_2018\_01,
“./tmp/green\_tripdata\_2018\_01\_sampled.csv”, row.names = FALSE)

fhv\_tripdata\_2018\_01 = read\_csv(file = “/Users/Kasza
Lab/Desktop/fhv\_tripdata\_2018-01.csv”) %\>% janitor::clean\_names()
%\>% sample\_n(10000) %\>% arrange(pickup\_date\_time) %\>% view()

write.csv(fhv\_tripdata\_2018\_01,
“./tmp/fhv\_tripdata\_2018\_01\_sampled.csv”, row.names = FALSE)
