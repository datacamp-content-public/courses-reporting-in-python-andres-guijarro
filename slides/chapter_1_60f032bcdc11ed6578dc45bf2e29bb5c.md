---
title: Insert title here
key: 60f032bcdc11ed6578dc45bf2e29bb5c

---
## Making effective plots

```yaml
type: "TitleSlide"
key: "2ace50a7ae"
```

`@lower_third`

name: Andres Guijarro
title: Instructor


`@script`
A plot is a visual representation of data that can present complex information quickly and clearly and assist the reader in seeing patterns and trends in data.

However, it is not enough to create the plots. They must be clutter-free, easy to interpret, and appropriately represent trends or differences in the data.


---
## **Making effective plots**

```yaml
type: "FullSlide"
key: "e4b6f32653"
```

`@part1`
You will learn how to create meaningful, easy to read and well-formatted graphs for use in statistical reporting.{{1}} 

Specifically:{{2}}

- Labels {{3}}

- Ticks {{4}}

- Titles {{5}}

- Visual style {{6}}


`@script`
This video provides guidelines on how to create meaningful, easy to read and well-formatted graphs for use in statistical reporting. It contains hints and tips on presentation. Specifically, you will learn how to include additional objects and characteristics such as Labels, Ticks, Titles, and visual style required to create effective plots.


---
## **Basic Plot**

```yaml
type: "TwoColumns"
key: "c1dc627c67"
center_content: false
```

`@part1`
```python
import matplotlib.pyplot as plt
import seaborn as sns

# Create data
objects = ('Python', 'C++', 'Java', 
'Perl', 'Scala', 'Lisp')
y_pos = np.arange(len(objects))
performance = [10,8,6,4,2,1]

# Create Plot
plt.bar(y_pos, performance, 
align='center', alpha=0.5, 
color = ['#E13F29','#D69A80',
'#D63B59','#AE5552','#CB5C3B'])

# Display plot
plt.show()


```{{1}}


