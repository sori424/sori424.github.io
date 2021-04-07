---
layout: page
title: Covid19 & Crime
description: Correlation between covid-19 and crime in US cities
img: /assets/img/covid.PNG
importance: 4
---

As a part of Data mining lecture, me and <a href="https://sites.google.com/view/jisukim8873/home">Jisu Kim</a> analyzed the crime data in US cities after and before covid-19.

<h3>Backgroud</h3> 

Washington Post (Jackman, 2020) reported 25% decline in Chicago and up to 20% in Washington and Baltimore between March 16 and April 22, 2020 compared to the same period in 2019.

USA Today reported that weekly calls for service dropped “at least” 12% between February 2 and March 28, 2020 (Jacoby et al., 2020).

CNN reports that calls for police service are down in New York City.

: Crime has in fact decreased in the U.S. since states started moving towards lockdowns.

: Nearly all evidence on calls for service nationwide demonstrate that crime is down, but serious crimes are largely unchanged, ‘everyday-type’ misdemeanors are decreased and highly location dependent.  

Based on the backgroud, we assumed that there would be some differences in crime in US cities by Covid-19. 
Therefore, we collected Covid-19 data from <a href="https://github.com/nytimes/covid-19-data">NY Times</a> and crime data from cities as below:
  
  Austin, Boston, Chicago, Cincinnati, Dallas, Denver, Detroit, Forthworth, Los Angeles, Milwaukee, New York, Phonix, Sanfrancisco, Seattle, Washington DC
  
Also, the targeted crime types are as below:

  theft, assault, burglary, vehicle theft, property, robbery, weapon, drugs, rape, homicide, domestic violence

  ---
  H1 : Number of crime decreased in 2020 compared to 2019 with the same time period.
  ---

The number of crime decreased by 831,441 to 711,870 (decreased by 119,571) within the same period (2019-01 ~ 2019-09 VS 2020-01 ~ 2020-09).

Next, we used bipartite graph network to analyze the crime and city data as below in the Figure. 


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/city.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/crime.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
   Bipartite graph to analyze the crime and city data. Left is city network, Right is crime network made by bipartite graph. 
</div>




