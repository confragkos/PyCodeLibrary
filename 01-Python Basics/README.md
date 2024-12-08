## Dynamic Typing

Python uses *dynamic typing*, meaning you can reassign variables to different data types. This makes Python very flexible in assigning data types; it differs from other languages that are *statically typed*.

```python 
my_dogs = 2
print(my_dogs) # 2

my_dogs = ['Rex', 'Aris']
print(my_dogs) # 'Rex', 'Aris'
```


#### Cons of Dynamic Typing
* may result in unexpected bugs!
* you need to be aware of `type()`


## Determining variable type with `type()`
You can check what type of object is assigned to a variable using Python's built-in `type()` function. Common data types include:
* **int** (for integer)
* **float**
* **str** (for string)
* **list**
* **tuple**
* **dict** (for dictionary)
* **set**
* **bool** (for Boolean True/False)

# Strings

```python 
string_a = "Now I'm ready to use the single quotes inside a string!"

# length of the string
len('Hello World') 

# String Indexing, we should also note that indexing starts at 0 for Python

s = 'Hello World'

s[0] # H
s[1:] # 'ello World'

# Grab everything UP TO the 3rd index
s[:3] #  'Hel'


# Grab everything but the last letter
s[:-1] # 'Hello Worl'

# Grab everything, but go in step sizes of 2
s[::2] # 'HloWrd'



# We can use this to print a string backwards
s[::-1]  # 'dlroW olleH'

# Basic Built-in String methods

# Upper Case a string
s.upper()

# Lower case
s.lower()

# Split a string by blank space (this is the default)
# 'hello world concatenate me!' -> ['Hello', 'World', 'concatenate', 'me!']
s.split()

# Split by a specific element (doesn't include the element that was split on)
# 'hello world concatenate me!' -> ['Hello ', 'orld concatenate me!']
s.split('W') 


# Print Formatting

# We can use the .format() method to add formatted objects to printed string statements.

# The easiest way to show this is through an example:

'Insert another string with curly brackets: {}'.format('The inserted string')
```

# String Formatting

#### Inserted objects can be assigned keywords:
```python
print('First Object: {a}, Second Object: {b}, Third Object: {c}'.format(a=1,b='Two',c=12.3))
#print('First Object: {a}, Second Object: {b}, Third Object: {c}'.format(a=1,b='Two',c=12.3))
```

## Formatted String Literals (f-strings)
```python
name = 'Fred'

print(f"He said his name is {name}.") # He said his name is Fred.

print(f"He said his name is {name!r}") # print(f"He said his name is {name!r}")
```


# Lists
```python
# Grab element at index 0
my_list[0]

# Grab index 1 and everything past it
my_list[1:]

# We can also use + to concatenate lists, just like we did for strings.

my_list + ['new item']  # This doesn't actually change the original list!

# You would have to reassign the list to make the change permanent.

# Reassign
my_list = my_list + ['add new item permanently']

# Use the **append** method to permanently add an item to the end of a list:
list1.append('append me!')

# Use **pop** to "pop off" an item from the list. By default pop takes off the last index, but you can also specify which index to pop off. Let's see an example:
list1.pop(0)

# Use sort to sort the list (in this case alphabetical order, but for numbers it will go ascending)
new_list.sort()
```

## Nesting Lists
A great feature of of Python data structures is that they support *nesting*. This means we can have data structures within data structures. For example: A list inside a list.

```python
# Let's make three lists
lst_1=[1,2,3]
lst_2=[4,5,6]
lst_3=[7,8,9]

# Make a list of lists to form a matrix
matrix = [lst_1,lst_2,lst_3]

# Grab first item in matrix object
matrix[0] # [1,2,3]

# Grab first item of the first item in the matrix object
matrix[0][0] # 1
```

# Dictionaries

We've been learning about *sequences* in Python but now we're going to switch gears and learn about *mappings* in Python. If you're familiar with other languages you can think of these Dictionaries as hash tables. 

This section will serve as a brief introduction to dictionaries and consist of:

    1.) Constructing a Dictionary
    2.) Accessing objects from a dictionary
    3.) Nesting Dictionaries
    4.) Basic Dictionary Methods

