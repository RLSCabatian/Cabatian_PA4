Dateframe
1.
``` python
import pandas as pd
#Input of the board2.xlsx file
df = pd. read_excel ("board2.xlsx" )
df ['Average'] = df.mean (numeric_only=True, axis=1)
df
```
![image](https://github.com/user-attachments/assets/f2f2044c-9cc6-4c36-97a8-c1f4d3964b9e)
![image](https://github.com/user-attachments/assets/582def43-4b74-4c20-be44-a7834fe5bc7b)
``` python
#Function to print the instruction asked.
print("--Instru--")
Instru = df.loc[(df.Track=="Instrumentation") & (df.Hometown=="Luzon") & (df.Electronics>70), ['Name', 'GEAS' , 'Electronics']]
Instru
```
![image](https://github.com/user-attachments/assets/2927b106-a886-47ba-a2cb-ad0703cc5967)
``` python
#Function to print the instruction asked.
print("—-Mindy--")
Mindy = df.loc[(df.Hometown=="Mindanao") & (df.Gender=="Female") & (df.Average>=55) , ['Name', 'Track', 'Electronics', 'Average']]
Mindy
```
![image](https://github.com/user-attachments/assets/2f3a0d10-e573-445b-93d4-f21f617ffca9)

2.
``` python
import matplotlib.pyplot as plt

#Function to print the graph that states the correlation of chosen track to grades.
plt.figure (figsize=(5,6))
plt.bar (df ['Track'], df ['Average'])
plt.xlabel ("Chosen Track in College") 
plt.ylabel ("Average")
plt.title ("Table 1.1: A bar graph showing the relationship of chosen track in college .")
```
![image](https://github.com/user-attachments/assets/349120d0-4876-492b-8af7-8ba9bcdd01cd)
``` python
#Function to print the graph that states the correlation of gender to grades.
plt.figure (figsize=(5,6))
plt.bar (df ['Gender'], df ['Average'])
plt.xlabel ("'Gender")
plt.ylabel ("Average")
plt.title ("Table 1.2: A bar graph showing the relationship of gender and average grade.")
```
![image](https://github.com/user-attachments/assets/e122b03d-c862-4283-a97a-8c3bd6cc7910)
``` python
#Function to print the graph that states the correlation of hometown to grades.
plt.figure(figsize=(5,6))
plt.bar (df['Hometown'],df ['Average'])
plt.xlabel ("Hometown" ) 
plt.ylabel ("Average")
plt.title ("Table 1.3: A bar graph showing the relationship of hometown and average grade.")
```
![image](https://github.com/user-attachments/assets/a7f6f602-a833-4463-a9f6-c1f6b24abd7c)



