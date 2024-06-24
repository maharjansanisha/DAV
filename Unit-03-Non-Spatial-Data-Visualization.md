# Unit 3: Non-Spatial Data Visualisation

## Visualization of One, Two and Multi-Dimensional Data

**Non-spatial data** is such kind of data that does not have any geographical location associated with it i.e. it can be number, text or image and can be used to describe people, events and things. This type of dat provides context and additional information about the spatial features and can be in form of alphanumeric values, numbers dates and so on. Some example of non-spatial data are names, phone numbers, email address, genders, prices etc. non-spatial data can be used in a variety of ways such as to build machine learning model, to make prediction, to improve decision making, to conduct statistical analysis etc. the non-spatial data can be used with spatial data to provide more meaning to the spatial data. For eg map of landslide affected area and earthquake affected area to understand the relationship between the two.

Non-spatial data visualization is the process of representing non-spatial data in a visual way to help user to understand in easy way. Visualization of non-spatial data can be done using charts and graphs (used to show trend, patterns and relationship of data), tables (used to show relationship between different variables in the data), heatmaps (uses color to show the distribution of data or highlight low or high values), tree maps (used to show the structure of a organization and relationship between different categories of data), scatterplots (uses points to represent the values of two variables in the data), word clouds (uses size of words to represent the frequency in the data and used to show the most important words in a document), bar charts (used to display categorical or discrete data using a bar and height of bar corresponds to the value of category), pie chart (use slice of pie to show composition of whole), line chart (used to display trend over time), box and whisker plot (used to show summary of statistics of a datasets including median, quartiles and potential outliers).  
For effective non-spatial data visualization following terms should be considered:

- Use color and shapes that are easy to distinguish from each other
- Use a legend to explain the meaning of each color and shapes
- Use labels to identify the different parts of the visualization
- Use consistent style throughout the visualization.

In data visualization, dimension refers to the number of variables that are being represented in data.

**One dimensional data** also known as **univariate data** that consists of a single variable or attribute for each data point and can be represented along single axis. For example, a list of numbers or a time series, daily temperatures for a specific location over a year etc. Visualization technique used for one dimensional data are histogram, bar charts, line charts, box plot.

**Two-Dimensional data** is such kind of data that involves two variable or attributes for each data points and each data points is represented by a pair of values. Two-dimensional data can be represented along two axes. For example: scatterplot showing height vs weight, heatmap showing correlation between data etc. some visualization technique used for two-dimensional data are scatter plots, bubble charts, heat map etc.

**Multi-dimensional** data also known as multivariate data are such kind of data that have more than two variables or attributes for each data point i.e. can be thought of as data with three or more dimensions and represented along three or more axes. For example, ecommerce datasets with variables like product category, price, customer rating and sales volume, climate data with variables such as temperature, humidity, wind, speed recorded at different locations and times. Some visualization technique used in multi-dimensional data are 3D scatter plots, ternary plots etc.

## Tabular Data

**Tabular data** is such kind of data that is organized in form of row and column which are used in data analysis, reporting and decision making. Each row typically represents a single data entry or observation while each column represents a specific attribute or variables associated with that data. Some visualization technique used for tabular data are line charts, bar charts, heat map scatter plots and tree maps.
For visualization of different dimension of data following factor should be consider:

- The number of dimensions of the data
- The goal of visualization
- The user for the visualization

## Why do you need data tables

Human eyes are drawn to patterns and blocks with specific padding. So data tables engage people with the cells, rows, and columns separation.
We can list lots of benefits of data visualization in tables.

- Organizing dynamic data types
- Data correlation is clear
- Rows and columns
- Merged table cells
- Sticky header or column
- Smart info distribution
- Multiple sets of related data
- Compare data
- Condense info

A data table, or a spreadsheet, is an efficient format for comparative data analysis on categorical objects. Usually, the items being compared are placed in a column, while the categorical objects are in the rows. The quantitative value is then placed at the intersection of the row and column, called the cell. The following examples demonstrate data tables.

## Scatter Plot

