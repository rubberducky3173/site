**Lab 5- Food and Land Use**

Welcome back to my blog and to the final lab assignment of the year :( However, I’m 100% this isn’t the last data analysis I’m ever going to do. Plus, this assignment is important to me and probably important to read. So let’s jump right in!

**The Question: How much land does every person on the planet use for food?**

I've wondered for a while how much impact we actually have on the environment for our food. Many of us don't know about what's happening or realize how the bad feelings of negative impacts taper off as they move further away from us. I aim to generally quantify individual impact here,

![farmland](https://github.com/rubberducky3173/site/blob/master/assets/img/farmland.jpg?raw=true)

I got my datasets from the Food and Agriculture Organization and The World Bank!

**The Process**

Firstly, I imported pandas to read the datasets and Altair to visualize the data. Then I started sorting through the land dataset first. I would need to see how much land is being used to make food each year. Using .loc and .isin, I was able to isolate the global land for every year then isolate global land only being used to produce food- agriculture and cultivated meadows/pastures. I excluded the rest of the categorizations for land because there were overlaps. 

![lab5imports](https://github.com/rubberducky3173/site/blob/master/assets/img/lab5imports.PNG?raw=true)
![lab5land1](https://github.com/rubberducky3173/site/blob/master/assets/img/lab5land1.PNG?raw=true)

Next, I used .groupby() and .sum() for the “Area” (which is the World) to get the food total for land globally each year. I then deleted unnecessary columns that were not years or land amounts. 

![lab5land2](https://github.com/rubberducky3173/site/blob/master/assets/img/lab5land2.PNG?raw=true)

I ran into a problem right after- the years were all in one row; not in columns. I needed to find a way to swap columns and rows in order to make a visualization. Luckily I found a solution online, which was converting my data to a DataFrame and then using .T and .reset_index() to create a column that I can use for my x-axis. I created a bar chart where the x-axis is years and the y-axis is the land usage in 1000 hectares:

![landuse](https://github.com/rubberducky3173/site/blob/master/assets/img/landuse.PNG?raw=true)
Our usage is quite impressive for our population (which I will talk about soon.) We can see how a generally similar amount of land starting in 1961, which is about 4.5 billion hectares, can support a much larger population in 2020 with a little less than 5 billion hectares. This is because of food innovation and being able to grow more for the less or same.

I analyzed the population dataset after. I used similar processes that I did with the land usage dataset. Luckily I was able to reuse the “World” category to get the global population per year with .isin and .loc. I used .sum to get the total for the year and deleted columns 2022, 2021, 1960, and ‘Unnamed: 67’ to match the years with land (1961-2020). 

![lab5population1](https://github.com/rubberducky3173/site/blob/master/assets/img/lab5population1.PNG?raw=true)

After that it was simple from there; I used DataFrame and .reset_index() to prepare my data for the chart because the years were also a single row just like the land dataset. The chart’s x-axis was the years from 1961 to 2020 and the y-axis was the global population. As one can see, the population increases quite quickly by jumping from just over 3 billion in 1961 to nearly 8 billion in 2020. We hit 8 billion this year even though it’s not shown because the datasets match only from 1961 to 2020. 

![lab5population2](https://github.com/rubberducky3173/site/blob/master/assets/img/lab5population2.PNG?raw=true)
![population](https://github.com/rubberducky3173/site/blob/master/assets/img/population.PNG?raw=true)

I next prepared my data to get the “per person” numbers. I concatenated the global land production to my population datasets as “Per_Person” so I was able to divide the land by the population per year, as shown below.

![lab5concat](https://github.com/rubberducky3173/site/blob/master/assets/img/lab5concat.PNG?raw=true)

So here I am with the land usage in 1000 hectares per person globally each year from 1961 to 2020. I wanted to get it in hectares and square feet, so I multiplied the numbers by 1000. Then, to get it in square feet, I multiplied by 107639.104 because that’s the square feet equivalent of a hectare. 

![lab5perperson](https://github.com/rubberducky3173/site/blob/master/assets/img/lab5perperson.PNG?raw=true)

I finally created a chart using years as the x-axis and the products as the y-axis. We can see that the values go down over time because we’re distributing generally the same amount of land for food to a larger number of people. We were at about 155,570 square feet of land per person in 1961, but in 2020, we were at about 65,700 square feet of land per person.

![perperson](https://github.com/rubberducky3173/site/blob/master/assets/img/perperson.PNG?raw=true)

**Discussion**

A lot of struggles I had came from syntax and troubleshooting through messy datasets little by little. But with help from my teacher and the internet, I was able to get what I needed.  Something else to note is that the population and the land usage numbers are all estimates and how it’s impossible to accurately count everything. I also did not count the ocean in this dataset because agriculture takes place on habitable land while we do not live in the ocean (yet?). This is from 1961 to 2020 because some data were not available yet and the land use only spanned from 1961 to 2020, not 2023.

The results made me think of how more people are getting less (just by this dataset.) However, I realized that there are hundreds of millions of people that are affected by hunger, nearly 10% of the world. In addition, the people in the top percentage of income consume a lot more food than the rest who can afford food. That means their “land usage” is a whole lot higher than the others. So it’s important to know that my charts are showing if there was an equal distribution for everyone, while in reality, the distribution is VERY unequal. We need a lot of land to feed a lot of people. We already use half of habitable land for agriculture. 
About 17% of food available at the commercial level for consumers is actually thrown away yearly. This is more than 900 million tons each year and plenty of land. Just think about how many people we can feed if we redistributed the food instead of trashing it! There honestly is a lot I can say about this in relation to climate change and food security and societal inequalities. To keep feeding our growing population, we have to look at crop calories and agricultural expansion but also keep in mind sustainability. I aim to take a look at a lot of these factors.

This was immensely fun and in my opinion, helpful to visualize and important to spread. Over the past year I’ve learned so much on how to sift through data and now see the world in a different way. I’m looking forward to continuing my data/computer science interest in the future!

Thank you for reading!

