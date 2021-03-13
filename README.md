# Analysis of the NASA Earthdata Coivd-19 Dashboard
### **NASA Earthdata Covid-19 Dashboard:** https://earthdata.nasa.gov/covid19/

![Dashboard](https://github.com/dhritiy/458Final_Essay/blob/main/img/Intro%20Image.PNG?raw=true)

### **Dashboard Introduction**
#### ***Project Goal:***
Due to the coronavirus pandemic, the majority of the world has faced a big a shift and had to move their lives indoors. There have been many dashboards created that attempt to analyze the negative impacts of the coronavirus and to perform risk analysis. However, with Earthdata dashboard, the National Aeronautics and Space Administration (NASA) aimed to go past the individual risk dashboard, and they tried to present a change in the Earth and climate due to the pandemic. Through the use of their monitoring systems, NASA has been able to track changes in multiple places across the world during this time.

Specifically, through this dashboard, NASA wanted to present changes that they saw in Water Quality, Air Quality, Landscapes, and Climate. In order to do so, NASA created 8-9 different thematic layers for each of these of these topics based on the data and statistics they were presenting.

#### ***Water Quality Layer:***
![Water Quality](https://github.com/dhritiy/458Final_Essay/blob/main/img/Water%20Quality.PNG?raw=true)
*Caption:* In this layer, NASA is examining the levels of Chlorophyll-a in the waters of Chesapeake Bay. This chemical is an indicator of algae growth and a darker red color was used to represent areas with more growth and worse water quality. The darker bluer represents areas with less growth.  Since Chesapeake Bay is often negatively affected by human activities, there could potentially be an increase in water quality because of pandemic related shifts.

#### ***Air Quality Layer:***
![Air Quality](https://github.com/dhritiy/458Final_Essay/blob/main/img/Air%20Quality.PNG?raw=true)
*Caption:* In this layer, NASA aims to examine the impact of Covid-19 on Air Quality around the world. There are many areas around eastern USA and Europe that have blue overlaid indicating a decrease in Nitrogen Dioxide levels. NASA was able to use this layer to hypothesize that as people transitioned to remote working, the quantity of air pollutants emitted drastically decreased, thus increasing air quality.


#### ***Changing Landscapes Layer:***
![Changing Landscapes](https://github.com/dhritiy/458Final_Essay/blob/main/img/Changing%20Land%20Scapes.PNG?raw=true)
*Caption:* One of the most interesting layers that NASA presented was through the use of their High-Definition Nightlights dataset. This data contains information of how much light is emitted from a variety of different energy sources and uses. As people began to travel, shop, eat out, and socialize less, there were much fewer nightlights. The darker purple and pink areas represent a lower number of nightlights, whereas yellow areas present an increase.


#### ***Climate Change Layer:***
![Climate Change](https://github.com/dhritiy/458Final_Essay/blob/main/img/Climate%20Change.PNG?raw=true)
*Caption:* NASA was able to use a similar thematic and base map as they used in the Air Quality layer to present a new idea in the climate change layer. Here they analyzed the decrease and increase in carbon dioxide levels at a global scale. Which most of Asia and the west is blue and saw lower CO2 levels, the area around Australia was a dark red. This area actually saw an increase in carbon dioxide levels due the wildfires that swept through Australia towards the end of 2019.

#### ***Audience and Use:***
The intended audience of this smart dashboard and the web maps it contains is the average internet user. NASA presents an easily accessible and readable dashboard and makes sure to clearly explain all of the data and scientific elements in relation to climate change. This dashboard could also be directed to people who are doing scientific research on the coronavirus pandemic and its impact on climate. For scientific research, this dashboard would only provide a basic starting point. In order to access more advanced materials and articles, the user would have to navigate to the Additional Resources part of each section. Here they will be directed to more in-depth NASA resources. By not presenting all of the in-depth data on the main dashboard, NASA ensures that they are able to easily convey their research to a casual and average viewer.

#### ***Web Mapping Elements and Interactivity:***
NASA made use of several basic mapping elements such as a scalar bar and legend. However, they never used a north arrow. Most of the time it was clear which way is north, but sometimes when they presented a zoomed in map of a region or an inset a map, a north arrow would have been very useful.
**Note:** The screenshots I pasted in this essay were of the full screen map itself. The web map on the dashboard has the legend and a description in a box to the right of the map which is not picture in this essay.

They also had several different forms of interactivity. For example, in the Changing Landscapes layer above you can see the horizontal slider in the middle of the map. As you move the slider to the right, you are able to see more of a map from an earlier time period (January 2020). As you move the slider to the left, you can see more of a more current map (February 2020). This element of interactivity allows the user to view multiple time periods on one map and perform more analysis.

They also had a tool to zoom in and out of the map. As you zoomed in very close into one country or city, you would be able to see more features of that location. For example, NASA displayed locations of different airports, their names, and denotated them with a plane marker in the Air Quality layer.

#### ***Authors and Data Sources:***
The majority of the data used in this dashboard was all collected by NASA through the use of the global satellite system. They were also able to gather some of this data by using scientific instruments that are on the International Space Station and also through some ground observatories. In order to further the analysis presented in this dashboard, the authors (NASA scientists), worked with the Japan Aerospace Exploration Agency (JAXA) and European Space Agency (ESA). By working with multiple agencies, they were able to perform a much deeper and more detailed analysis of climate change during the global pandemic.

The majority of this data is from January 2020 to the present, as this is the duration of the pandemic. However, at times NASA also used earlier data from 2019 in order to analyze change in patterns over time.



### **Systemic Architecture**
#### ***Client, Server, Services, and Data:***
The data used in this smart dashboard came from a variety of different sources and in order to compile and power it, NASA used an API. This was an open-source API that was specifically created as "lightweight tile server" for coronavirus related data. The file format that they used for their data were GeoTIFFs. This is a raster-based format and since it is cloud supported, it allowed for NASA to create a more advanced web application.

In order to manage the data flow and set up the environment for the web page NASA used node.js and Yarn which is a packaging manager. Then they created three different environments: local.js, staging.js, production.js. Essentially, they started with local.js to begin any development that needs to be done locally. Then they would use the staging file server. Finally, when the production file server is created, it overrides the other two.

One of the interesting things with data flow here is that the dashboard uses live reload. As NASA collects live data and inputs it into its database, that data is then processed and presented to the client on the smart dashboard. The website that hosts this dashboard makes use of http://localhost:9000/. Then whenever the system notices a change in the data files or executes a new task, the webpage will refresh.


### **UI/UX and Web Mapping Critique**
#### ***Pros:***
One thing that really stood out as a positive for this dashboard was NASA's use of different basemaps for different thematic layers. Often times, creators of smart dashboards will use the same basemap in all of the web maps they are presenting. However, NASA used a variety of basemaps. For example, in some web maps they used a Grayscale basemap which allowed the reader to be able to clearly see the data NASA was presenting. They did this mainly when they were presenting a choropleth or density thematic layer. In others, where it was important to understand the urban geography of the region, NASA used a Satellite basemap. By doing so they were able to present their narrative in an informative way and still allowed the viewer to easily and quickly comprehend the data.

Additionally, another pro of this smart dashboard was its responsive web design. The images, web maps, and layouts of the different web pages were all very flexible and they rendered very well on screens of different sizes. As I moved the below indicator dashboard from my laptop, to my larger monitor screen, the size of the map expanded to fit the width of the screen. The Insights text on the right also automatically enlarged and so did the graphs to better fit the height of the screen. The smart dashboard was also responsive when I accessed it my mobile device. Many dashboards usually struggle with have a cohesive and understandable mobile design. But the NASA earthdata dashboard made use of a variety of different hamburger menus to aid with navigation. This allowed me to view the map and then collapse it and navigate to a different indicator. When I toggled on a new indicator, the dashboard would automatically bring up the corresponding web map.

#### ***Cons:***
One critique, I have for this dashboard is the way in which climate change indicators were presented. As you can see in the image below, I chose to use the dashboard to show the Agriculture indicator in Beijing. Here NASA is aiming to present the global changes and performance of food access and supply flows. From this web map, I can only see that there is an area in Eastern China that is performing at the Exceptional level on the agriculture scale and the rest of China seems to have no data. This was an issue at that I saw with many of the indicators. As a suggestion, rather than showing a map of China that mainly has no data, I would have the basemap automatically zoom into the area that is green and exceptional. Here, in the dashboard Insights text on the right, I would explain that this area is exceptional. But then I would also reclassify this Agriculture indicator to show the different level of exceptional food supply flows in this region of China.

Additionally, another con I see with this map is that there is no search bar. This makes it hard for the user to navigate through the dashboard or web maps to find the topic that they are looking for. If the user could type in a location on climate change indicator they are interested in and immediately see all of the places this smart dashboard writes about that topic, they would be much more inclined to use it.

***Indicator Dashboard:***
![Climate Change](https://github.com/dhritiy/458Final_Essay/blob/main/img/Critique.PNG?raw=true)

### **Connection to Social Theories:**
This smart dashboard connected very well with the article by Joel Shapiro, [*3 Ways Data Dashboards Can Mislead You*](https://hbr.org/2017/01/3-ways-data-dashboards-can-mislead-you#). In his work, Shapiro explains what he calls the "Causality Trap". Essentially when a viewer sees two attributes being compared and linked with another on a dashboard, they tend to assume causality in between both. While there may be a correlation between the data they are viewing, there is a high chance that they can mistake correlation for causation.

This is related directly to the NASA dashboard, because just from looking at the first few web maps and dashboards, the average viewer may likely assume that the pandemic had a positive impact on climate change. However, once they actually scroll through several on the web maps and read the insights NASA makes sure to point out that some climate indicators cannot be attributed to human changes in activity. While they do share this information, it is not readily available on the main page or even the first few dashboards the viewer is likely to click through. Therefore, if the viewer is a casual reader and just spends a small amount of time on the smart dashboard, they are likely to fall for the "Causality Trap".

Furthermore, the digital divide can also have an impact on people who use this dashboard for research purposes. For example, when you read through the open-source code and GitHub repository for this web site, you are able to see that this dashboard is not complete and refreshes automatically. However, due the gap in access to technology, many people may not be aware that they have to read and understand such background information. Therefore, if a student without much access to technology was to go to the library, access this smart dashboard, and use it as the basis for their research they may present incorrect information. Chances are the data the student collected and the analysis they read has likely changed and their initial data gathering could now be false.

While the NASA Earthdata COVID-19 dashboard is a very informative and useful resource, I would urge that a user view it as a living document. They must understand that it is live and updates and refreshes on its own. They must also make sure to note that they take the data at face value and can attempt to make and find correlations, but cannot use it to prove causation.


**Author:** Dhriti Yandapally
**Professor:** Bo Zhao
**Class:** GEOG 458
**Date:** 12th March, 2021


### **References:**
\* Dashboard: https://earthdata.nasa.gov/covid19/
\* Dashboard GitHub Repository: https://github.com/NASA-IMPACT/covid-dashboard
\* Class Reading: https://hbr.org/2017/01/3-ways-data-dashboards-can-mislead-you#
