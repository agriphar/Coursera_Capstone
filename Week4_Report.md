# <center>Coursera Capstone </center>
<br>
## <center>IBM Data Science Course Final Report </center>
<br>
<br>

# <center>Opening A New Restaurant in Shanghai, China</center>
<br>
#### <center>By: Jeffrey Hu</center>
##### <center>July 2020</center>
<br>
<br>
<br>

## Background Introduction
As we all know, opening a restaurant of your own is one of the biggest dream for many entrepreneurs. However, as with any business decision, it may require serious consideration and is much complicated than it seems. Particularly, the location of the restaurant is one of the most important decisions that will determine whether it will be a success or not.  
<br>  

## Business Problem
The aim of this capstone projecgt is to analyse and choose the best location in the cith of Shanghai, China to open a new restaurant. Using data science methodology and machine learning techniques like clustering, the project's purpose is to provide a solution to answer the question: In the city of Shanghai, China, if someone is looking to open a restaurant, where would you recommend that they open it?  
<br>

## Data Section
#### The following data will be needed for us to solve the problem:  
* List of administrative divisions of Shanghai: this defines the scope of this project which is confined to the city of Shanghai, one the of biggest city in East Aisa.
* Latitude and longitude coordinate of these administrative divisions, which is needed to plot the map and get the venue data.
* Venue data, especially data related to restaurants. We will use them to perform clustering algorithm on the neighbourhoods to find the best location.

#### Source of data and methods to extract them
The wikipedia page <https://en.wikipedia.org/wiki/List_of_administrative_divisions_of_Shanghai> contains a list of administrative divisions of Shanghai, with a total of 16 administrative divisions. We will use web scraping techniques to extract data from the wikipedia page, with the help of Python requests and other liberary packages. Then we will get the geographical coordinates of the neighbourhoods using Python Geocoder package which will give us the latitude and longitude coordinates of the neighbourhoods.  
After that, we will use Foursquare API to get the venue data for those neighbourhoods. Foursquare has one of the largest database of 100+ million places and is used by over 125,000 developers. Foursquare API will provide many categories of the venue data and we wil be particularly interested in the restaurant category in order to help us to solve the business problem we put forward.  
This is a project that will make use of many data science skills, from web scraping, working with API(Foursquare), data cleaning, data wrangling, to machine learning(K-means clustering) and map visualization(Folium). In the next section, we will present the Methodology part where we will discuss the steps taken in this project, the data anyalysis and the machine learning techniques we've used. 








 