It is a data visualization technique used to show the relationship between two continuous variables and are useful for identifying patterns, trends and outliers in the data. The data for each point is represented by its horizontal (x) and vertical (y) position on the visualization. It shows linear relationship (such relationship between two variable that can be represented by a straight line for example: height and weight of a group of people), non-linear relationship (such relationship between two variables that cannot be represented by a straight line. For example, price of stock over a time), correlation (used to measure strength of relationship between two variables by looking at how closely the points are clustered together) and outliers (data points that are far from each other. This can be shown by scatterplot by looking for a point that are much farther away from the rest of the data points). To create effective scatter plot flowing factor should be consider:

- Choose right variables
- Use appropriate labels and title to describe variables
- Use legend to describe each points, shape of points and colors
- Add annotation to highlight important features of the visualization

## Histogram

It shows the distribution of a datasets i.e. display the frequency or count of data points falling
into specific intervals known as bins. It is useful for identifying patterns, understanding the
spread and shape of data. It is like a bar graph in which the bar represent the number of data
points that fall within the certain range of values and the height of each bar represent the
frequency of the data points in that range. To create histogram, number of bins should be
determined first (bins are the range based on which count to be made like within rang of 10,
20, 5 etc.), appropriate labels and titles, consistent style, add legends and proper annotation.
Histogram works with only one variables.

**Plotting histogram to show distribution of sepal width of all species:**

```
plt.hist(flowerData.sepal_width,edgecolor='black',color='green',bins=5);
plt.xlabel("sepal width");
plt.ylabel("range");
plt.title("distribution of sepal width for all species")
```

## Bar chart

It is used to represent categorical or discrete data and display data using rectangular bars or
column. The height of each bar represents the frequency associated with a specific category.
Bar charts are specially used for comparing the values of different categories over time,
comparing values of a category across different groups. To create effective bar chars first
categories of data should be choosen, appropriate label and title should be used to describe
each coordinate, proper legend should be used to convey meaning of color, shapes and sizes
of the bars.

**Creating bar chart using seaborn library**

```
sns.barplot(data=flowerData,x="species",y="petal_width")
```

## Heat Map

Heat map uses a color to represent the values of data. It is used to visualize two-dimensional
data. It contains matrix where cells are colored according to the values of the data. The
warmer colors represent higher values and the cooler colors represents lower values. Heat
map represent data in a tabular format where individual values are depicted as colors which
is useful for finding out patterns, trends and relationship in two-dimensional data. It shows
correlation between variables. To create effective heat maps, first proper colors should be
choses, add proper labels and titles, add proper legend and annotation

```
sns.heatmap(flowerData.corr(), cmap=’coolwarm’)
plt.xlabel(‘x-axis labels’)
plt.ylabel(‘y-axis labels’)
plt.title(‘heatmap example’)

```

## Box Plot

A box plot or box and whisker plot is used to show the distribution of data in a five-number
summary: the minimum, first quartile (Q1), median, third quartile (Q3) and a maximum. It
represents central tendency, spread and the presence of outliers. Box represent the
interquartile range which spans the 50% of the data. It contains a horizontal line that shows
the median of data and the top and bottom of edges of box represent the first quartile and
third quartile of the data. Whisker extends from the box to minimum and maximum values
within a defined range. Data points beyond whiskers are considered as outliers. Outliers are
data points that falls outside of whiskers and are represented as individual point or dots.

```
sns.boxplot(data=flowerData,x='species',y='sepal_width')
```

## Tree Data Visualisation

Tree data is a type of data that is organized hierarchically with each data point having one or more
parent data points. Tree data can be used to represent a variety of real-world structure such as
organizations, product hierarchies and family trees. The data points are organized in a tree like
structure with each data point having one or more child data points. The root is the topmost data
point in the tree and it has no parent data points. The child data points are its immediate
descendants. Visualizing tree data can help reveal patterns, relationship and structures within the
data. Some of the visualizing technique used for displaying hierarchical data are tree maps,
sunburst chart etc. key components of a tree data structure are:

Root nodes: the topmost node which serves as the starting point for traversing the
tree and it has no parent

- Child node: a node that is directly connected to another node and is one level below it in the hierarchy. A node can have multiple child nodes
- Parent node: a node that has one or more child nodes. It is one level above its child nodes
- Sibling: nodes that share same parent node are siblings
- Leaf node: a node that has no child nodes i.e. it is a terminal node at the end of branch.

The tree data structure are used to represent hierarchical relationship and organizational
structure.

Visual Heirarchical Data:

