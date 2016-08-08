#variables

boolean caps

** exponent



```
monty = True

python = 1.234

monty_python = python ** 2

string = "string"
```

\ operator to escape chars

``'This isn\'t flying, this is falling with style!'``




#Whitespace

`IndentationError: expected an indented block`


code needs to be indented with 4 spaces


```
def spam():
    eggs = 12
    return eggs

```

#Comments

`#single line comment`

```
"""multi
line
comment"""
```

#variables

can use mathmatical operators on variables

```
addition = 72 + 23
subtraction = 108 - 204
multiplication = 108 * 0.5
division = 108 / 9
```

#Strings

`len()` length of string
`lower()`
`str()` turns non strings into strings
`.isalpha` checks if the strings is just alhpabet

methods that use dot notation only work on strings


```
parrot = "Norwegian Blue"

print len(parrot)
print parrot.lower()

```

adding variables to strings

```
string_1 = "Camelot"
string_2 = "place"

print "Let's not go to %s. 'Tis a silly %s." % (string_1, string_2)
```

raw input takes an input from the keyboard

`quest = raw_input("What is your quest?")`

#Date

`from datetime import datetime`

`datetime.now`

```
now = datetime.now()

print now

print now.year
print now.month
print now.day
print '%s:%s:%s' % (now.hour, now.minute, now.second)
```

#Conditional operators

`and`

`or`
`not` swaps true for false and vice versa


there is an order of operations

not then and then or

#If statement
```
if 8 < 9:
    print "Eight is less than nine!"
```

#functions

still need paranthesis on a method that takes no args

```
def cube(number):
    return number ** 3

def by_three(number):
    if number % 3 == 0 :
        return cube(number)
    else :
        return False
```

#importing pythons modules

`import this`


for whole module...

```
import math
print math.sqrt(25)
```

for one function

`from math import sqrt`


list all the functions

```
import math            # Imports the math module
everything = dir(math) # Sets everything to a list of things from math
print everything       # Prints 'em all!
```

some python modules without importing libraries

`max(args)`
`min(args)`
`abs(args)` positive number
`type(args)` type of object


```
def distance_from_zero (num):
    if type(num) == int or type(num) == float:
        return abs(num)
    else:
        return "Nope"

    ```

#Lists

List are a datatype you can use to store a collection of different pieces of info as a sequence under a single variable.

zero indexed

Ruby Arrays?!

`list_name = [item_1, item_2]`

Lists do not have a fixed length, you can add items to a list at any time.


```
suitcase = []
suitcase.append("sunglasses")
list_length = len(suitcase)
```

can slice a list to access a portion of the list.

```
letters = ['a', 'b', 'c', 'd', 'e']
slice = letters[1:3]
```

strings are lists of charachters

```
my_list[:2]
# Grabs the first two items
my_list[3:]
# Grabs the fourth through last items
```
`.index()` returns the index of the element in the array.
`.insert(index, element)`

```
animals = ["ant", "bat", "cat"]
print animals.index("bat")
```

`.sort()` to sort the list

`.remove()` to remove elements from a list

`backpack = ['xylophone', 'dagger', 'tent', 'bread loaf']``
`backpack.remove("dagger")`


`n.pop(index)` removes an element from the list at the index you specify and returns it

`n.remove(item)` removes the item from the list not the element at the index.

`del(n[1])` is like `.pop` in that it will remove the item at the given index, but it won't return it


When we pass a list to a function and modify that list, like in the double_first function above, we end up modifying the original list.

```
def double_list(x):
    for i in range(0, len(x)):
        x[i] = x[i] * 2
    return x
```

indentation is crucial, will fail if the return keyword is not indented back from the loop

2 ways to iterate through a list:

Method 1 - for item in list:

```
for item in list:
    print item
```    

Method 2 - iterate through indexes:

```
for i in range(len(list)):
    print list[i]
```

`range()` produces lists of the length you pass as a param

```
range(6) # => [0,1,2,3,4,5]
range(1,6) # => [1,2,3,4,5]
range(1,6,3) # => [1,4]
The range function has three different versions:

