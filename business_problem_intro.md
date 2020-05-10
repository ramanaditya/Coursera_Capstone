# Maintaing Social Distancing during COVID-19

The world is getting affected with COVID-19 and we do not have enough medications to fight with this pandemic. But certainly there are a lot of measures that can be taken in order to avoid or minimize this pandemic

Unfortunately this is not taken in srious actions and the effect caused are increasing day by day. Governemnt need to force people not to crowd or gather together.

__In this project, I will analyze different parts of Pandemic, using Foursquare API, information from Wikipedia, and data from OpenStreetMaps, to find out the places which are crowded in real time and will infrom the concerned authorities about this__. I will use different criteria, which I consider important.

_Please take into account, that this project is simplified and inlcudes only some basic criteria, thus it does not reflect whole reality._

## Usage of data in planning

For our project, I decided to set several criteria, which may be important for analysis of different locations. But before that, we need to decide how to determine what is _part of Pandemic_. 

### Dividing city into different neighborhoods / districts

- The data will be divided on the basis of districcts.
- The location getting higher than expected number of users will be regarded as danger zone.
- When the specific location gathers more number of people it will notify the concerned authorities.
 
For our purpose, it is best to use Cadastral areas, as they are smaller (thus more precise) than Administrative or Municipal districts.

### Selecting our criteria
As our criteria I decided to ask following questions, about each district:

 - How much is the district good for relaxation?
     - What is the size of nature areas (forests, parks,...) available to public in the district? (available on OpenStreetMaps)
     - How many clubs, bars and hotels are in the district? These places usually attract people who wants to enjoy their free time, so there could be problems . This data is also available on Foursquare.
     - Also what is the population density - more people means usually more danger. This is available on Wikipedia
 - How much is the district suitable in terms of public services? 
     - How many hospitals, pharmacies, and clinics are in the district? (available on Foursquare)
     - How many stores and supermarkets are in the district? (available on Foursquare)
     - Is there any public transport station? (available on Foursquare)
     
There is more criteria which could be considered, but for purpose of our project, these should be enough.

## How the data will be used and processed

For figuring out solution for this problem, we will do multiple clustering of districts according to different criteria. This will show us how districts can be grouped according each of criteria. Each of this criteria can be quantified and it can be told, whether higher values of that criteria are better or worse for purpose of the project. Then we will try to find intersection of districts, that were grouped into best, or at least not worst (for criteria that are less important) clusters according to each criteria.
