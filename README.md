**IBM Data Science Capstone Project**



1. Description of Problem & Background:

Imagine you wanted to open a restaurant in New York City. You want to maximize your revenue, but you don't know which neighborhood in New York City is most in need of a restaurant, and what type of restaurant you should open. There are nearly 200 neighborhoods in NYC spread across 6 main boroughs, each with a different population and a different number of restaurants and cuisines, so there is no easy way to decide where to open your restaurant. However, with the suitable data, this can be solved. My project aims to analyze data from all the neighborhoods in New York City, and determine which neighbourhood is best to open a new restaurant in (based on population, number of restaurants...etc) and what type of restaurant is most suitable to maximize sales.


2. Description of Data


I will be analyzing data about the 195 neighborhoods in New York, collected from 3 main datasets.

A. **Geospatial data from NYC Open Data**: This dataset contains the name of each neighbourhood in New York City, the borough they belong in, as well as the latitude & longitude of each neighbourhood. This data will be used to make 'explore' queries using the FourSquare API. 

B. F**ourSquare data**: Inputting the geospatial data, the FourSquare API can output all the restaurants within a certain radius of each neighbourhood. This allows us to count the number of restaurants in the vicinity of each neighbourhood so we can determine which neighborhood is most in need of a new restaurant. This data can be further analyzed to reveal the types of cuisines available for each neighborhood. However, the number of restaurants is not sufficient to tell us which neighborhood to open the restaurant in - we need the population of each neighborhood as well.

C. **Population data**: This dataset contains the population of each neighborhood in New York City.


Using this data, we can calculate divide the number of restaurants in each neighbourhood by the population of the neighbourhood, and multiply it by a constant (say, 1000) to give us the number of restaurants per 1000 people in each neighbourhood. The smaller this number, the more 'in need' the neighbouhood is for a new restaurant, because there are very few restaurants per 1000 people. The neighbourhood with the smallest value may be deemed the best place to open the new restaurant. We will then analyze the cuisines for each of the existing restaurants in the neighbourhood, and decide what type of restaurant should be opened, based on what types of food is not currently available there.
