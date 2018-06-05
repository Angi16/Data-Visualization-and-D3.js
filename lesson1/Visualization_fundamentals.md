**Introduction:**

Data visualisation is used to explore patterns in data and  represent visually some underlying data using things like color, size, shape to ultimately convey their information or some insight.
		
Basedon the purpose of the data visualization we can draw a distinction between the exploratory and the explanatory - Where in exploratory we try to get relevant information from data and after we get the analysis, we share our insights in the Explanatory.


**Explanatory itself can be divided into further five steps:**
1. Target our audience - If we have public audience, we want to make a visualization that caught general attention
		         - If we present it to other scientists, we want to make more scientific approach
  2. Choose what kind of plot or graph is optimal to communicate our findings to our targeted audience. Use colors and annotation.
  3. Then eliminate the content that not worth adding.
  4. Then move the position of our plot accordingly. When they enter our page, what are the first visualization do they see, and what's next in order. 
  5. Make it a narrative story.
  
Now, whether we come from background that takes coding, design, or communication. It takes all of these three background to make a great visualization.

![](ImagesL-1/f1.jpg)

Thus, Data Visualization takes a greater part in Data Science. In Data Science, we wrangle the data, make an analysis from it, and then perform the visualization.

Data Visualization Process:

Part -1 : Wrangling and munging. we wrangle data, from multiple resources. It can  come from other website through API, scrapping data,users' log, database or loading some mapreduce pipeline.

Part -2 : Here we perform some Exploratory Data Analysis, maybe some statistical or mathematical theory implemented, to get insight of the data.

Part -3 : Here we make the visualization. We share insights of the data that we have by choosing different plot that most effectively explain our insights.

Part -4 :  we make the narrative story in a way to achieve Human Computer Interaction.


**Difference between Exploratory and Explanatory:**

In the exploratory section, it's us and our data. We make scatter plot, histogram, or boxplot that best repsents the insight that we want to learn.
In the explanatory section, it's us and our audience. We repsent in the most interesting way that your reader could get through.

**IMPORTANCE OF VISUALIZATION:**

![](ImagesL-1/f2.jpg)

We shouldn't simply rely only on the summary statistics of our data. 
For example, on the left of above figure we have dataset for x, y representing  mean,correlaction coeffecient, line of best fit, standar deviation and so on. When we plot it for the visualization as in Right Figure, We get better insights of our data.
To depict importance of visualization following graph shows how our brains process insights faster significantly by  visuals:

![](ImagesL-1/f3.jpg)

When we see through our eyes, we proceeds faster and become more aware. Take a look at the Edwards Tufte's explanation and Penn researchers of how powerful visuals and eye in the human brain.

Below graph is the visualization of the Health care data from Hans Rosling, take a look at "this" youtube video.

![](ImagesL-1/f4.jpg)

So, the above graphs shows different data types - 
**Quantitative data**- that can be usede to do the computations, like income per person, life expectancy, total population etc.
**Time Series data**- that range from (day,month,year,etc), 
**Categorical data**-Nominal data, for example, geographic data(Indonesia, China,Italy, etc). 
**Ordered series data**- that take categorical but still ordered data. Example- class of difficulty level of beginner to advanced, or categorical bucket from 100 million,200 million,..., > 500 million.

Now we take a look at following graph from Hans Rosling's Health care data :

![](ImagesL-1/f5.jpg)

Now we try to find out different data types:

![](ImagesL-1/f6.jpg)

so we see that-
Spending per person and life expectancy can be moved as quantitative data, data that we can take computation.
While doctor visits, as explained, has been divided into categorical ordered bucket
Then, has or hasn't health care is just yes/no categorical.

##VISUAL ENCODINGS:

![](ImagesL-1/f7.jpg)

Visuals Encodings means how we map data to visuals.
we see here that each of the variable fall nicely to the type of data. This is multi dimension of data. 
3D graph is difficult to perceieved than 2d graph, because we may have ambiguous perspective.