`@part2`
![](https://assets.datacamp.com/production/repositories/4187/datasets/229f43406cf9270e3d4b0960ad78dd95e80b20ff/screencast1.png){{2}}


`@script`
Let’s start with the code to build a simple bar plot. It’s similar to the bar plot we have created in the previous lessons.

If you run this script, we get a pretty nice plot with no meaning at all. So that, there are many things that need to be improved.


---
## **Axis labels**

```yaml
type: "TwoColumns"
key: "8b98a9b8ac"
```

`@part1`
```python
import matplotlib.pyplot as plt
import seaborn as sns

# Create data
objects = ('Python', 'C++', 'Java', 
'Perl', 'Scala', 'Lisp')
y_pos = np.arange(len(objects))
performance = [10,8,6,4,2,1]

# Create Plot
plt.bar(y_pos, performance, 
align='center', alpha=0.5, 
color = ['#E13F29','#D69A80',
'#D63B59','#AE5552','#CB5C3B'])
```{{2}}
```python
# Label both axis
plt.xlabel('Programming language')
plt.ylabel('Usage')
```{{3}}
```python
# Display plot
plt.show()
```{{2}}


`@part2`
![](https://assets.datacamp.com/production/repositories/4187/datasets/8eb2df1b059d55ff2ab65ba7260c2c543146bbff/screencast2.png){{4}}


`@script`
The first thing you always need to do is include labels for both the x-axis (horizontal) and y-axis (vertical). Labels should be brief and explain exactly what each aspect of the graph is showing. Let’s do this by adding the xlabel() and ylabel() functions. As inputs, we pass strings that should be placed alongside the axes. Make sure to call these functions before calling the show() function, otherwise labels will not be displayed. If we run the script again, this time the axes are annotated.

However, let's verify if the labels of the x-axis make sense, and the answer is no because they are not descriptive names.


---
## **Ticks**

```yaml
type: "TwoColumns"
key: "f347730912"
```

`@part1`
```python
import matplotlib.pyplot as plt
import seaborn as sns

# Create data
objects = ('Python', 'C++', 'Java', 
'Perl', 'Scala', 'Lisp')
y_pos = np.arange(len(objects))
performance = [10,8,6,4,2,1]

# Create Plot
plt.bar(y_pos, performance, 
align='center', alpha=0.5, 
color = ['#E13F29','#D69A80',
'#D63B59','#AE5552','#CB5C3B'])
```{{1}}
```python
# Modify Ticks
plt.xticks(y_pos, objects)
```{{2}}
```python
# Label both axis
plt.xlabel('Programming language')
plt.ylabel('Usage')
```{{1}}
```python
# Display plot
plt.show()
```{{1}}


`@part2`
![](https://assets.datacamp.com/production/repositories/4187/datasets/4a6fbda5ed5f08c95dfe45818a2ce569fed56741/screencast3.png){{3}}


`@script`
To customize the labels, we will use ticks. Ticks are small marks on both axes of a figure. Matplotlib's default tick locators and formatters are designed to be sufficient in many common situations but are in no way optimal for every plot.  For our example, we will use xticks() function. The first input is an ordered list of numbers, and the second input is a list with the display names of the ticks. Both lists must have the same size. If we run this version of the script, the x-labels will change and make sense now.


---
## **Title**

```yaml
type: "TwoColumns"
key: "fbea6a8342"
```

`@part1`
```python
import matplotlib.pyplot as plt
import seaborn as sns

# Create data
objects = ('Python', 'C++', 'Java', 
'Perl', 'Scala', 'Lisp')
y_pos = np.arange(len(objects))
performance = [10,8,6,4,2,1]

# Create Plot
plt.bar(y_pos, performance, 
align='center', alpha=0.5, 
color = ['#E13F29','#D69A80',
'#D63B59','#AE5552','#CB5C3B'])
# Modify Ticks
plt.xticks(y_pos, objects)
# Label both axis
plt.xlabel('Programming language')
plt.ylabel('Number of Users')
```{{1}}
```python
# Add title
plt.title('Number of Users by Programing Language')
```{{2}}
```python
# Display plot
plt.show()
```{{1}}


`@part2`
![](https://assets.datacamp.com/production/repositories/4187/datasets/06ee72c1f2b46d8f3bfdb03763aa9638a2ff2b8b/screencast4.png){{3}}


`@script`
We are also going to add a title to our graph with the title() function. This function receives a string as an input.

The title is usually placed in the center, either above or below the graph. It summarize what the graph shows by explaining what the x and y axes represent. 

For example, if we want to show the number of users per Programing Language the Programing Language would be the independent variable and the number of users would be the dependent variable. 

Therefore, the title should be "Number of Users by Programing Language”.


---
## **Colors**

```yaml
type: "TwoColumns"
key: "94048a07da"
```

`@part1`
![](https://assets.datacamp.com/production/repositories/4187/datasets/06ee72c1f2b46d8f3bfdb03763aa9638a2ff2b8b/screencast4.png){{1}}


`@part2`
![](https://assets.datacamp.com/production/repositories/4187/datasets/a1965d841a5d500453ea61ffdabb537067acf556/screencast5.png){{2}}


`@script`
Finally, use different colors only when they correspond to differences of meaning in the data.

The following graph illustrates one version of what we should avoid.

What do the different bar colors in this graph mean? Nothing. The colors add no meaning or value. The labels along the X-axis tell us what the bars represent.


---
## **Colors (2)**

```yaml
type: "TwoColumns"
key: "b8a94f465b"
```

`@part1`
```python
import matplotlib.pyplot as plt
import seaborn as sns

# Create data
objects = ('Python', 'C++', 'Java', 
'Perl', 'Scala', 'Lisp')
y_pos = np.arange(len(objects))
performance = [10,8,6,4,2,1]
```{{1}}
```python
# Create Plot
plt.bar(y_pos, performance, 
align='center', alpha=0.5, 
color = ['#E13F29','#D69A80',
'#D63B59','#AE5552','#CB5C3B'])
```{{2}}
```python
# Modify Ticks
plt.xticks(y_pos, objects)
# Label both axis
plt.xlabel('Programming language')
plt.ylabel('Number of Users')

# Add title
plt.title('Number of Users by Programing Language')

# Display plot
plt.show()
```{{1}}


`@part2`
```python
import matplotlib.pyplot as plt
import seaborn as sns

# Create data
objects = ('Python', 'C++', 'Java', 
'Perl', 'Scala', 'Lisp')
y_pos = np.arange(len(objects))
performance = [10,8,6,4,2,1]
```{{1}}
```python
# Create Plot
plt.bar(y_pos, performance, 
align='center', alpha=0.5)
```{{2}}
```python
# Modify Ticks
plt.xticks(y_pos, objects)
# Label both axis
plt.xlabel('Programming language')
plt.ylabel('Number of Users')

# Add title
plt.title('Number of Users by Programing Language')

# Display plot
plt.show()
```{{1}}


`@script`
So, let’s remove the bar color. To do that, in the bar function remove the color attribute, and that's it!


---
## Let's practice

```yaml
type: "FinalSlide"
key: "762e4eeca3"
```

`@script`
Now it is your turn. Head over to the exercise and let’s get  building an effective plot. I will see you back here soon!

