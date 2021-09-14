**India is a founding member of an alliance which has potential to become very important in
future and i.e International Solar Alliance(ISA) in which India has the motive to make a unified solar
power grid for the whole world under ‘One Nation One Grid’. Not only solar but India is also doing a
great job of increasing power generation depending on other renewable sources. Renewable Energy
Sources(RES), including carbon-neutral sources such as solar, wind, hydro/water, geothermal, etc., is
useful energy obtained from renewable resources which are naturally replenished on a human time
scale. In this report, we are going to analyze different types of RES in India and how states are coping
with RES for their power generation. What is India’s plan for RES in future as a founding member of
ISA? We have located different types of power plants both conventional and non-conventional in
India. We have also found that states with newly developed energy plants and with difficult terrains
have more renewable energy generation as compared to others. Hydel energy has great numbers
followed by Solar and Wind. And, how’s India doing to achieve its target for Solar Energy Capacity
till 2022.**


Is India doing significant development in the renewable energy sector to become energy leader in the world?
The data found for current scenarios of energy sources and renewable to be precise from given links:
- All-India installed capacity of power stations till 30th november 2020 (https://npp.gov.in/public-reports/cea/
monthly/installcap/2020/NOV/capacity2-Western-2020-11.pdf) [1]
- List of Power stations in India (https://en.wikipedia.org/wiki/List_of_power_stations_in_India)
- Target for Solar Energy by 2022 (https://data.gov.in/resources/target-solar-energy-generation-2022-
ministry-new-and-renewable-energy)

‘ETEmergyWorld’ has energy sector-related news covered by Economic Times India. On 11th of December
2020, it published news that India added 764 Megawatts of renewable energy capacity alone in November
month! Especially wind and solar. For small hydro and biomass, it remains unchanged.[2]

Although nuclear power itself is a source of renewable energy, the material used in nuclear power plants is
not.[3] The strong energy in the nucleus of an atom is harvested by nuclear power. Via nuclear fission, the
process where an atom's nucleus breaks, nuclear energy is released. Complex devices that can regulate
nuclear fission to generate electricity are nuclear power plants. The element uranium is the substance that is
most commonly used in nuclear power plants. While uranium is present in rocks all over the world, a very
rare form of uranium, U-235, is typically used for nuclear power plants. A non-renewable resource is
uranium.

On 6 March 2019, the Union Cabinet approved a new hydropower strategy aimed at improving the industry,
including the status of renewable energy projects according to major hydropower projects. Large hydro
projects will now be designated as renewable energy projects, according to the new legislation. Only smaller
projects with a capacity of less than 25 MW have so far been listed as renewable energy. Large hydro
projects will be included as a separate category under the non-solar renewable purchase obligation scheme
with the abolition of this distinction. Power buyers would have to procure a portion of energy from major
hydro projects under this scheme.[4] As power generation through large hydro sources has disputable claims
to be a renewable source of energy. It has been put under the ‘Conventional’ source of energy in this report.

If one consumes it faster than it can be regenerated, biomass is not considered a sustainable resource.
Biomass coming from forests will increase carbon emissions as compared to coal and other fossil fuels.
There are majorly three energy resources which come under the category of “other renewable sources” like
small hydro energy, wind energy, solar energy and biomass energy. These sources of energy share very few
percent of total electricity production in India but are present in the significant amount.

India was the first country in the world to set up a Department of Non-Conventional Energy Resources
(Ministry of New and Renewable Energy (MNRE)) in the early 1980s, and India's Solar Energy Corporation
is responsible for developing India's solar energy industry through its public sector enterprises. The Ministry
of Power administers hydroelectricity separately and is not included in the MNRE goals.

This report will find the answers for the questions like, which states are doing more total power generation,
which states have more production of renewable energy resources, what different types of renewable source
of energy at what level are they producing in different states and which states have better renewable to total
energy production ratio.

**Analysis**

Breakdowns of analysis for above tasks have divided up into three segments. First, locating different kinds of
power plants in India. Second, Analyzing total power generation, renewable sources of energy capacity and
percentage of renewable energy to total energy capacity using choropleth maps in which we shade area state
wise. Also, stacked bar plots have been done for non conventional renewable energy resources including
small hydro, solar, wind and biomass. Thermal vs Renewable Energy stack bar plot has also been plotted.
And the third, for conclusion we plotted current solar energy capacity in India and it’s target till 2022.

a) Locating different Power Plants in India:
Data of locations for different power plants like coal-thermal, diesel-thermal, gas-thermal, nuclear, hydro,
wind, solar and biomass have been put into data frames with columns of States/UT names and coordinates of
those plants.
After that, data cleaning has been done like putting coordinates in a correct coordinate. Coordinate present in
both DMS(degrees, minutes & seconds) and DEC(decimal) format with directions. After taking decimal
format, latitude and longitude separated into two values in a single list and each list became the value of each
index in the data frame column of coordinates. A function has been created to convert all seven plant type
coordinates at once.
Now markers should have to be added on the map to locate power plants. Folium library has been used here
to add markers on the map. First, the centre of the map is India which is 21,78; the zoom level at which map
starts has set at four. For the tiles, the OpenStreetMap has been used as it is open-source and easily available.
Now, the folium.marker function has been used to locate markers and for the exact location, it has given the
coordinates in latitude, longitude form as parameters as inputs. Popup attribute used to give the name of the
plant at that particular location.
There has been a large number of datasets of power plants and placing each marker one by one would be a
very lengthy process, so iteration has been used to place all markers of a data frame at once.

