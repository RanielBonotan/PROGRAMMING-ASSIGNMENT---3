### PROGRAMMING-ASSIGNMENT 3

#### PROBLEM 1 - We are tasked to: a. Load the corresponding .csv file into a data frame named cars using pandas
and b. Display the first five and last five rows of the resulting cars.

a. 

1. First, I imported panmdas as pd to make the coding possible and not lead to error
 ```python
import pandas as pd #import the pandas to be used
```

2. I then went on to import the csv file to use the list
```python
cars = pd.read_csv("cars.csv")

cars #move the downloaded file and read the list of cars
```
b.

3.  I then used both head and tail function to obtain the first and last rows and columns on the list while combining them using concat
```python
firstlast = pd.concat([cars.head(), cars.tail()])

print("FIRST 5 and LAST 5: ") 

firstlast # arranges the list, limiting them to the first 5 and the last 5
```


#### PROBLEM 2 - We are tasked to: a. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars, b. Display the row that contains the ‘Model’ of ‘Mazda RX4’., c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?, and d. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4

a. 

1. using iloc, i was able to specifically choose the specific number of rows and the specific number of columns to be displayed.
```python
cars.iloc[[0, 1, 2, 3, 4], [1, 3, 5, 7, 9, 11]] #displays the first five rows in the list and the 5 odd-numbered columns
```
b.

2. being that the Mazda model is in the first of the list, Cars[0,1] was used to display the 1st on the list and is limited until there.
```python
cars[0:1] #locates the row of the MAZDA RX4 car
```
c.

3. Using cars.loc, i can specify which display name of where the column "model" and "cyl" is located and since the model Camaro is in the 24th row, I used 23 as the indicating row.
```python
cars.loc[[23], ["Model", "cyl"]] #locates the model CAMARO Z28and how many cylinders it contains.
```
d.

4. Similar to the previous part, using loc, I specified which row the specified cars are and displayed which columns "Model", "cyl", and "gear" are.
```python
cars.loc[[1, 28, 18], ["Model", "cyl", "gear"]] #locates the model, number of cylinders, and the number of gears of
# the Maza RX4 WAG, FORD PANTERA L, and the HONDA CIVIC
```