range(stop)
range(start, stop)
range(start, stop, step)
```

#For loops

for loops different from JS

A variable name follows the `for` word; it will be assigned the value for each in the list in turn.

```
my_list = [1,9,3,8,5,7]

for number in my_list:
    print 2 * number

```


```
start_list = [5, 3, 1, 2, 4]
square_list = []

# Your code here!

for number in start_list:
    square_list.append(number ** 2)
square_list.sort()
print square_list

```

functions with loops

```
def count_small(numbers):
    total = 0
    for n in numbers:
        if n < 10:
            total = total + 1
    return total

lost = [4, 8, 15, 16, 23, 42]
small = count_small(lost)
print small
```

a list of lists within a functions

```
n = [[1, 2, 3], [4, 5, 6, 7, 8, 9]]
# Add your function here
def flatten(lst):
    results=[]
    for number in lst:
        for n in number:
            results.append(n)
    return results
```

#While loops

```
while count < 10:
    print "Hello, I am a while and count is", count
    count += 1
```
```
count = 0

while True:
    print count
    count += 1
    if count >= 10:
        break
```

While/ else statement is completely different in python... The else block will evalutate anytime the while block evaluates to false

```
import random

print "Lucky Numbers! 3 numbers will be generated."
print "If one of them is a '5', you lose!"

count = 0
while count < 3:
    num = random.randint(1, 6)
    print num
    if num == 5:
        print "Sorry, you lose!"
        break
    count += 1
else:
    print "You win!"
```

alertative sytax using for loop

```
print "Counting..."

for i in range(20):
    print i

```

to loop over a dictionary printing the key and then the value.

```
d = {'a': 'apple', 'b': 'berry', 'c': 'cherry'}

for key in d:
    # Your code here!
    print key, d[key]
```

`.zip(list1,list2)` creates pairs of elements when passed two lists, and will stop at the end of the shorter lists
zip can handle 3 or more lists.

```
fruits = ['banana', 'apple', 'orange', 'tomato', 'pear', 'grape']

print 'You have...'
for f in fruits:
    if f == 'tomato':
        print 'A tomato is not a fruit!' # (It actually is.)

    print 'A', f
else:
    print 'A fine selection of fruits!'

```
A weakness of using this for-each style of iteration is that you don't know the index of the thing you're looking at. Generally this isn't an issue, but at times it is useful to know how far into the list you are. Thankfully the built-in `enumerate` function helps with this.

`enumerate` works by supplying a corresponding index to each element in the list that you pass it.

```
choices = ['pizza', 'pasta', 'salad', 'nachos']

print 'Your choices are:'
for index, item in enumerate(choices):
    print index+1, item
```



#Dictionaries

Ruby hashes?!

a key can be any string or number

`d = {'key1' : 1, 'key2' : 2, 'key3' : 3}`

access in the same way as a dictionary


```
residents = {'Puffin' : 104, 'Sloth' : 105, 'Burmese Python' : 106}

print residents['Puffin'] # Prints Puffin's room number
```

like Lists Dictionaries are mutable, can be changed after they are created

`dict_name[new_key] = new_value`


```
menu = {} # Empty dictionary
menu['Chicken Alfredo'] = 14.50 # Adding new key-value pair
```

lists can be added to Dictionaries.

items can be removed from Dictionaries with the `del` keyword
`del dict_name[key_name]` deletes and entry
`dict_name[key] = new_value` assigns a new value



```
my_dict = {
    "fish": ["c", "a", "r", "p"],
    "cash": -4483,
    "luck": "good"
}
print my_dict["fish"][0]
```

prints out 'c'


```
shopping_list = ["banana", "orange", "apple"]

stock = {
    "banana": 6,
    "apple": 0,
    "orange": 32,
    "pear": 15
}

prices = {
    "banana": 4,
    "apple": 2,
    "orange": 1.5,
    "pear": 3
}

# Write your code below!
def compute_bill(food):
    total = 0
    for item in food:
        if stock[item] > 0:
            stock[item]-=1
            total += prices[item]
    return total
```

The `\` character is a continuation character. The following line is considered a continuation of the current line.