1. **Treemaps:** it uses nested rectangles to represent the hierarchical structure of tree
   data. The size of each rectangle represents the value of the data point it represents. It
   is done in python my using plotly library. Following program shows an example on
   treemaps.

**Step 1**: Import plotly.express as px  
**Step 2**: Create data set or import dataset  
**Step 3**: Use plotly.treemap(dataset, path, values,color)

Here dataset is the actual data for which tree map is to be created, path indicates list
of columns name or column of rectangular data frame defining hierarchy of sector
from root to leaves. Values is either a name of a column or pandas’ series and such
field is used to set values associated to sector. Color are used to assign appropriate color pallet

**Treemap by creating own series of data**

let’s create two series (array) using pandas: first one is name of people and second
one is name of parent for corresponding name of people. Import plotly.express as pl

```
res=pl.treemap(names=["Ram","Sam", "Hari", "Gita", "Sita", "Ramila" "Pawan",
"Riya", "Sarmila"], parents=["", "Ram", "Ram", "Hari", "Hari", "Ram", "Ram", "Pawan",
"Ram"])  res.update_traces(root_color='lightgrey')  res.update_layout(margin = dict(t=50, l=25, r=25,
b=25)) res.show()
```

**Treemap for tip data sets**

```
import plotly.express as px
import seaborn as sns
#load dataset
df=sns.load_dataset('tips')
#plotting treemap
fig=px.treemap(df,path=[px.Constant("all"),'day','time','sex'],values='total_bill')
fig.update_traces(root_color="lightgrey") # to put color in root
fig.update_layout(margin = dict(t=50, l=25, r=25, b=25))
fig.show()
```

## Text and Document Data

Text and document data are a type of data that consists of text and other unstructured data which are difficult to visualize. Text data refer to textual information and documents that can be in various formats such as plain text, pdf, word document etc. Text visualization involves techniques for representing and visualizing textual information and document in a way that helps users to understand and gain insight from data. Text data can be from various sources such as articles, books, customer review etc. some visualization technique used for text visualization are word clouds (display the most frequently occurring words in a text. Used to identify frequently mentioned terms in documents), bar chart and histogram, network diagram, heatmaps, time series plot (shows specific text segment by highlighting and annotating document or articles). Some characteristics of text data are unstructured, diversity, volume, variety etc. Here we consider visualizing the text within a document, and collections of documents which are likely related (corpus).

Difficulty in analysis includes the loose structure, varied vocabulary, and optional metadata such as author(s), date, modification dates, comments, keywords, catalog codes, citations.

Levels of text to be represented:

**Lexical level** -- Simple grouping of characters into "tokens" which are typically words, but word stems, phrases, word n-grams and character n-grams may be beneficial
**Syntactic level** --Parsing purpose of token, grammatical category, tense, plurality, in the context of the phrase, sentence and paragraph
**Semantic level** -- Extract meaning of the syntactic structure with the tokens using fuller analysis of the context.

Text visualization is a visual way of presenting information—word clouds, graphs, maps, timelines, networks and more, can all be used to visualize text data. Doing so provides a brief understanding of the most important keywords, and sums up and communicates trends and frameworks within a specific text.

Text visualization is the technique of using graphs, charts, or word clouds to showcase written data in a visual manner. This provides quick insight into the most relevant keywords in a text, summarizes content, and reveals trends and patterns across documents.

Companies use text visualization to:

- **Summarize large amounts of text**: Automatically highlight key terms in a series of texts, and categorize text by topic, sentiment, and more, saving hours of reading time. How long would it take you to read 500 online reviews? With a word cloud or data visualization dashboard, you can understand text data at a glance.
- **Make text data easy to understand**: The human brain loves visual data. In fact, we are able to process images much faster than text. Text visualization is an effective way of simplifying complex data and communicating ideas and concepts to team managers.
- **Find insights in qualitative data**: Customer feedback holds a trove of insights. Through text visualization, you can get an overview of the features, products, and topics that are most important to your customers. Learn what their pain points are and what you’re doing right.
- **Discover hidden trends and patterns**: Analyze and visualize insights over time to detect fluctuations, and quickly find the root cause.

