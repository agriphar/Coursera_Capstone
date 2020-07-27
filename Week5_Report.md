# Coursera Capstone 
<br>
## IBM Data Science Course Final Report 
<br>
<br>

# Opening A New Restaurant in Shanghai, China
<br>
#### By: Jeffrey Hu
##### July 2020
<br>
<br>

## Background Introduction
As we all know, opening a restaurant of your own is one of the biggest dream for many entrepreneurs. However, as with any business decision, it may require serious consideration and is much complicated than it seems. Particularly, the location of the restaurant is one of the most important decisions that will determine whether it will be a success or not.  
<br>  

## Business Problem
The aim of this capstone project is to analyse and choose the best location in the city of Shanghai, China to open a new restaurant. Using data science methodology and machine learning techniques like clustering, the project's purpose is to provide a solution to answer the question: In the city of Shanghai, China, if someone is looking to open a restaurant, where would you recommend that they open it?  
<br>

## Data Section
#### The following data will be needed for us to solve the problem:  
* List of administrative divisions of Shanghai: this defines the scope of this project which is confined to the city of Shanghai, one the of biggest city in East Asia.
* Latitude and longitude coordinate of these administrative divisions, which is needed to plot the map and get the venue data.
* Venue data, especially data related to restaurants. We will use them to perform clustering algorithm on the neighbourhoods to find the best location.

#### Source of data and methods to extract them
The wikipedia page <https://en.wikipedia.org/wiki/List_of_administrative_divisions_of_Shanghai> contains a list of administrative divisions of Shanghai, with a total of 16 administrative divisions. We will use web scraping techniques to extract data from the wikipedia page, with the help of Python requests and other library packages. Then we will get the geographical coordinates of the neighbourhoods using Python Geocoder package which will give us the latitude and longitude coordinates of the neighbourhoods.  

After that, we will use Foursquare API to get the venue data for those neighbourhoods. Foursquare has one of the largest database of 100+ million places and is used by over 125,000 developers. Foursquare API will provide many categories of the venue data and we will be particularly interested in the restaurant category in order to help us to solve the business problem we put forward.  

This is a project that will make use of many data science skills, from web scraping, working with API(Foursquare), data cleaning, data wrangling, to machine learning (K-means clustering) and map visualization(Folium). In the next section, we will present the Methodology part where we will discuss the steps taken in this project, the data analysis and the machine learning techniques we've used. 


### Methodology
Firstly, we need to get the list of administrative divisions in the city of Shanghai. Through wikipedia page <https://en.wikipedia.org/wiki/List_of_administrative_divisions_of_Shanghai>, we will do web scraping using Python requests and libraries to extract the list of neighbourhoods data. However, this is just a list of names. We need to get the geographical coordinate in the form of latitude and longitude in order to be able to use Foursquare API. Through Geocoder package, we convert address into geographical coordinates in the form of latitude and longitude. After gathering the data, we will populate the data into a pandas DataFrame and then visualize the neighbourhoods in a map using Folium package. This allows us to perform a sanity check to make sure that the geographical coordinates data returned by Geocoder are correctly plotted in the city of Shanghai.  

Next, we will use Foursquare API to get the top 100 venues that are within a radius of 2000 meters. We need to register a Foursquare Developer Account in order to obtain the Foursquare ID and Secret key. We then make API calls to Foursquare passing in the geographical coordinates of the neighbourhoods in a Python loop. Foursquare will return the venue data in JSON format and we will extract the venue name, category, latitude and longitude. With the data, we can check how many venues were returned for each neighbourhoods and examine how many unique categories can be curated from all the returned venues. Then, we will analyse each neighbourhood by grouping the rows and taking the mean of frequency of occurrence of each venue category. 

Finally, we will analyse the result and give some useful recommendations for opening a restaurant in Shanghai based on their frequency of occurrence. According to their different frequency rate in different neighbourhoods, it will help us to answer the question as to which place is most suitable to open new restaurants. 


## Results 
The results can be shown on the following frequency chart.

<br>
<br>
<br>
<br>

## Discussion and Observations  
For the question that we want to answer, "how to open a restaurant in Shanghai" depends on which kind of restaurant you want to choose from.

Base on the principle of __knock-on effect__, we advice you'd better open a restaurant which is located near other similar ones.

For this reason, we get some conclusions as follows: 

1. Qingpu District will be a best choice if you want to open a __coffee shop__ because its frequency is as high as 0.50; Minhang, Yangpu and Pudong New area can also be considered since their frequency is more than 0.20
2. If you want to open a Chinese restaurant, then Changning and Chongming District should be your first consideration since it is the 1st most common venue in this area. 
3. Fengxian District is a good choice for Korean style and Putuo District is suitable for Fast Food restaurant.
4. For westerners, Huangpu and Xuhui district can be considered first because they have the highest rate of frequency for western style restaurant, say, French, Italian, Cocktail Bar, etc. 


## Conclusion and Suggestions for Further Research 
In this project, we only consider administrative divisions of Shanghai and its frequency rate of occurrence. In fact, deeper and more specific sub-districts can be divided into more details, and there are other factors such as population and income of residents that could also influence the location decision of a new restaurant.  

However, to the best knowledge of this research, such data are not available to the neighbourhood level required by this project. Further research could devise a methodology to estimate such data to be used in the clustering algorithm to determine the preferred locations to open a new restaurant. 

In addition, this project made use of the free Sandbox Tier Account of Foursquare API that came with limitations as to the number of API calls and results returned. Further research could make use of paid account to bypass these limitations and obtain more results. 

In this project, we have gone through the process of identifying the business problem, specifying the data required, extracting the preparing the data, performing machine learning by analysing the data and give some recommendations to the relevant stakeholders, say, property developers and investors regarding the best location to open a new restaurant in Shanghai.


## References 
List of administrative divisions of Shanghai. Wikipedia. Retrieved from 
<https://en.wikipedia.org/wiki/List_of_administrative_divisions_of_Shanghai>

Foursquare Developers Documentation. Foursquare. Retrieved from   
<https://developer.foursquare.com/docs>









 









