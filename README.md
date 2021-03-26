![Ironhack logo](https://i.imgur.com/1QgrNNw.png)

# Woomie | Final project Data analytics bootcamp - Mexico City

# Team members:
- [Paola Franco](https://github.com/paofrancomonge) 
- [Patricia Villa](https://github.com/patocuak08)
- [Paola Malherbe](https://github.com/PaoMg)

## Introduction

This repository presents the final project of Ironhack Mexico's Data analytics bootcamp.

**Woomie's** goal is to provide Mexican women alternative mobility routes, avoiding insecure areas on public roads in Mexico City.

The general functionality is as follows: the user indicates the point of origin, the point of destination and the method of transportation by which the user is going to move, either walking, by car or by bicycle. 

The final result provides 3 maps: 
- The first one traces 2 routes, a lower-risk route and a higher-risk route. Both with the kilometers and the time it will take to go through them.
- The second one indicates on a 5-color scale the severity of crimes committed on public roads.
- The third one shows on a 3-color scale the time of the day when the crimes were committed on public streets (morning: 05:00 to 12:00, afternoon: 13:00 - 20:00, night: 21:00 - 04:00) 

## What we did

The database we used for our analysis contains updated information of victims in the [investigation files of Mexico City Fiscalía General de Justicia (FGJ)](https://datos.cdmx.gob.mx/dataset/victimas-en-carpetas-de-investigacion-fgj) from January 2019 onwards and from the [2020 census conducted by INEGI.](https://censo2020.mx)


The information had a cleaning process where we considered only crimes committed on public roads where the victims were women.

For the route's calculation we used the direction API from [openroutservice.org.](https://openrouteservice.org/example-avoid-obstacles-while-routing/) This API avoids nodes delimited by longitude and latitude. Also, it helped us to draw polygons with a diameter in meters according to our requirement so that the traced route did not pass near those polygons.

For this API it is necessary to create an API key within the platform

The way to capture information is by a [google sheets](https://docs.google.com/spreadsheets/d/17bfRz3X-qvqHr74QaY4aAYxsaUlFrF1-YiF7r2swFxI/edit?usp=sharing) that connects directly to our colab.


## Colabs

- 5-color scale map with the severity of crimes committed on public roads (painting only one route)
- 3-color scale map with the time of the day when the crimes were committed on public streets (morning: 05:00 to 12:00, afternoon: 13:00 - 20:00, night: 21:00 - 04:00) and painting both routes with time and distance (km)

## Website
- https://woomie.squarespace.com



