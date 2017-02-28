---
layout: post
title:  "Is the flu really worse this year? Comparing across using using CDC data"
date:   2017-02-28 09:28:00 -0500
categories: R 
---

I was sick last week, and I think I might have had a mild case of the flu. Since it seems like a lot of people have been sick, I was curious whether the flu was really worse this year than last... and since the CDC makes the data available for each year, I put the data together and created a GIF. The measure of flu activity is from minimal (1-3) to high (8-10) and the scale in the chart is the difference from the 16-17 and 15-16 flu seasons (which range from November - March; it ends in week 7 because that's the most recent data for this year.

![flu](https://cloud.githubusercontent.com/assets/4596214/23408837/7cb56b9e-fd97-11e6-817d-a9dd743b532e.gif)

The data is from [this CDC page](https://www.cdc.gov/flu/weekly/fluviewinteractive.htm).

I used the new (and in-development) [gganimate package](https://github.com/dgrtwo/gganimate) to create the GIF. The basic idea is to create a `ggplot`, and then add an aesthetic for the `Frame`, which represents the change between frames in the plot, which in this case is the week.

This project is just a first attempt but the code for it is available in [a GitHub repository](https://github.com/jrosen48/cdc-flu-vis).
