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
