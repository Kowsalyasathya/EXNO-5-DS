# EXNO 5 DS DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
### 1.Line Chart:
```
import matplotlib.pyplot as plt
import numpy as np
x=[0,1,2,3,4,5]
y=[0,2,8,12,26,25]
plt.plot(x,y)
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/0cdc3ead-38fe-4898-931f-63c254b58157)
### 2.Multi Line Chart:
```
x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1,label="line 1")
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label="line 2")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Multi-Line Chart')
plt.legend()
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/c2786229-7453-4dbf-8b07-031e6d59dad2)
### 3.Area chart:
```
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='pink')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='blue')
plt.legend(['y1','y2'])
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/028f686d-a547-4449-a8a7-06d029a7069b)
### 4.Stacked Area Chart:
```
plt.stackplot(x,y1,y2,y3,labels=['Line 1','Line 2','Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/f175f755-21ba-4583-9cdf-2c5c92f2c5e2)
### 5.Spine Chart:
```
plt.stackplot(x,y1,y2,y3,labels=['Line 1','Line 2','Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/d5109079-2124-48d0-93e6-54ea285cdd76)
### TO VISUALIZE RELATIONSHIPS:
### 1.Bar chart:
```
val=[5,6,4,7,2]
names=["A","B","C","D","E"]
plt.bar(names,val,color="pink")
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/3b85a8f1-a85a-4bb3-83a5-d3d9ca262cc4)
### 2.Scatter Plot:
```
x=[0,1,2,3,4,5]
y=[0,1,4,9,11,15]
plt.scatter(x,y,s=30,color="Black")
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/6c975c2c-5e25-47cc-95a2-0460a3c7e46b)
### 3.Bubble chart:
```
x = [1, 2, 3, 4, 5]
y = [10, 15, 20, 25, 30]
sizes = [100, 200, 300, 400, 500]
plt.scatter(x, y, s=sizes, alpha=1)
plt.xlabel('x_values')
plt.ylabel('y_values')
plt.title('Bubble Chart')
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/d43f3e75-07aa-4e72-9a4a-6294cb88b432)
### TO CAPTURE DISTRIBUTIONS:
### 1.Histogram:
```
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color='red',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('No. Of People')
plt.title('Histogram')
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/aee6595b-5ce6-489b-bcf8-d9b398474f34)
### 2.Box Plot:
```
np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/74ffc3dd-69a5-4d09-9b7f-ca964212bf41)
```
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box Plot')
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/9a0dd385-b47a-4de2-9407-f5c73ae54fe7)
### 3.Violin Plot:
```
data = [np.random.normal(loc=0, scale=1, size=100),
        np.random.normal(loc=2, scale=1, size=100),
        np.random.normal(loc=1, scale=2, size=100)]
plt.violinplot(data)
plt.xlabel('Groups')
plt.ylabel('Values')
plt.title('Violin Plot')
plt.xticks([1, 2, 3], ['Group 1', 'Group 2', 'Group 3'])
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/ac31f799-bff7-46a4-9fa5-5460efb63de4)
### 4.Density Chart:
```
data = np.random.normal(0, 1, 1000)
plt.hist(data, bins=30, density=True, alpha=0.2)
plt.title('Density Plot Example')
plt.xlabel('Values')
plt.ylabel('Density')
from scipy.stats import gaussian_kde
kde = gaussian_kde(data)
x_vals = np.linspace(min(data), max(data), 1000)
plt.plot(x_vals, kde(x_vals), 'r')
plt.show()
```
![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/cd91a1fb-335e-4439-a89a-56722ef3baeb)
### 5.Pie chart:
```
act=['eat','sleep','work','play']
slices=[3,7,8,6]
color=['r','y','g','b']
plt.pie(slices,labels=act,colors=color,startangle=90,shadow=True,explode=(0.1,0.1,0.1,0.1),radius=1.2,autopct='%1.1f%%')
plt.legend()
plt.show()
```

![image](https://github.com/Kowsalyasathya/EXNO-5-DS/assets/118671457/a550e6df-4110-4acc-a69a-3fc24afa4604)

# Result:
The Data Visualization using matplot python library is implemented successfully.