So what are mappings? Mappings are a collection of objects that are stored by a *key*, unlike a sequence that stored objects by their relative position. This is an important distinction, since mappings won't retain order since they have objects defined by a key.

A Python dictionary consists of a key and then an associated value. That value can be almost any Python object.

```python
# Make a dictionary with {} and : to signify a key and a value
my_dict = {'key1':'value1','key2':'value2'}

my_dict['key2'] # value2

# Its important to note that dictionaries are very flexible in the data types they can hold. For example:
my_dict = {'key1':123,'key2':[12,23,33],'key3':['item0','item1','item2']}
# Can call an index on that value
my_dict['key3'][0] # item0

# We can also create keys by assignment. For instance if we started off with an empty dictionary, we could continually add to it:

# Create a new dictionary
d = {}

# Create a new key through assignment
d['animal'] = 'Dog'

# Can do this with any object
d['answer'] = 42
print(d) # {'animal': 'Dog', 'answer': 42}
```

## A few Dictionary Methods

There are a few methods we can call on a dictionary. Let's get a quick introduction to a few of them:

```python
# Create a typical dictionary
d = {'key1':1,'key2':2,'key3':3}

# Method to return a list of all keys 
d.keys()

# Method to grab all values
d.values()

# Method to return tuples of all items
d.items()
```

# Tuples

In Python tuples are very similar to lists, however, unlike lists they are *immutable* meaning they can not be changed. You would use tuples to present things that shouldn't be changed, such as days of the week, or dates on a calendar. 

```python
t = (1,2,3)
# Can also mix object types
t = ('one',2)

# Use .index to enter a value and return the index
t.index('one') # 0

# Use .count to count the number of times a value appears
t.count('one') # 1
```
## When to use Tuples

You may be wondering, "Why bother using tuples when they have fewer available methods?" To be honest, tuples are not used as often as lists in programming, but are used when immutability is necessary. If in your program you are passing around an object and need to make sure it does not get changed, then a tuple becomes your solution. It provides a convenient source of data integrity.

You should now be able to create and use tuples in your programming as well as have an understanding of their immutability.


# Sets

Sets are an unordered collection of *unique* elements. We can construct them by using the set() function. Let's go ahead and make a set to see how it works
```python
x = set()
# We add to sets with the add() method
x.add(1)
x.add(2)

# Create a list with repeats
list1 = [1,1,2,2,3,4,5,6,1,1]
# Cast as set to get unique values
set(list1)


```

# Comparison Operators 

In this lecture we will be learning about Comparison Operators in Python. These operators will allow us to compare variables and output a Boolean value (True or False). 

If you have any sort of background in Math, these operators should be very straight forward.

First we'll present a table of the comparison operators and then work through some examples:

<h2> Table of Comparison Operators </h2><p>  In the table below, a=3 and b=4.</p>

<table class="table table-bordered">
<tr>
<th style="width:10%">Operator</th><th style="width:45%">Description</th><th>Example</th>
</tr>
<tr>
<td>==</td>
<td>If the values of two operands are equal, then the condition becomes true.</td>
<td> (a == b) is not true.</td>
</tr>
<tr>
<td>!=</td>
<td>If values of two operands are not equal, then condition becomes true.</td>
<td>(a != b) is true</td>
</tr>
<tr>
<td>&gt;</td>
<td>If the value of left operand is greater than the value of right operand, then condition becomes true.</td>
<td> (a &gt; b) is not true.</td>
</tr>
<tr>
<td>&lt;</td>
<td>If the value of left operand is less than the value of right operand, then condition becomes true.</td>
<td> (a &lt; b) is true.</td>
</tr>
<tr>
<td>&gt;=</td>
<td>If the value of left operand is greater than or equal to the value of right operand, then condition becomes true.</td>
<td> (a &gt;= b) is not true. </td>
</tr>
<tr>
<td>&lt;=</td>
<td>If the value of left operand is less than or equal to the value of right operand, then condition becomes true.</td>
<td> (a &lt;= b) is true. </td>
</tr>
</table>