Text is maybe the most underrated element in any data visualization. There’s a lot of text in any chart or map — titles, descriptions, notes, sources, bylines, logos, annotations, labels, color keys, tooltips, axis labels — but often, it’s an afterthought in the design process. This article explains how to use text to make your visualizations easier to read and nicer to look at.

**Show information where readers need it**

1. Label directly
2. Repeat the units your data is measured in
3. Remind people what they’re looking at in tooltips
4. Move the axis ticks where they’re needed
5. Emphasize and explain with annotations

**Design for readability**

1. Use a font that’s easy to read
2. Lead the eye with font sizes, styles, and colors
3. Limit the number of font sizes in your visualization
4. Don’t center-align your text
5. Don’t make your readers turn their heads
6. Use a text outline

**Phrase for readability**

1. Use straightforward phrasings
2. Be conversational first and precise later
3. Choose a suitable number format

**Why Do We Need Text Visualization?**

Text Visualization can help reveal your audience’s thoughts You can use the chart to understand your audience’s feelings about a topic/situation. Besides, you can leverage the chart to summarize data-driven views. The chart can help you summarize the market feedback using first-hand data.

**Quick and informative**

You can easily get live feedback from your audience in real-time

**Exciting and emotional**

The chart can help audiences feel part of your data story.

**Engaging**

The Word cloud is incredibly engaging and visually appealing to many audiences. The chart can be an icebreaker or an entry point for a topic of discussion.

**Word Clouds are visual**

Our brains process visual content 60,000 times faster than texts and numbers. This provides a logical rationale for using the Word Cloud generator to analyze your textual data for actionable insights.

**Creating a text visualization is straightforward**

Generating text visualization examples is easy to follow. Yes, you read that right. Besides, the chart can provide you with insights into large data sets.

**Text Data Visualization Examples**

**Word Cloud**

Word Clouds are charts that display insights into qualitative data frequency.

The visualization design gives greater prominence to words that appear more frequently in a source text. The larger the word, the higher its frequency. You can use the chart (one of the text visualization examples) to perform exploratory textual analysis by identifying words that frequently appear in a set of interviews, documents, or other text.

**Tag Clouds**

Tag clouds or text clouds are ideal if your goal is to pull out the most pertinent parts of textual data, from blog posts to databases. You can use the tag cloud as a text visualization tool to compare and contrast two different pieces of text for similarities and differences.

**Slope Chart**
Slope Charts show transitions, changes over time, absolute values, and even rankings. Besides, they’re also called Slope Graphs.

Slope Graphs (one of the text visualization examples) can be useful when you have two time periods or points of comparison and want to show relative increases and decreases quickly across various categories between two data points.

**Sankey Chart**
A Sankey Diagram visualizes “a flow” from one set of values to the next. The two items being connected are referred to as “nodes.” The connections are labeled as “links”.

**Text Visualization is Useful for:**
Condensing a lot of content. Cut down on time spent reading by emphasizing central phrases across multiple texts, grouping content by topic, sentiment and more. Could you imagine having to get through hundreds of client reviews? With a word cloud or bar chart, you can visualize data and instantly make sense of things.

**Simplifying text data**: Our brains are wired to enjoy and make sense of visual data and it’s proven that we sort through images quicker than we do with the written word. If you’re looking to simplify complex data and transmit those concepts to team managers, then text visualization is the way to go.

**Determining insights in qualitative data**: Customer feedback is jam-packed with practical insights. You’ll get an effective outline of the products, features and subjects that matter most to your clientele and the opportunity to figure out not only their pain points but where you’re succeeding with them.

**Discover hidden trends**: Use text analysis and gradually visualize insights in order to spot easily any inconsistencies and figure out the leading causes.

**Text Mining**

The fast growth spurt of social media platforms and availability of the internet means that year after year, a massive quantity of unstructured text data is produced. And that’s what text analysis is all about—acquiring insights or assembling this raw data with a view to propelling research, projects, business and other such activities.

A fresh area of research has emerged in the use of machinery to investigate texts—text mining. This is in contrast to the process of data mining used in computer science.

Text mining aims to uncover statistical patterns as it uses machines to analyze data points in a body of content with a large volume of text. Through this procedure, various patterns within a big data system begin to emerge.

Text mining benefits from text visualization tools as it’s so easy to read for both machine and human alike. The most vital bits of information are communicated through easy-to-read visual representations such as a bar chart, word cloud, graph, map, timeline or network.

