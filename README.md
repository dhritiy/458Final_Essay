# Analysis of the NASA Earthdata Coivd-19 Dashboard
### **NASA Earthdata Covid-19 Dashboard:** https://earthdata.nasa.gov/covid19/

![Dashboard](https://github.com/dhritiy/458Final_Essay/blob/main/img/Intro%20Image.PNG?raw=true)

#### **Dashboard Introduction**
***Project Goal:*** Due to the coronavirus pandemic, the majority of the world has faced a big a shift and had to move their lives indoors. There have been many dashboards created that attempt to analyze the negative impacts of the coronavirus and to perform risk analysis. However, with Earthdata dashboard, the National Aeronautics and Space Administration (NASA) aimed to go past the individual risk dashboard, and they tried to present a change in the Earth and climate due to the pandemic. Through the use of their monitoring systems, NASA has been able to track changes in multiple places across the world during this time.

Specifically, through this dashboard, NASA wanted to present changes that they saw in Water Quality, Air Quality, Landscapes, and Climate. In order to do so, NASA created 8-9 different thematic layer for each of these of these topics based on the data and statistics they were presenting.

**Water Quality Layer:**
![Water Quality](https://github.com/dhritiy/458Final_Essay/blob/main/img/Water%20Quality.PNG?raw=true)
*Caption:* In this layer, NASA is examing the levels of Chlorophyll-a in the waters in Chesapeake Bay. This chemical is an indicator of algae growth and a darker red color was used to represent areas with more growth and worse water quality. The darker bluer represents areas with less growth.  Since Chesapeake bay is often affected by human activities this could potentially be an increase in water quality because of pandemic related shifts.

**Air Quality Layer:**
![Air Quality](https://github.com/dhritiy/458Final_Essay/blob/main/img/Air%20Quality.PNG?raw=true)
*Caption:* In this layer, NASA aims to examine the imapct of Covid-19 on Air Quality around the world. There are many areas around eastern USA and Europe that have blue overlaid indicating a decrease in Nitrogen Dioxide levels. NASA was able to use this layer to hypothesize as people transitioned to remote working, the quanity of air pollutants emmitted drastically decreased, thus increase air quality.


**Changing Landscapes Layer:**
![Changing Landscapes](https://github.com/dhritiy/458Final_Essay/blob/main/img/Changing%20Land%20Scapes.PNG?raw=true)
*Caption:* One of the most intersting layer that NASA presented was through the use od their High Definition Nightlights dataset. This data contains information of how much light is emmitted from a variety of different energy sources and uses. As people began to travel, shop, eat out, and socialize less, there were much fewer nightlights. The darker purple and pick areas represent a lower amount of nightlights, where as yellow areas present an increase.


**Climate Change Layer:**
![Climate Change](https://github.com/dhritiy/458Final_Essay/blob/main/img/Climate%20Change.PNG?raw=true)
*Caption:* NASA was able to use a similar thematic and base map as they used in the Air Quality layer to present a new idea in the climate change layer. Here they analyzed the decrease and increase in carbon dioxide levels at a global scale. Which most of Asia and the west is blue and saw lower CO2 levels, the area around Austalia was a dark red. This area actually saw an increase in carbon dioxide levels due the wildfires that swept through Australia towards the end of 2019.

***Audience and Use:***
The intended audience of this smart dashbaord and the web maps it contains is the average internet user. NASA presents an easily accessible and readable dahsboard and makes sure to clearly explain all of the data and scientific elements in relation to climate change. This dashboard could also be directed to people who are doing scientific research on the coronavirus pandemic and its impact on climate. For scientific research, this dashboard would only provide a basic starting point. In order to access more advance materials and articles, the user would have to navigate to the Additional Resources part of each section. Here they will be directed to more in depth NASA resources. By not presenting all of the in-depth data on the main dashboard, NASA ensures that they are able to easily convey their research to a casual and average viewer.

***Web Mapping Elements and Interactivity:***
NASA made use of several basic mapping elements such as a scalar bar and legend. However, they never used a north arrow. Most of the time it was clear which way is north, but sometimes when they presented a zoomed in map of a region or an inset a map, a north arrow would have been very useful.

They also had several different forms of interactivity. For example, in the Changing Landscapes layer above you can see the horizontal slider in the middle of the map. As you move the slider to the right, you are able to see more of a map from an earlier time period (January 2020). As you move the slider to the left, you can see more of a more current map (February 2020). This element of interactivity allows the user to view multiple time periods on one map and perform more analysis.

They also had a tool to zoom in and out of the map. As you zoomed in very close into one country or city, you would be able to see more features of that location. For example, NASA displayed locations of different airports, their names, and denotated them with a plane marker in teh Air Quality layer.

***Authors and Data Sources:*** The majority of the data used in this dashboard was all collected by NASA through the use of the global satellite system. They were also able to gather some of this data by using scientific instruments that ar on the International Space Station and also through some ground observatories. In order to further the analysis presented in this dashboard, the authors (NASA scientistics), worked with the Japan Aerospace Exploration Agency(JAXA) and European Space Agency(ESA). By working with multiple agencies, they were able to perform a much deeper and more detailed analysis of climate change during the global pandemic.

The majority of this data is from January 2020 to the present, as this is the duration of the pandemic. However, at times NASA also used earlier data from 2019 in order to analyze change in patterns over time.



#### **Systemic Architecture:**
The data used in this smart dashboard came from a variety of different sources and in order to compile and power it, NASA used an API. This was an open source api that was specifically created as "lightweight tile server" for coronavirus related data. The file format that they used for their data were GeoTIFFs. This is a raster based format and since it is cloud supported, it allowed for NASA to create a more advanced web application.

In order to manage the data flow and set up the environment for the wbe page NASA used node.js and Yarn which is a packaging manager. Then they created three different environments: local.js, staging.js, production.js. Essentially they started with local.js to begin any development that needs to be done locally. Then they would use the staging file server. Finally when the production file server is created, it overrites the other two.

One of the intersting things with data flow here is that the dashboard uses livereload. As NASA collects live data and inputs it into its database, that data is then processed and presented to the client on the smart dashboard. The website that hosts this dashboard makes use of http://localhost:9000/. Then whenever the system notices a change in the data files or executes a new task, the webpage will refresh.


#### **UI/UX Critique (Pros and Cons):**
Does this project support responsive design?:
Descripe basemap, thematic layer, and interactive features:
One thing that really stood out as a positive for this dashboard was NASA's use of different basemaps for different thematic layers. Often times, creators of smart dashboards will use the same basemap in all of the web maps they are presenting. However, NASA used a variety of basemaps. For example, in some web maps they used a Grayscale basemap which allowed the reader to be able to clearly see the data NASA was presenting. They did this mainly when they were presenting a choropleth or density thematic layer. In others, where it was important to understand the urban geography of the region, NASA used a Satellite basemap. By doing so they were able to present their narrative in an informative way and still allow the viewer to easily and quickable comprehend the data.

Additionally, another pro of this smart dashboard was the was its responsive web design. The images, web maps, and layouts of the different web pages were all very flexible and they rendered very well on screens of different sizes. As I moved the below indicator dashboard from my laptop, to my larger monitor screen, the size of the map exapanded to fit the width of the screen. The Insights text on the right also automatically enlarged and so did the graphs to better fit the height of the screen. The smart dashboard was also responsive when I accessed it my mobile device. Many dashboard usually struggle with have a cohesive and understandable mobile desing. But the NASA earthdata dashboard made use of a variety of different hamburger menus to aid with navigation. This allowed me to view the map and then collapse it and navigate to a different indicator. When I toggled on a new indicator, the dashboard would automatically bring up the web map for it.

One critique, I have for this dashboard is the way in which climate change indicators were presented. As you can see in the image below, I chose to use the dashboard to show the Agriculture indicator in Beijing. Here NASA is aiming to present the global changes and performace of food access and supply flows. From this web map, I can only see that there is an area in Eastern China that is performing at the Exceptional level on the agriculture scale and the rest of China seems to have no data. This was an issue a that I saw with many of the indicators. As a suggestion, rather than showing a map of China that mainly has no data, I would have the basemap automatically zoom into the area that is green and exceptional. Here, in the dashboard Insights text on the right, I would explain that this area is exceptional. But then I would also reclassify this Agriculture indicator to show the different level of exceptional food supply flows in this region of China.

Additionally, another con I see with this map is that there is no search bar. This make it hard for the user to navigate through the dashboard or web maps to find the topic that they are looking for. If the user could type in a location on climate change indicator they are intersested in and immediately see all of the places this smart dashboard writes about that topic, they would be much more inclined to use it.

**Indicator Dashboard:**
![Climate Change](https://github.com/dhritiy/458Final_Essay/blob/main/img/Climate%20Change.PNG?raw=true)

#### **Connection to Social Theories:**
