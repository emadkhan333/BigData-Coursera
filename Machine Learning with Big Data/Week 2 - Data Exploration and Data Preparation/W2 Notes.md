# Week 2 - Data Exploration & Data Preparation #
## Sample and Variable ##
A sample is an instance or example of an entity in your data. This is typically a row in your dataset. 
Values associated with the sample are called variables. These values are different information pieces about the sample such as the sample ID, sample date. Each variable has a data type associated with it. The most common data types are numeric and categorical.
There are many names for sample and variable. Some other terms for sample that you might hear in a machine learning context include record, example, row, instance and observation. There are also many names for the term variable, such as feature, column, dimension, attribute, and field. All of these terms refer to specific characteristics for each sample in your dataset. 
Each variable has a data type associated with it. The most common data types are numeric and categorical. As the name implies, numeric variables are variables that take on number values. Numeric variables can be measured, and their values can be sorted in some way. A variable with labels, names, or categories for values instead of numbers are called categorical variables. 
## Data Exploration ##
Data exploration means doing some preliminary investigation of your data set. The goal is to gain a better understanding of the data that you have to work with. Data exploration is also called exploratory data analysis, or EDA for short. 
There are two main categories of techniques to explore your data
- summary statistics
- visualization. 
*Summary Statistics*
Summary statistics provide important information that summarizes a set of data values. There are many such statistics such as mean, median, and standard deviation. A summary statistic provides a single quantity that summarizes some aspects of the dataset. For example, the mean, is a single value that describes the average value of the dataset, no matter how large that dataset.
*Visualization*
Data visualization techniques allow you to look at your data, graphically. There are several types of plots that you can use to visualize your data. Some examples are histogram, line plot, and scatter plot. Each type of plot serves a different purpose.
*Why to do Data Exploration*
You use statistics and visual methods to summarize and describe your dataset, and some of the things you'll want to look for are 
- Correlations
- General trends 
- Outliers 
Correlations provide information about the relation took between variables in your data. By looking at correlations, you may be able to determine that two variables are very correlated. This means they provide the same or similar information about your data. Since this contain redundant information, this suggest that you may want to remove one of the variables to make the analysis simpler. 
Trends in your data will reveal characteristics in your data. For example, you can see where the majority of the data values lie, whether your data is skewed or not, what the most frequent value or values are in a date set, etc. 
Calculating the minimum, the maximum and range of the data values are basic steps in exploring your data. Determining outliers is a also very important. Outliers indicate potential problems with the data and may need to be eliminated in some applications. In other applications, outliers represent interesting data points that should be looked at more closely. In either case, outliers usually require further examination. 

## Data Exploration through Summary Statistics ##
Summary statistics are quantities that describe a set of data values. Summary statistics provide a simple and quick way to summarize a dataset. We will discuss three main categories of summary statistics:
- Measures of location or centrality: Mean, Median
- Measures of spread: Standard deviation
- Measures of shape: Skewness
## Statistics on Numerical Variables ##
### Measures of Location ###
Measures of location are summary statistics that describe the central or typical value in your dataset. These statistics give a sense of the middle or center of the dataset. Examples of these are mean, median and mode. The mean is just the average of the values in a dataset. The median is the value in the middle if you sorted the values in your dataset.The mode is a value that is repeated more often than any other value. 
### Measures of Spread ###
Measures of spread describe how dispersed or varied your dataset is. Common measures of spread are minimum, maximum, range, standard deviation and variance. Minimum and maximum are of course the smallest and largest values in your dataset respectively. The range is simply the difference between the maximum and minimum and tells you how spread out your data is. Standard deviation describes the amount of variation in your dataset. 
A low standard deviation value means that the samples in your dataset tend to be close to the mean. And a high standard deviation value means that the data samples are spread out. Variance is closely related to standard deviation. In fact the variance is the square of the standard deviation. So it also indicates how spread out the data samples are from the mean 

### Measures of Shape ###
Measures of shape describe the shape of the distribution of a set of values. Common members of shape are skewness and kurtosis.  
Skewness indicates whether the data values are asymmetrically distributed. A skewness value of around zero indicates that the data distribution is approximately normal, as shown in the middle figure in the top diagram. A negative skewness value indicates that the distribution is skewed to the left, as indicated in the left figure in the top diagram. A positive skewness value on the other hand indicates that the data distribution is skewed to the right. 
 