**Why Text Visualizations are Necessary**

**Makes Text Data Easy to Grasp**

Did you know that your brain sorts through visual data 60 000 times faster than words or numbers? Text visualizations make complex data clearer and powerfully transmit ideas to team managers.

**Communicates What’s on Your Audience’s Mind**
A chart can help you figure out how your audience feels about a certain subject or issue. This chart can also be leveraged to condense data-driven views. First-hand data can be used to summarize any market feedback.

**Condenses Big Volumes of Text**
Reduce the time you’d spend reading big volumes of text. Instantly emphasize the main terms in a string of texts, categorize content by subject, sentiment or other themes.

A quick scan of a text data visualization or dashboard will update you on all the vital info you want and need to know.

**It Captivates**
If you take a look at a word cloud, you’ll see that it is both eye-catching and informative. A well-designed chart can be used to start a conversation on an array of interesting topics.

**It is Simple and Direct**
Creating and reading text visualizations are actually pretty straightforward. Whether it’s a bar chart or a graph, you’ll gain some actionable insights into sizable data sets.

**Word Cloud**
A word cloud is a text visualization technique that focuses on the frequency of words and correlates the size and opacity of a word to its frequency within a body of text. The output is usually an image that depicts different words in different sizes and opacities relative to the word frequency.

An application of this form of visualization is document summarization, where you can process a body of text within a document and, based on the most prominent words, get a general summary of what the document is all about. This can also be applied in job applications where if the job description is analyzed, the largest words to appear are most likely the most important skills for the job.

**Visualizing text data using word cloud:**

Use to visualize the frequency of words in a text groups with word size proportional to frequency. To use wordcloud, first download the package using pip install wordcloud. After this import the library using from wordcloud import WordCloud. Further process are shown below

Importing library from wordcloud import WordCloud

```python
import matplotlib.pyplot as plt
#text to be visualized
text = "hello BCA 8th semester. you are studying data visualization and best of luck for your board exam. you exam is on sunday and center is in padmakanya. if you fail in exam you get astrick in marksheet. Best of Luck "
plotting word cloud
wc = WordCloud(width=800, height=400, background_color="white").generate(text)
plt.figure(figsize=(10, 5))
plt.imshow(wc, interpolation="bilinear")
plt.axis("off")
plt.show()
```

In above code: wc = WordCloud(width=800, height=400, background_color="white").generate(text)

WordCloud function is used to generate wordcloud and text to be represented is calculated by generate() method.  
Visualizing text data using bar graph:

```python
import matplotlib.pyplot as plt
import seaborn as sns

from collections import Counter

text = "hello BCA 8th semester. you are studying data visualization and best of luck for your board exam. you exam is on sunday and center is in prime. if you fail in exam you get astrick in marksheet. Best of Luck, best best best best bestbest best best best best"

word_list = text.split()
word_freq = Counter(word_list)
sns.set_style("whitegrid")
plt.figure(figsize=(10, 5))
sns.barplot(x=list(word_freq.keys()), y=list(word_freq.values()))
plt.xticks(rotation=45)
plt.xlabel("Words")
plt.ylabel("Frequency")
plt.title("Word Frequencies")
plt.show()
```

**Separate, Order and Align**
In information visualization the most effective channel for encoding information is position. The usage of this channel depends of the type of attribute encoded. Quantitative variables should express its value across a continues scale, but for categorical ones you should **separate, order and align**.

**Separate:**

- To separate means to divide or set apart different elements or entities.
- It involves creating distinct boundaries or divisions between items or groups.
- The purpose of separation is to distinguish or isolate individual components, ensuring that they are distinct and independent from one another.

**Separate (Data Visualization):**

- In data visualization, separation involves visually distinguishing or isolating different data elements or categories.
- It entails creating clear boundaries or visual cues that set apart various data points, groups, or variables.
- By separating data, you can enhance the viewer's ability to differentiate and understand the distinct components within a visual representation, such as charts, graphs, or diagrams.

**Example**

- Suppose you have a bar chart representing sales data for different product categories. To separate the data, you can use distinctive colors for each category. For instance, you could assign the color blue to electronics, red to clothing, and green to furniture. This visual separation helps viewers easily identify and differentiate the sales figures for each product category.

