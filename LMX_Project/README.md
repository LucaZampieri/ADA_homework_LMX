# Title : Stay Safe in Geneva

# Abstract

This project will investigate the Geneva accidents from 2010 to 2016. The main goal is to draw as many insights as possible in order to use this information to reduce and avoid future accidents in this region. Not just having a global overview of the ensemble of accidents but elaborate a more detailed analysis depending the time, seasonality, weather, road conditions, location, ect. In this way, more localisated prevention measures could be effectuated by predicting the type of accident in the different regions of Geneva.


# Research questions
The following research questions will be answered:

* Which are the main causes of accidents?
* Which are the type vehicles with more accident risk in Geneva?
* Can we identify clusters by type, time, and causes of accidents?
* How does the weather influences on the risk to have an accident?
* Does the time of a day influences on the risk to have an accident?
* Does the day of the week influences on the risk to have an accident?
* Where are the regions or routes with more accidents in Geneva?
* Is the state of the route is correlated with the risk to have an accident?
* Can we predict the safety of a new installation (e.g. round-abouts), based e.g. on neiboorhood and trafic zone?
* Given two/three possible routes, can we select the safest?

# Dataset
List the dataset(s) you want to use, and some ideas on how do you expect to get, manage, process and enrich it/them. Show us you've read the docs and some examples, and you've a clear idea on what to expect. Discuss data size and format if relevant.

Our datasets have been taken on:
http://ge.ch/sitg/sitg_catalog/sitg_donnees?keyword=&distribution=tous&datatype=tous&topic=transportation&service=tous
and can be found by searching for their name (hereby in noted in bold characters)

From _Swiss open data_ site, the datasets selected are the following:
* **ACCIDENTS DE LA CIRCULATION (DEPUIS 2010)**: **main dataset**         
  Dateset with information about the accidents with gravity, geolocalisation, and kind of involved person and vehicle, meteo, state of the road, kind of accident, and cause.
  - Size: 6.54 MB
  - Number of datapoints: 19'231
  - Number of features: 35
  
  
* **COMPTAGE DU TRAFIC ROUTIER**:       
  Dataset with information about trafic in given roads. We are interested in name of roads and averaged trafic data that can complement our main dataset


* **GRAPHE DE LA MOBILITE - GRAPHE ROUTIER**:         
  Complementary information about the kind of road. There are attributes of the road like lenghts, if it is unique sens or not, classification, number of lanes, restrictions about the weight (ect) associated to a road name


eventually: 
* **GRAPHE DE LA MOBILITE - CARREFOURS**:        
  Dataset with additional information about the kind of carrefour. Most of it is "autres carrefours", for round-abouts we have the diameter. We would need to link each of these carrefours to their linked roads. 
 
All the dataset are in .csv format and are accompagned with a good documentation

A way to enrich the main dataset is to cross information with trafic density data, important points in the city, corossing points, etc.


# What we have done so far?
### Week 1 (1st nov - 8th November) : 
1. Missing values
2. Change the data formats
3. Understand the categorical data
4. Find distributions 
5. Correlations between the different features
6. Find patterns
7. Check for errors/dubious data


### Week 2 (9th - 16th November):
1. Search for external dataset that could further complete our dataset
2. Understand the new data
3. Transform this data
4. Merge with the global dataset
5. Relate adress, road and geolocalisation of our datasets
6. Begin exploratory analysis


### Week 3 (17th - 24th November)
1. Finalise the exploratory anlysis and feature engineering (Find on 01_Geneva_accidents.ipynb).
2. Brainstorm about the main pilars of this project (visulaizations, predictiors, clustering, etc)

    
### Week 4 (25th November - 28th December) 
1. Interactive visualization of the accidents plan (Find on 05_Viz_of_accidents_distribution_on_the_territory.ipynb):
    2.1 Create a GeoJSON of the regions
    2.2 Accidents per region
    2.3 By conditions (light, road, weather,...)
    2.4 By vehicles
2. Create Road risk feature plan (Find on 03_Road_name_traffic.ipynb):
    3.1 Request street names with GoogleAPI
    3.2 Merge with traffic data
    3.3 Define Road risk
3. Start notebook to create the group accident predictor depending certain conditions 
 

# Planning for milestone 3:
### Week 5 (29th November - 6 December)
1. Go deeper on the exploratory analysis to find out interseting insights. Do more feature engineering.
2. Create a unique interactive map with more filters and conditions (A user-friendly interactive map to identify main insights)
3. Plot traffic and accidents in the same plot
4. Continue working on the predictor.

### Week 6 (7th - 13th December)
1. Creating the github website and brainstorm about the structure
2. Improve visualizations
3. Improve predictors


### Week 7 (14th - 29th December)
1. End the site 



# Questions for TAa
* Is there any preprocessing technique as PCA that works well with categorical data?
* What classifiers do you recommend us to work with categorical data?
* We have troubles to visualize interactive maps (different layers) on nbviewer. Do you have any recommendation?


# Note about the rights: 
right notice: 

to use the data you would need to: (in French)

* Vous mentionnez la paternité : « Source : Système d'information du territoire à Genève (SITG), imprimé et/ou extrait en date du […] »
* Vous mentionnez clairement toute modification ou autre traitement apporté aux géodonnées.
* Vous respectez la protection des données.
* Vous partagez à des conditions identiques.

thus for the data files we should cite:

_Source : Système d'information du territoire à Genève (SITG), imprimé et/ou extrait en date du 31 octobre 2017_