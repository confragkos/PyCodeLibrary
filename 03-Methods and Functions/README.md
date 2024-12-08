## Function

```python
def name_of_function(arg1,arg2):
    '''
    This is where the function's Document String (docstring) goes.
    When you call help() on your function it will be printed out.
    '''
    # Do stuff here
    # Return desired result
    # Return stuff
```


# Lambda Expressions, Map, and Filter

##The **map** function allows you to "map" a function to an iterable object. That is to say you can quickly call the same function to every item in an iterable, such as a list. For example:


```python
def square(num):
    return num**2

my_nums = [1,2,3,4,5]


# To get the results, either iterate through map() 
# or just cast to a list
list(map(square,my_nums))  #[1, 4, 9, 16, 25]
```

## filter function

The filter function returns an iterator yielding those items of iterable for which function(item)
is true. Meaning you need to filter by a function that returns either True or False. Then passing that into filter (along with your iterable) and you will get back only the results that would return True when passed to the function.

```python
def check_even(num):
    return num % 2 == 0 

nums = [0,1,2,3,4,5,6,7,8,9,10]
list(filter(check_even,nums)) #[0, 2, 4, 6, 8, 10]
```

## lambda expression

One of Pythons most useful tools is the lambda expression. lambda expressions allow us to create "anonymous" functions. This basically means we can quickly make ad-hoc functions without needing to properly define a function using def.

```python
def square(num):
    result = num**2
    return result

square(2)

#So why would use this? Many function calls need a function passed in, such as map and filter. Often you only need to use the function you are passing in once, so instead of formally defining it, you just use the #lambda expression. Let's repeat some of the examples from above with a lambda expression
list(map(lambda num: num ** 2, my_nums)) #[1, 4, 9, 16, 25]
```

# `*args` and `**kwargs`
## `*args`

When a function parameter starts with an asterisk, it allows for an *arbitrary number* of arguments, and the function takes them in as a tuple of values. Rewriting the above function:

```python
def myfunc(*args):
    return sum(args)*.05

myfunc(40,60,20)
```
## `**kwargs`

Similarly, Python offers a way to handle arbitrary numbers of *keyworded* arguments. Instead of creating a tuple of values, `**kwargs` builds a dictionary of key/value pairs. For example:

```python
def myfunc(**kwargs):
    if 'fruit' in kwargs:
        print(f"My favorite fruit is {kwargs['fruit']}")  # review String Formatting and f-strings if this syntax is unfamiliar
    else:
        print("I don't like fruit")
        
myfunc(fruit='pineapple') # My favorite fruit is pineapple
```