b) Creating choropleth maps using Folium:
GeoJSON is an open standard format designed to represent, along with its non-spatial attributes, simple
geographical features.[5] The JSON format is based on it. The components include polygons of points, line
strings and multi-part sets of these kinds. In this report geojson file is used to cover Indian state shapes to fill
colours inside it.
State wise data of different power generation capacity in India used as basic dataset to plot maps here. Like,
total energy produced, sub-total of renewable energy and percentage of renewable energy to total energy.
Folium again used to plot choropleth maps. Center of the map is set to center of india (21,78) and the zoom
starts at four. Now, folium.choropleth function with parameters like, geo_data which is equal to states of
India GeoJSON file; name of the layer; data is used like data frame of the state-wise energy capacity in India
(thermal, nuclear, renewable and total). key_on parameter is used to make a common value of geojson and
state_data like name of the states which is ‘properties.st_nm’; fill_color, to give colour of the choropleth;
fill_opacity; line_opacity; legend_name of the layer.
HTML file is also generated for these choropleth maps.

c) Graphs plotting of different datasets:
Two stacked bar plots using matplotlib library of python have been created to display different attributes and
their total (as they are stacked). For example, a stacked bar of two attributes has been used to display thermal
and renewable energy generation in India to compare their values with different colour combinations. To plot
stacked bars, the bottom of the second bar is given the value of the first bar of that corresponding index.
Here, to plot the bar of renewable energy capacity, it’s bottom value is given as the thermal energy capacity
of the same state.

**Conclusions:**

More than 36% of power generation capacity comes from renewable energy sources which include large
hydro, small hydro, solar, wind and biomass. It means, India is doing a significant amount of development to
obtain energy from renewable sources.
Most of the renewable energy generated either from hilly states or coastal states. Coastal states in India have
capacity to produce large amounts of energy from winds and sun. Also, these states have good river systems
which give them water availability to build small as well as large hydro power plants. That is why states like,
Andhra Pradesh, Gujarat, Karnataka, Maharashtra and Tamil Nadu have larger numbers of renewable energy
capacity. Rajasthan also produces a huge number of solar and wind energy because of its large land area and
deserted terrain where winds speed is more and horizontal irradiation is better.
Most of the northern states generate electricity from thermal sources like coal (lignite), gas or diesel. They
have a huge capacity of electricity production but most of it only from thermal energy production. It makes
these states with least percentage of renewable energy source out of total energy source.
Northeastern states have the least number of energy capacity in india due to less development. They have
most of the source of solar only and depend on other states for generation. They have the best percentage of
renewable energy source out of total energy source but negligible as compared to other states. Bhutan also
provides energy in these states as India has helped bhutan in development of huge dams which also helps to
improve Indo-Bhutan relations and India’s image as energy leader in the world.[7]
India has overall great horizontal irradiation capacity by which it can increase it’s solar power generation
capacity. India has target of increasing solar energy capacity till 2022 upto 175 GW. [6]

**References:**

[1] “ALL INDIA INSTALLED CAPACITY (IN MW) OF POWER STATIONS (PDF). National Power
Portal, Ministry of Power, Government of India. Retrieved 11 December 2020.

[2] “India adds 764-MW renewable energy capacity in November 2020”

(https://energy.economictimes.indiatimes.com/news/renewable/india-adds-764-mw-renewable-energy-
capacity-in-november-2020/79681630)

[3] Dunn, Margery G. (Editor). (1989, 1993). "Exploring Your World: The Adventure of Geography."
Washington, D.C.: National Geographic Society.
[4] “Large hydro projects get ‘renewable energy’ status” - The Hindu.
https://www.thehindu.com/business/large-hydro-projects-get-renewable-energy-status/article26460181.ece

[5] Butler, Howard; Daly, Martin; Doyle, Allan; Gillies, Sean; Hagen, Stefan; Schaub, Tim (August
2016). RFC 7946. IETF. DOI:10.17487/RFC7946

[6] “Report of the Expert Group on 175 GW RE by 2022” – NITI Aayog.
https://niti.gov.in/writereaddata/files/175-GW-Renewable-Energy.pdf

[7] Chhetri, Pushkar (2010-11-10). “ADB Grants $21.6 M for Rural Electrification”. Bhutan Observer
online. Archived from the original on 2011-08-24. Retrieved 2011-11-29.
