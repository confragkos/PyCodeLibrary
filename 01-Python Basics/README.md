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
```
