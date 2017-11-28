# Title : Stay Safe in Geneva

# Abstract

We would like to tell a story about road safety in the area of Geneva. As students connected to people that had accidents we would like to have a better understanding of how those tragedies can happen.

For this we will use data from _Swiss open data_, in particular the one from _SITG_ about transportation.

# Research questions
A list of research questions you would like to address during the project: 

* Which are the type vehicles with more accident risk in Geneva?
* Which are the main causes of accidents?
* Can we identify clusters by type of accidents?
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
  
* **COMPTAGE DU TRAFIC ROUTIER**:       
  Dataset with information about trafic in given roads. We are interested in name of roads and averaged trafic data that can complement our main dataset

* **GRAPHE DE LA MOBILITE - GRAPHE ROUTIER**:         
  Complementary information about the kind of road. There are attributes of the road like lenghts, if it is unique sens or not, classification, number of lanes, restrictions about the weight (ect) associated to a road name

eventually: 
* **GRAPHE DE LA MOBILITE - CARREFOURS**:        
  Dataset with additional information about the kind of carrefour. Most of it is "autres carrefours", for round-abouts we have the diameter. We would need to link each of these carrefours to their linked roads. 
 
All the dataset are in .csv format and are accompagned with a good documentation

A way to enrich the main dataset is to cross information with trafic density data, important points in the city, corossing points, etc.


# A list of internal milestones up until project milestone 2
Add here a sketch of your planning for the next project milestone.

Planning:

##### Week 1 (1st nov - 8th Nov) : Understand the data 
 
1. Missing values
2. Change the data formats
3. Understand the categorical data
4. Find distributions 
5. Correlations between the different features
6. Find patterns
7. Check for errors/dubious data

##### Week 2 (9th - 16th nov)  Enrich the dataset

1. Search for external dataset that could further complete our dataset
2. Understand the new data
3. Transform this data
4. Merge with the global dataset
5. Relate adress, road and geolocalisation of our datasets
6. Begin exploratory analysis
    
##### Week 3 (17th - 24th nov) Brainstorm about ideas of how to visualise the results and continue with data processing:
Finalyse the exploratory analysis and find all the patterns and the features we could use to make predictions about the safety of new infrastructures
    
##### Week 4 (25th nov - 2nd dec) Finalize for milestone 2
Finalise the predictive analysis. Use the features found at the previous week to do the predictions

##### Week 5-6-7 (3rd ) Data Vizualisation:
Make website on github with interactive plots for the found results and display a safety map where we could change the transportation mean, hour, weather. Also a tool where the user could input infos about a new infrastructure it could return its safety 
    
 

# Questions for TAa

### project specific:
* How feasible would it be to ask itineraries on the go to google maps and retrieve from it the path of the itinerary (like have the name or geolocalisation of the taken routes)?


### In general:
* Will the exam only contain stuff seen during the homeworks, or it will test us as well on other competences that we should acquire during this course

# note about the rights: 
right notice: 

to use the data you would need to: (in French)

* Vous mentionnez la paternité : « Source : Système d'information du territoire à Genève (SITG), imprimé et/ou extrait en date du […] »
* Vous mentionnez clairement toute modification ou autre traitement apporté aux géodonnées.
* Vous respectez la protection des données.
* Vous partagez à des conditions identiques.

thus for the data files we should cite:

_Source : Système d'information du territoire à Genève (SITG), imprimé et/ou extrait en date du 31 octobre 2017_
