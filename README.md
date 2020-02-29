# Project3

Shamber Goldstein | B ME 450 | February 28, 2020 | Project 3: Plate Tectonics

## Introduction:

Earthquakes are caused by convection between the core and crust which causes movement in the tectonic plates. This movement can create three different boundary types: divergent, convergent, and transform. The divergent boundary is when two plates slide apart from each other causing magma to rise in between them, cool, and form a new plate. The convergent boundary occurs when two plates slide toward each other, either colliding or creating a subduction zone (one plate moves under the other). This can create mountain ranges, volcanoes, and trenches. Finally, the transform boundary is where two plates slide parallel to each other creating faults that can result in strong earthquakes [1].

The purpose of this project was to analyze earthquake locations and magnitudes around the Juan De Fuca Plate. This included plotting earthquake magnitude vs. time as well as plotting earthquake locations and magnitudes on a map for 10 years of data. The combination of these plots allow us to determine earthquake patterns in different location and at different times. Looking at the earthquake locations on the map also allows us to determine the boundary types by looking at the geographical properties at those locations. The project also instructed to recreate the map plot for the month of April only. Doing this allows us to consider the possible causes of the earthquakes that month.

## How I Did it:

I began my code by importing any packages that I needed in my code. I then loaded in my 2010-2020 earthquake data as a csv. This data I found using the USGS Earthquake Catalog [2] where I was able to download data for the specified years and the specified longitude and latitude which included the Juan De Fuca Plate. After loading in the data I extracted the variables that I needed to proceed with my code: time, earthquake magnitude, earthquake longitude, and earthquake latitude. I put these into easy-to-access lists. I had to convert the time into local time. I did this by cycling through the time values and converting them into a format that displayed them as year-month-day-hour-minutes-seconds. I then took these dates and converted them to the local time zone. I used these converted times to plot the earthquake magnitudes versus time. I was able to do this by simply using the scatter plot from matplotlib, and plotting the converted times on the x-axis and the extracted magnitudes on the y-axis. 

The next task was to graph the earthquake locations and magnitudes on a map of the area I took data from. I was able to figure this part out thanks to the Towards Data Science website [4]. I first calculated the maximum and minimum latitudes and longitudes of the area and saving this as a variable called bb (boundary box). I then downloaded my map using Open Street Map [3] where I was able to enter in these latitudes and longitudes and get a map of that area only. I imported this image into my code and plotted the latitudes and longitudes on it. I looped through each earthquake magnitude value and checked with a series of if statements how large the magnitude was. In the if statement that magnitude fell into, I plotted the corresponding latitude and longitude of that earthquake along with a color and size (larger magnitude = larger size). This resulted in a plot of earthquake magnitude according to location, layered over the map. The project asked to repeat this plot for the month of April 2015 only. To do this I loaded in data again from the USGS Earthquake Catalog, but only for this month. I found this was much easier to do than loop through the data I had and extract only the data for that month. I then extracted the needed data from this file and repeated the plotting process with the same map and the narrowed down data.

## Results/Plots:

Figure 1: Plot of Earthquake Magnitude vs. Time

Figure 2: Map of Earthquake Locations and Magnitudes (10 years)

Figure 3: Map of Earthquake Locations and Magnitudes (April 2015)

## Analysis/Conclusions:

a. Across what geographic area are you able to observe earthquake data in this map? Why do you see most of the earthquakes in that area? 

As shown in Figure 2, most of the earthquake data appears in the southern half of the map (below 45 degrees latitude) going diagonally more south from west to east. There is also a large cluster of earthquakes in the northwest corner, going along the same diagonal. Most earthquakes fall along this diagonal line because this is where the plate boundaries lie between the Pacific, Juan De Fuca, and North American Plates. This means that condensation in the earth mantle causing the plates to move then causes one of the three boundary conditions, each of which result in earthquake(s).

b. What is the range of earthquake size (magnitude) in these data? What is the average earthquake size in this area?

The minimum earthquake magnitude found in the data is 2.5. However, we limited our lowest magnitude to 2.5 when downloading the data from the USGS Earthquake Catalog so there are likely earthquakes lower than this in the area that we are not looking at. The maximum magnitude found was 6.8. The average magnitude was 3.24. The average being in the middle of the range (from 0 to 6.8) proves that there is a pretty even distribution of larger and smaller earthquakes in the Pacific Northwest region.

c. Map the earthquakes in April 2015 (include this map in your report). Where are those earthquakes mostly located? What event can you link these earthquakes to?  

The map for April 2015 is shown in Figure 3. There seem to be three regions with earthquake data. The first is along the coast, the second is horizontal across the southern region of the map, and the last is in the western area of the map (in the Pacific). The biggest cluster seems to be in the last mentioned area. After doing some research, these earthquakes can be linked to the eruption of the Axial Seamount submarine volcano that occurred that month [5]. 

d. Identify a divergent boundary and a transform boundary on the map you selected in part I.

A divergent boundary can be found where the Juan De Fuca Plate meets with the Pacific Plate at the east most boundaries. This area has a long submarine mountain chain called the Juan De Fuca Ridge. Young volcanoes, lava flows, and hot springs have been discovered in this area [6]. This supports that this area is divergent because this boundary type causes lava to flow up through the surface. The Juan De Fuca Plate is separated into fracture zones by transform faults [7]. These boundaries are shown on the map in Figure 2 in the zig zag pattern of earthquakes in the southern half of the map. Transform boundaries cause strong earthquakes, explaining why the earthquakes in this area have high magnitudes. The convergent boundary can be clearly seen by the subduction zone on the east side of the Juan De Fuca Plate, off the coast of North America.

e. What kind of patterns in earthquake magnitude and location you observe over time along each boundary?



## References:

[1] Shima Abadi. In Class Lecture – Marine Geology. [19 Feb. 2020].
	
[2] USGS Earthquake Catalog. (2020). Latest Earthquakes. [online] Earthquake.usgs.gov. Available at: https://earthquake.usgs.gov/earthquakes/map/  [Accessed 29 Feb. 2020].

[3] OpenStreetMap. (2020). Export | OpenStreetMap. [online] Open Street Map. Available at: https://www.openstreetmap.org/export#map=5/51.500/-0.100 [Accessed 29 Feb. 2020].

[4] Ahmed Qassim. (2020). Easy Steps To Plot Geographic Data on a Map — Python. [online] Towards Data Science. Available at: https://towardsdatascience.com/easy-steps-to-plot-geographic-data-on-a-map-python-11217859a2db [Accessed 29 Feb. 2020].

[5] Caplan-Auerbach, J., Dziak, R., Bohnenstiehl, D. and Garcia, C. (2017). Explosive processes during the 2015 eruption of Axial Seamount, as recorded by seafloor hydrophones. [online] Advancing Earth and Space Science. Available at: https://agupubs.onlinelibrary.wiley.com/doi/full/10.1002/2016GC006734?fbclid=IwAR0Qv0COOkBMUOwQ_oHyu_WKYEfpQ_696rYNStmbg9y4-gU-ifsWPmQUjfc [Accessed 29 Feb. 2020].

[6] Cires1.colorado.edu. The Juan de Fuca Microplate System. [online] Available at: http://cires1.colorado.edu/people/jones.craig/WUStectonics/PacNW/juan_de_Fuca_general.html [Accessed 29 Feb. 2020].

[7]  DiPietro, J. (2013). Juan De Fuca Plate - an overview. [online] ScienceDirect Topics. Available at: https://www.sciencedirect.com/topics/earth-and-planetary-sciences/juan-de-fuca-plate [Accessed 29 Feb. 2020].
