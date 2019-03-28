# londonVIsit

This repository aims to decide which attractions to visit in London as a function of the number of days that you will be visiting, by applying K-means algorithm.

As input you need to give the GPS coordinates of the main attractions you want to visit during your stay, and the number of days you are planning to be visiting.
Notice that attractions that are not within map screenshot boundaries will be discarded. See Disclaimer below.

The K-means algorithm will interpret:
List of GPS coordinates of the main attractions that you want to visit as 2D samples, after converting to UTM.
Number of days of the visit as Number of clusters.

Of course, this is rather unrealistic because of several reasons, such as:
- Not taking into account if they want to just pass by London Eye, or have a ride on it; 
- Assumes that we are in a no man’s land since it completely bypass the existence of other buildings, roads, …; 
- Does not consider altitude, even though London is rather plane;
- Does not consider the number of attractions that one can possibly do per day;
- Plus, if there was to be an attraction really far from the centre, it may happen that the algorithm considers an entire day for it (this would depend upon kernel initialisation)

Nonetheless, I think this is a funny exercise, and if I were to select the areas to visit by myself, it would most likely be a similar choice to the one taken by K-means.

Disclaimer: I did not know how to use Google API (neither wanted to pay for a key to be fair) hence I just took a screenshot of google maps and wrote down the coordinate of the lower left corner, so that I could use it as my origin. I also took the right top corner coordinate so that I could give the map with an “accurate” scaling. 

Note: GPS coordinates (latitude, longitude) have degrees has units, thus, explaining why the conversion to UTM coordinates, which uses meters.
