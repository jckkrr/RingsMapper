RingsMapper
A script that plots growth-rings across map-like scatter plots; the grwoth-rings represent a change in value (such as a shift in airport traffic) over two periods.

![newplot(4)](https://user-images.githubusercontent.com/69304112/133867248-512d56e8-4dc5-49ce-94a1-413e7ad356ab.png)

# How it works

At each location, an unfilled marker (a thin, dark ring) is drawn based on the initial value for that location (colA).

It then calculates where the ring for the second value would be (colB) - though does not draw it. 

The position of a mid-ring is then calculated. For this mid-ring, another unfilled marker is created. This time, however, the width of the ring (the marker_line_width) is the difference between the two value's (real and imagined) rings. This fills the space between the two value rings neatly.

Therefore, where there has been growth, the ring increases in size; where there has been contraction, the 'fill' goes inwards.

Each set of rings (initial and midpoint) follow the same color scheme - green for growth; red for reduction - though the growth ring is at a lessened opacity.

This script accepts any dataframe containing longitude and latitude (or x and y) values plus two columns of size values. A 'name' column is also required by the hover text.

Graphing is done in Plotly (GO).

# Examples

In this instance, a map of Autralian airport cooridinates has been used, with airports selected and values generated at random. 

It includes an underlayer that plots (with small dots) each airport in the country.

![newplot(5)](https://user-images.githubusercontent.com/69304112/133867509-b4626711-9af3-47ef-bc72-4fb54cc337ae.png)