Kurtosis measures the tailedness of the data distribution or how heavy or fat the tails of the distribution are. A high kurtosis value describes a distribution with longer and fatter tails and a higher and sharper central peak, indicating the presence of outliers. A low kurtosis value on the other hand, describes a distribution with shorter and lighter tails and lower and broader central peak, suggesting the lack of outliers. 
### Measures of Dependence ###
Measures of dependence determine if any relationship exists between variables. Pairwise correlation is a commonly used measure of dependence. Correlations is between zero and one, with zero indicating no correlation, and one indicating a one to one correlation. 
## Statistics on Categorical Variables ##
For categorical variables, we want to look at statistics that describe the number of categories and the frequency of each category. This is done using a contingency table. 
For machine learning problems, we also want to examine some additional statistics to quickly validate the data. One of the first things to check is the number of rows and the number of columns in your dataset. Does the number of rows match the expected number of samples? Does the number of columns match the expected number of variables? These should be very quick and easy checks. 
Another easy data validation check is to look at the values in the first and last few samples in your dataset to see if they're reasonable. Are the data types for your variables correct, for example, is the date field captured as dates or timestamp. Or is it capture as a string or numerical value? These will have consequences in how these fields should be processed. 
Another important step is to check for missing values. You need to determine the number of samples with missing values. You also need to determine if there are any variables with a high percentage of missing values. 
## Data Exploration through Visualizations ##
Visualizing data, that is looking at data graphically, is a great way to explore your data set. Data visualization is a nice complement to using summary statistics for exploring data. There are several types of plots that you can use to visualize your data. Some of them are:
- histogram
- line plot
- scatter plot
- bar plot
- box plot </br>
*Histogram*
A histogram is used to display the distribution of a variable. The range of values for the variable is divided into the number of bins, and the number of values that fall into each bin is counted. Which determines the height of each bin. 
 
A histogram can reveal many things about a variable in your data, for example, you can usually determine the central tendency of a variable, that is where the majority of the values lie. You can also see the most frequent value of values for that variable. 
A histogram also shows whether the values for that variable are skewed and whether the skewness is to the left towards smaller values or to the right towards larger values. You can also pick outliers in the histogram as shown on the bottom plot. 
*Line Plot*
A line plot shows how data values change over time. The values of a variable or variables are shown on the Y axis and the X axis shows the motion of time. The resulting line displays the data values over time. 
 
A line plot can show patterns in your variables. For example, a cyclical pattern can be detected as in this plot, where the values start high, then decrease and go back up again. 
Trends can also be detected as shown in the upper-right plot where the values fluctuate but show a general upward trend over time. 
It is also easy to compare how multiple variables change over time on a single line plot as displayed in the center bottom plot. 
*Scatter Plot*
A scatter plot is a great way to visualize the relationship between two variables. One variable is on the x axis. The other variable is on the y axis Each sample is a product using the values of the 2 variables aspects and Y coordinates. The resulting plot shows how one variable changes as the other is changed. 
A scatter plot can be used to display the correlation between 2 variables. For example, 2 variables such as the high temperature of the day, and the low temperature of the day, can have a positive correlation as shown in this plot. 
 
A positive correlation means that as the value of one variable increases, the value of the other variable also increases by a similar amount. 
The upper right scatter plot shows a negative correlation between two variables. This means that as the value of one variable increases, there is a corresponding decrease in the other variable.
 Two variables can also have a non-linear correlation as shown in the lower left plot. This means that a change in one variable will not always correspond to the same change in the other variable. This is indicated by the curve in the scatter plot as opposed to something closer to a straight line for linear correlation. 
There can also be no correlation between two variables. In this case, you will see something like randomly placed dots as displayed in the lower right plot, indicating no relationship between how the two variables change with respect to each other.
*Bar Plot*
A bar plot is used to show the distribution of categorical variables. Recall that a histogram is also used to look at the distribution of the values of the variable. The difference is that in general, a histogram is used for numeric variables whereas a bar plot is used for categorical variables. In a bar chart, the different categories of a categorical variable is shown along the x-axis, and the count of instances for each category is displayed on the y-axis. This is an effective way to compare the different categories. 
 
A bar plot is also a great way to compare two categorical variables. For example, this plot compares two categorical variables. One in blue and the other in orange, each with three different categories. Here you can see that for the first category, the blue variable has the higher count, while the orange variable has a higher count for the second and third category. This type of Bar Plot is called a Grouped Bar Chart. And the different variables of products side by side. 
A different kind of comparison can be performed using a Stacked Bar chart as seen in a lower right quad. Here, the accounts for the two variables are stacked on top of each other for each category. With this bar chart, you can determine that the combined count for the first category is about equal to the combine count for the second category, while the compliant count for the third category is much larger. 
*Box Plot*
 
A box plot is another plot that shows the distribution of a numeric variable, it shows the distribution in a different format than the histogram. This is how a box plot displays the distribution of values for a variable, the gray portion in the figure is the box part. The lower and upper boundaries of the box represent the 25th and 75th percentiles respectively. This means that the box represents the middle 50% of the data, the median is the 50th percentile, meaning that 50% of the data is greater than its value and 50% of the data is less than this value. The top and bottom lines are the Whiskers and represent the 10th and 90th percentiles respectively. So, 80% of the data are in the region indicated by the upper extreme and lower extreme. Any data values outside of this region are outliers and are indicated as single point on the box plot. 
Box plots provide a compact way to show how variables are distributed, so they are often used to compare variables. The box plot on the left for example compares the base salary for two different roles.
 
A box plot can also show you if the distribution of the data values is symmetrical, positively skewed or negatively skewed. Here we see that a box plot can also be displayed on its side. A symmetric distribution is indicated if the line in the box which specifies the median, is in the center of the box. A negative skew is indicated when the median is to the right of the center of the box. This means that there are more values that are less than the median than there are values greater than the median. Similarly, a positive skew is indicated when the median is to the left of the center of the box. 
