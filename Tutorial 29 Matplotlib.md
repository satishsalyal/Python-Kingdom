# Matplotlib

In this chapter, we will delve into the powerful world of data visualization using Matplotlib, a comprehensive library for creating static, animated, and interactive visualizations in Python. Matplotlib is widely used for generating plots, charts, histograms, and more, making it an essential tool for data analysis and presentation.

### Introduction to Matplotlib

Matplotlib is an open-source library that provides a plethora of functions for creating high-quality visualizations in Python. Developed by John D. Hunter in 2003, Matplotlib has since become one of the most popular plotting libraries due to its flexibility, extensive functionality, and vibrant user community.

### Installation

Before we begin, ensure that Matplotlib is installed in your Python environment. You can install it via pip:


```python
pip install matplotlib
```
### Getting Started
Let's start by importing Matplotlib into our Python script:

```python

import matplotlib.pyplot as plt
```
The **pyplot** module is a collection of functions that make Matplotlib work like MATLAB. It provides a convenient interface for creating plots and modifying them with various parameters.

### Basic Plotting

One of the simplest plots to create with Matplotlib is a line plot. Let's generate a basic plot to visualize a mathematical function:

```python

import numpy as np

# Generate data
x = np.linspace(0, 10, 100)
y = np.sin(x)

# Create a plot
plt.plot(x, y)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Sine Function')
plt.grid(True)
plt.show()
```
In this example, we use NumPy to create an array of evenly spaced numbers (x) from 0 to 10 and calculate the corresponding sine values (y). We then use plt.plot() to create a line plot, and plt.xlabel(), plt.ylabel(), and plt.title() to add labels and a title to the plot. Finally, plt.grid(True) adds grid lines to the plot, and plt.show() displays the plot.

### Customizing Plots

Matplotlib allows for extensive customization of plots. Here's an example demonstrating various customization options:

```python

# Customize plot
plt.plot(x, y, color='red', linestyle='--', linewidth=2, marker='o', markersize=5, label='Sine Curve')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Customized Sine Function')
plt.grid(True)
plt.legend()
plt.savefig('sine_plot.png')  # Save plot as PNG file
plt.show()
```
In this example, we customize the line color, style, width, marker style, and size using arguments in the plt.plot() function. We also add a legend with plt.legend(), and save the plot as a PNG file using plt.savefig().


### Axes Class
Axes class is the most basic and flexible unit for creating sub-plots. A given figure may contain many axes, but a given axes can only be present in one figure. The axes() function creates the axes object. Let’s see the below example.

### Syntax:

matplotlib.pyplot.axis(*args, emit=True, **kwargs)

```python 

# Python program to show pyplot module 
import matplotlib.pyplot as plt  
from matplotlib.figure import Figure  
# Creating the axes object with argument as  
# [left, bottom, width, height] 
ax = plt.axes([1, 1, 1, 1])
```

## What is a Legend?
A legend is an area describing the elements of the graph. In simple terms, it reflects the data displayed in the graph’s Y-axis. It generally appears as the box containing a small sample of each color on the graph and a small description of what this data means.

### Creating the Legend
A Legend can be created using the legend() method. The attribute Loc in the legend() is used to specify the location of the legend. The default value of loc is loc=”best” (upper left). The strings ‘upper left’, ‘upper right’, ‘lower left’, ‘lower right’ place the legend at the corresponding corner of the axes/figure.

The attribute bbox_to_anchor=(x, y) of legend() function is used to specify the coordinates of the legend, and the attribute ncol represents the number of columns that the legend has. Its default value is 1.

### Syntax:

matplotlib.pyplot.legend([“blue”, “green”], bbox_to_anchor=(0.75, 1.15), ncol=2)
```python

import matplotlib.pyplot as plt  
  
# data to display on plots  
x = [3, 1, 3]  
y = [3, 2, 1]  
plt.plot(x, y) 
plt.plot(y, x) 
  
# Adding the legends 
plt.legend(["blue", "orange"]) 
plt.show()
```


# Multiple Plots Using subplot() method. 
This method adds another plot to the current figure at the specified grid position.

### Syntax:

subplot(nrows, ncols, index, **kwargs)

subplot(pos, **kwargs) 

subplot(ax)

```python


import matplotlib.pyplot as plt  
# data to display on plots  
x = [3, 1, 3]  
y = [3, 2, 1]  
z = [1, 3, 1]  
  
# Creating figure object  
plt.figure()  
  
# adding first subplot  
plt.subplot(121)  
plt.plot(x, y)  
  
# adding second subplot  
plt.subplot(122)  
plt.plot(z, y)
```

# Python Matplotlib : Types of Plots
There are various plots which can be created using python matplotlib. Some of them are listed below:

### 1. Line Plot
A line plot is one of the simplest and most frequently used plot types. It's ideal for visualizing trends over a continuous interval.

```python

import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.plot(x, y)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot: Sine Function')
plt.show()
```

### 2. Scatter Plot
Scatter plots are useful for visualizing the relationship between two variables. Each data point is represented individually, making it easy to identify patterns or correlations.

````python

x = np.random.rand(100)
y = np.random.rand(100)

plt.scatter(x, y)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Scatter Plot')
plt.show()
```

### 3. Bar Plot
Bar plots are effective for displaying and comparing categorical data. They consist of rectangular bars with lengths proportional to the values they represent.

```python

x = ['A', 'B', 'C', 'D', 'E']
y = [10, 20, 15, 25, 30]

plt.bar(x, y)
plt.xlabel('Categories')
plt.ylabel('Values')
plt.title('Bar Plot')
plt.show()
```

### 4. Histogram
Histograms are used to visualize the distribution of a dataset. They display the frequency of data points within specified bins or intervals.

```python

data = np.random.randn(1000)

plt.hist(data, bins=30)
plt.xlabel('Value')
plt.ylabel('Frequency')
plt.title('Histogram')
plt.show()
```

### 5. Pie Chart
Pie charts represent data as slices of a circle, with each slice representing a proportion of the whole. They're suitable for showing relative proportions or percentages.

```python

sizes = [20, 30, 25, 15, 10]
labels = ['A', 'B', 'C', 'D', 'E']

plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.title('Pie Chart')
plt.show()
```
### 6. Box Plot
Box plots, also known as box-and-whisker plots, provide a graphical summary of the distribution of a dataset. They display the median, quartiles, and outliers if any.

```python

data = np.random.randn(100)

plt.boxplot(data)
plt.title('Box Plot')
plt.show()
```

### 7. Violin Plot
Violin plots are similar to box plots but provide a more informative representation by displaying the kernel density estimation of the underlying distribution.

```python

data = [np.random.normal(0, std, 100) for std in range(1, 4)]

plt.violinplot(data)
plt.title('Violin Plot')
plt.show()
```
