# car-sharing-analysis
What is the situation of mobile car sharing in China?  How people live with mobile car sharing?  What can we improve in mobile car sharing?

Demo: https://youtu.be/7xicwqQjBKE

We crawled the POI data from map API. After offset correction, we got locations of office building and residential area. To figure out when most people go to work, we first select orders that pick up in residential area and drop off in office building as working trip. To determine whether a pick-up place belongs to residential area, we calculate distance from pickup location to every residential area, pick-up place with minimum distance below 50 meters could be considered as residential. In the same way, we determine whether a drop-off is office building. After that, we generate order density plot, most people go out for work at 8:40, and arrive the office around 9:30.

To figure out the road traffic situation in morning rush hour, we generate vehicle flow heat map from gps data. From 7 am, people live in suburb go out for work, and drive by elevated outer ring highway, making this sector as hot area. Then traffic flows gradually gather to city center, with high density area centralizing. There are several hotspots of vehicle density distributed at city center and crossroads. 

This is our analysis process of popular pick-up and drop-off places. We use contour plot on map and hour selection, to get a general idea of the spatial distribution of car sharing orders during different hour. We also make comparison between weekday orders and weekend orders. From the line plot we can see car sharing order amount during the day.

The previous contour plot can be visualized only on static map. To do deep analysis on high order density area, we particularly extract the high density contour line and find interesting patterns by making comparison with poi markers on interactive map.

For example, we extract the high level contour line from drop-off plot at 9am. Here we can see there are many office building markers inside the extracted contour, which means most people work in this area.

Shopping: There is also interesting pattern that most car sharing orders happened in similar area in the afternoon, no matter weekday or weekends. The extracted area highly coincides with the most famous commercial area in Chengdu, with many restaurants, theaters, shopping malls inside. That’s why people’s afternoon activities centralize in this area.

Deserve to be mentioned, hot-pot restaurant and teahouse are popular catering place in Chengdu. From this density plot, orders with teahouse as destination mostly happened around 3pm, when people go for afternoon tea. And orders with hot-pot as destination mostly happened in lunch time and dinner time.

Night Life: From this density plot of orders pick up or drop off at pubs, we can see Chengdu night life starts from 8 pm and end up after midnight. 

Tourist attraction: The most famous attraction in Chengdu is the cute animal panda. Most orders arrive in Chengdu Panda Research Base around 10 am. Because panda baby feeding show starts at 10：30 everyday. 
