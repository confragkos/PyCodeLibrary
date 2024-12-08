# Introduction to Python Statements

## if, elif, else Statements

```python
person = 'George'

if person == 'Sammy':
    print('Welcome Sammy!')
elif person =='George':
    print('Welcome George!')
else:
    print("Welcome, what's your name?")
```

## for Loops

```python
list1 = [1,2,3,4,5,6,7,8,9,10]
for num in list1:
    print(num)

```

## while Loops

```python
x = 0

while x < 10:
    print('x is currently: ',x)
    print(' x is still less than 10, adding 1 to x')
    x+=1
else:
    print('All Done!')


while x < 10:
    print('x is currently: ',x)
    print(' x is still less than 10, adding 1 to x')
    x+=1
    if x==3:
        print('Breaking because x==3')
        break
    else:
        print('continuing...')
        continue
```

## range

The range function allows you to quickly *generate* a list of integers, this comes in handy a lot, so take note of how to use it! There are 3 parameters you can pass, a start, a stop, and a step size. Let's see some examples:

```python
# Third parameter is step size!
# step size just means how big of a jump/leap/step you 
# take from the starting number to get to the next number.

list(range(0,11,2)) #[0, 2, 4, 6, 8, 10]

```

## enumerate

enumerate is a very useful function to use with for loops. Let's imagine the following situation:

```python
index_count = 0

for letter in 'abcde':
    print("At index {} the letter is {}".format(index_count,letter))
    index_count += 1

#Keeping track of how many loops you've gone through is so common, that enumerate was created so you don't need to worry about creating and updating this index_count or loop_count variable
for i,letter in enumerate('abcde'):
    print("At index {} the letter is {}".format(i,letter))

```

## in operator

We've already seen the **in** keyword during the for loop, but we can also use it to quickly check if an object is in a list

```python
'x' in ['x','y','z'] # True or False
```

## Also there methods like not in, min and max

# List Comprehensions


```python
# Square numbers in range and turn into list
lst = [x**2 for x in range(0,11)]
#[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```



