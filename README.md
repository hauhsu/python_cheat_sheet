# Using Functions

```python
>>> def plus1(num):
...    return num+1
...
>>> plus1(3)
4

```

# Using Classes

```python

>>> class Man():
...
...     def __init__(self, name, age):
...         self.name = name
...         self.age = age
...
...     def introduce(self):
...         print("Hi, my name is " + self.name + ".")
...         print("I am " + str(self.age) + " years old.")
...
>>> tom = Man('Tom', 13)
>>> tom.introduce()
Hi, my name is Tom.
I am 13 years old.

```

# Using for-loops

```python
>>> refrigerator = ['apple', 'banana', 'orange']
>>> for food in refrigerator:
...    print(f"We have {food} in frige.")
...
We have apple in frige.
We have banana in frige.
We have orange in frige.

```


# Working with CSV (Comma Separate Values)

```python
>>> import csv
>>> csvlines = []
>>> with open('scores.csv', newline='') as csvfile:
...     reader = csv.reader(csvfile)
...     for row in reader:
...         csvlines.append(row)
...         print(row)
['Name', '1st round', '2nd round', '3rd round']
['Howard', '15.03', '14.11', '14.10']
['Karing', '16.33', '15.78', '16.04']

>>> with open('new_scores.csv', 'w', newline='') as newcsvfile:
...     writer = csv.writer(newcsvfile)
...     writer.writerow(csvlines[0])  # write header row
...     for line in csvlines[1:]:
...         line[2] = str(float(line[2]) + 0.3)
...         writer.writerow(line)
36
26
26

```
