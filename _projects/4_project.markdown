---
layout: page
title: Covid19 & Crime
description: Correlation between covid-19 and crime in US cities
img: /assets/img/covid.PNG
importance: 6
---

As a part of Data mining lecture, me and <a href="https://sites.google.com/view/jisukim8873/home">Jisu Kim</a> analyzed the crime data in US cities after and before covid-19.

Washington Post (Jackman, 2020) reported 25% decline in Chicago and up to 20% in Washington and Baltimore between March 16 and April 22, 2020 compared to the same period in 2019. And USA Today reported that weekly calls for service dropped “at least” 12% between February 2 and March 28, 2020 (Jacoby et al., 2020). CNN reports that calls for police service are down in New York City.

Based on the backgroud, we assumed that there would be some differences in crime in US cities by Covid-19. Therefore, we collected Covid-19 data from <a href="https://github.com/nytimes/covid-19-data">NY Times</a> and crime data from cities as below:
  
 * Austin, Boston, Chicago, Cincinnati, Dallas, Denver, Detroit, Forthworth, Los Angeles, Milwaukee, New York, Phonix, Sanfrancisco, Seattle, Washington DC
  
Also, the targeted crime types are as below:

 * theft, assault, burglary, vehicle theft, property, robbery, weapon, drugs, rape, homicide, domestic violence

   
**H1 : Number of crime decreased in 2020 compared to 2019 with the same time period.**

The number of crime decreased by 831,441 to 711,870 (decreased by 119,571) within the same period (2019-01 ~ 2019-09 VS 2020-01 ~ 2020-09).

Next, we used weighted bipartite graph network to analyze the crime and city data as below in the Figure. If there's a occurrence of certain crime in a certain city, the edge between both nodes are connected with updating the weights. 


<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/wb.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
   Weighted Bipartite graph to analyze the crime and city data. 
</div>



**H2: The number of crime occurrences changed in certain cities compared to 2019 which is related to COVID-19.**

We analyzed this by the degree centrality of city graph. If the degree centrality of a certain city gets highers, than the certain city increase with the varous crime types. To figure out the correlationship with covid-19, we averaged the confirmed cases in Feb to Sep. Therefore, we find out that the city with increased degree centrality showed higher confirmed cases whereas city with decreased degree centrality showed lower confirmed cases.


<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/city.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/c1.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
   City Graph and analyzed results.
</div>



**H3: The number of crime occurrences changed compared to 2019 which is related to COVID-19.**

The rate of increase with confirmed cases of covid-19 is over 1,000,000% in between Feb and March, 19% in Aug and Sep. 
We assumed that the number of occurrence of each crime type would be different depends on the increased number of confirmed cases. Not only with the simple number of crime, we get used of the degree centrality of each type, which reflects the crime occurrence within each city, sequentially. We found that there is difference between the number of crime and standardized degree centrality. 

Among the 11 crime types, homicide showed the opposite degree centrality compared to the same period of time in 2019. In 2019 Feb to March, degree centrality increased, but in Aug to Sept decreased. Whereas, in 2020 Feb to March, degree centrality decreased, but in Aug to Sept increased. Considering the difference of increase rate of confirmed cases of covid-10 in Feb to March and Aug to Sept, covid-19 might effect the homicide type crime. 



<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/crime.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/cr1.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
   Crime Graph and analyzed results.
</div>