So the way to do this is set another visuals that can add 3d dimension, which we can find in any of these Retinal Variables:
![](ImagesL-1/f8.jpg)

Saturation is difficult to differentiate with human eyes. So we can avoid that.
There is also time series in the graph that is represented as frame so it animates nicely when it's being played on.
![](ImagesL-1/f9.jpg)

BY looking at babove visualization we find out following visual encoding basis for variables
![](ImagesL-1/f10.jpg)

again we go through following example of visualization and find out what are the visual encodings for variables
![](ImagesL-1/f11.jpg)

solution:
![](ImagesL-1/f12.jpg)

**Ranking of visual encodings:**
If you plot multiple dimension of data, prioritized them in order, then you want to take 2 of most important variables as position and the rest as the other kind of retinal variables.

##Decomposing Visualizations

Decomposing visualizations is like a reverse-engineering for software. You want to know what the graph consists of and how it is effectively represented in a way showing their insights.Take a look at data visualization performed "by Nelson Auner, Making Indonesia"

He has recreated the work of Hans Rosling, we can see that similar to Hans Rosling, making time series as a frame we can play and animate towards the end. 

The positions are: % foreign investment as x axis and female employment as y axis, both are quantitative data.
Output as color saturation from blue to red, and the number of firms as the size of the circle, as quantitative discrete data. All of these circle are categorical from every sector of the job.
![](ImagesL-1/f13.jpg)

Let's take a look at Facebook Offering, we can find the link "here". We see that the first thing that it does is the title. It's important to create a title that makes the readers focus on the thing that data visualization want to say. In this example, The visualization makes double encoding, to emphasize more on the variables. the y position and size describes the company value, while x position and color describe time-series year of I.P.O.

![](ImagesL-1/f14.jpg)


#Spectrum of Visualization technologies

For the Data Visualization in the internet, D3.js by Javascript relies on the programming language of the assembly level, like html,css,svg.Because it's the lowest level, it's really efficient, flexible, but hard to develop with.

![](ImagesL-1/Q1.jpg)

D3.js is like the level of C++ complexity, where you pretty much encapsulate everything that needed for data visualization.

In the higher level, there's NVD3, Dimple.JS, Rickshaw that build on top of D3.js. Its scripting level is like Python or Ruby. But it get's lower flexibility like D3.js, and tailored for specific cases, like Rickshaw.

On the top level of spectrum, we have Chartio. It's a library  like tool, encapsulated from programming, and can be use for 90-95% cases. It builds dashboards and charts.

It's important to note this spectrum level of software. There's a trade off between the flexibility and effortless. We can stay away from the path that Chartio uses to have more flexibility but build time slower, or the other way around. From your data science project, we may want to think about how much data visualization impact in your project, and choose whichever library based on the tradeoff.

![](ImagesL-1/f15.jpg)

#D3: Data Driven Documents

Data is what usually refer to, in format like json or xml. The Documents itself is the source file(html file) that we want to parse on. So D3 is "Drive the Data towards Documents". During  page load, fetching html file from web server, DOM is created.DOM is Document Object Model that built based on parse html file from the server. DOM can be parsed by other programming languages, like Python or Java. D3 is built on top of Javascript API, which is built to the DOM, that later drive to the Documents. DOM is specification, a hierarichal object, from the root of tree that build the model.

![](ImagesL-1/Q2.jpg)

D3 has many advantage. D3 can encapsulate visualization from the mechanics. D3 code can generate its own html file and svg objects, so designer can build on top of this and ask the developers if it need to custom more visualization.D3 can manipulate its html file and nodes.
![](ImagesL-1/f16.jpg)

Javascript itself can provide some interactive visualization on the client side, while keeping static on the server side, so D3 can be benefit from it.For developer, they can use Javascript libraries, text-editor,speedup performance of the Documents, or other thing that already advantage of Javascript.