**Order:**

- Order refers to arranging or organizing things in a particular sequence or pattern.
- It involves placing items or elements in a structured manner according to a specific
  criterion or system.
- Ordering can be done based on various factors, such as numerical, alphabetical,
  chronological, or hierarchical order.
- It helps to bring clarity, efficiency, and logic to a set of elements.

**Order (Data Visualization):**

- Ordering data in the context of data visualization means arranging the data points or
  categories in a structured manner to convey meaning or facilitate comprehension.
- Depending on the nature of the data, you can order it based on numerical values,
  alphabetical sequences, time periods, or hierarchical relationships.
- By ordering the data, you bring a logical and coherent structure to the visualization,
  allowing viewers to identify patterns, trends, or comparisons more easily.

**Example**

- Consider a line graph depicting stock market prices over time.
- To order the data, you would typically arrange the time series on the x-axis in chronological order, with the oldest date on the left and the most recent date on the right.
- This allows viewers to observe the progression of stock prices over time and identify any patterns or trends, such as upward or downward movements.

**Align**

- Alignment means adjusting or positioning things in such a way that they are in proper or accurate coordination or arrangement with one another.
- It involves making sure that different elements are correctly placed or matched relative to a reference point or a common set of guidelines.
- Alignment ensures that components are in harmony, agreement, or conformity with each other, facilitating coordination and coherence.

**Align (Data Visualization):**

- Alignment in data visualization refers to positioning and coordinating visual elements to create a visually harmonious and informative display.
- It involves aligning data points, labels, axes, or other graphical components with precision.
- Proper alignment ensures that the visual elements are visually cohesive, making it easier for viewers to interpret and make accurate comparisons or connections within the visualization.
- Alignment can also apply to text, spacing, and grid lines, promoting readability and clarity in the visualization.

**Example**

- Imagine a scatter plot representing the relationship between a person's age and their income.
- To align the data points, you would ensure that the x-axis represents age, starting from the lowest age value on the left and increasing towards the right.
- The y-axis would represent income, starting from the lowest income value at the bottom and increasing as you move upward.
- Aligning the axes in this way ensures that the data points align with the appropriate age and income values, enabling viewers to accurately interpret the relationship between the two variables.

**Summary:**

- **Separate**: Visually distinguish or isolate different data elements or categories, creating clear boundaries or cues to enhance differentiation.
- **Order**: Arrange data points or categories in a structured manner based on a specific criterion, facilitating comprehension and pattern identification.
- **Align**: Position and coordinate visual elements with precision, creating a visually cohesive and informative display that promotes readability and interpretation.

**Bar Chart**

- Use the bar chart to compare many items. The bar chart typically presents categories or items displayed along the Y axis, with their values displayed on the X axis. You can also break up the values by another category or group.

**What can I use bar and column charts for?**

Use bar and column charts to summarize and compare values in a data category, and provide a snapshot of your data at specified points in time (or other dimensions).

Although bar and column charts are similar in their appearance and functions, their respective orientations mean they are better suited to different types of analysis:

- Bar charts use a horizontal display, which provides more room for long, complex or numerous labels on the Y-axis. The labels also go from left to right, making labels on bar charts easy to read. In bar charts, categories are usually displayed along the Y- axis, so they're commonly used for analyses where time is not a factor.
- In column charts, time is usually displayed along the X-axis, with the unit of measurement on the Y-axis. As this left to right direction is associated with a chronological sequence, column charts are ideal for highlighting changes over time.

You can also use bar and column charts to rank items in a data series. To do this, you must sort your data (by saving a view in your module, or designing a custom view) before creating a chart, so that the ranking is reflected in it.

Negative values are represented clearly in bar and column charts, as any negative values are plotted in the opposite direction to positive values. However, relatively large negative or positive values reduce the amount of space available on a chart, which can make it hard to differentiate between similar values.

Use a bar or column chart to answer:

- How does A differ from B?
- Which salesperson sold the most product?
- What was the average growth over the last X years?
- What is the composition of our website traffic?

**Considerations**

A bar or column chart may not be the best option when:

- your data categories have long labels.
- the height or width size of a chart card has been altered. This can change the scale of
  your unit of measurement, which can be misleading as this diminishes or emphasizes
  differences in value in your bar or column chart.
