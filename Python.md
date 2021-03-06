
## Function
- optional param
  - last
  - preset val
```py
def add_numbers(x, y, z=None, flag=False)

type(add_numbers)
```

## Type
- Make sure you convert objects to strings before concatenating.
- slicing
- packing
```py
for name, email in tel_dict.items():
    print(name)
    print(email)
```
- use Unicode(UTF)

- read CSV
```py
import csv

%precision 3

with open('mpg.csv') as csvfile:
    mpg = list(csv.DictReader(csvfile))
```

- date, time

```py
import datetime as dt
import time as tm

dtnow = dt.datetime.fromtimestamp(tm.time())
dtnow

dtnow.year, dtnow.month, dtnow.day, dtnow.hour, dtnow.minute, dtnow.second 
# get year, month, day, etc.from a datetime

delta = dt.timedelta(days = 100) # create a timedelta of 100 days
delta
today = dt.date.today()
today - delta # the date 100 days ago

```
- map()
  - applied to the items from all iterables in parallel.
  - stops when the shortest iterable is exhausted
```py
store1 = [10.00, 11.00, 12.34, 2.34]
store2 = [9.00, 11.10, 12.34, 2.01]
cheapest = map(min, store1, store2)
cheapest # lazy

for item in cheapest:
    print(item)
```

- lambda: 
  - no name
  - one line expression for simple task

```py
for person in people:
    print(split_title_and_name(person) == (lambda x: x.split()[0] + ' ' + x.split()[-1])(person))
    
list(map(split_title_and_name, people)) == list(map(lambda person: person.split()[0] + ' ' + person.split()[-1], people))

my_list = [number for number in range(0,1000) if number % 2 == 0]
[(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]
```
#3 NumPy
```py
import numpy as np

# matrix

m = np.array([[7, 8, 9], [10, 11, 12]])
m
array([[ 7,  8,  9],
       [10, 11, 12]])
# dimension
m.shape
(2, 3)

n = np.arange(0, 30, 3) # start at 0 count up by 2, stop before 30
o = np.linspace(0, 4, 9) # return 9 evenly spaced values from 0 to 4
n = n.reshape(3, 5) # reshape array to be 3x5

np.eye(3)
array([[ 1.,  0.,  0.],
       [ 0.,  1.,  0.],
       [ 0.,  0.,  1.]])

# dot product
x.dot(y) # dot product  1*4 + 2*5 + 3*6

# transpose
z.T

argmax and argmin return the index of the maximum and minimum values in the array.

r[3, 3:6]
r[r > 30]=30

r_copy = r.copy()

test = np.random.randint(0, 10, (4,3))
for i, row in enumerate(test):
    print('row', i, 'is', row)

for i, j in zip(test, test2):
    print(i,'+',j,'=',i+j)

```














