# Complete Python Tutorial

Checking Python Version


```python
!python --version
```

    Python 3.5.4
    

# Printing in python


```python
print("Hello World")
```

    Hello World
    

# Python Indentation
Python uses indentation to indicate a block of code.


```python
if 5 > 2:
  print("Five is greater than two!")
```

    Five is greater than two!
    

- Python will give you an error if you skip the indentation.
- The number of spaces is up to you as a programmer, but it has to be at least one.
- You have to use the same number of spaces in the same block of code, otherwise Python will give you an error:

# Python Comments

Comments starts with a #, and Python will ignore them:


```python
#This is a comment
print("Hello, World!")
```

    Hello, World!
    

Comments can be placed at the end of a line, and Python will ignore the rest of the line:


```python
print("Hello, World!") #This is a comment
```

    Hello, World!
    

# Multi Line Comments


```python
"""
This is a comment
written in
more than just one line
"""
print("Hello, World!")
```

    Hello, World!
    

# Python Variables

## Creating Variables

A variable is created the moment you first assign a value to it.


```python
x = 5
y = "John"
print(x)
print(y)
```

    5
    John
    

Variables do not need to be declared with any particular type and can even change type after they have been set.


```python
x = 4 # x is of type int
x = "Sally" # x is now of type str
print(x)
```

    Sally
    

String variables can be declared either by using single or double quotes:


```python
x = "John"
# is the same as
x = 'John'
```

## Variable Names

A variable can have a short name (like x and y) or a more descriptive name (age, carname, total_volume). Rules for Python variables:
- A variable name must start with a letter or the underscore character
- A variable name cannot start with a number
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
- Variable names are case-sensitive (age, Age and AGE are three different variables)


```python
#Legal variable names:
myvar = "John"
my_var = "John"
_my_var = "John"
myVar = "John"
MYVAR = "John"
myvar2 = "John"

#Illegal variable names:
2myvar = "John"
my-var = "John"
my var = "John"
```


      File "<ipython-input-247-a23a3e8b2732>", line 10
        2myvar = "John"
             ^
    SyntaxError: invalid syntax
    


## Assign Value to Multiple Variables

Python allows you to assign values to multiple variables in one line:


```python
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

And you can assign the same value to multiple variables in one line:


```python
x = y = z = "Orange"
print(x)
print(y)
print(z)
```

## Output Variables

The Python print statement is often used to output variables.

To combine both text and a variable, Python uses the + character:


```python
x = "awesome"
print("Python is " + x)
```

You can also use the + character to add a variable to another variable:


```python
x = "Python is "
y = "awesome"
z =  x + y
print(z)
```

For numbers, the + character works as a mathematical operator:


```python
x = 5
y = 10
print(x + y)
```

## Global Variables

Variables that are created outside of a function (as in all of the examples above) are known as global variables.

Global variables can be used by everyone, both inside of functions and outside.


```python
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
```

If you create a variable with the same name inside a function, this variable will be local, and can only be used inside the function. The global variable with the same name will remain as it was, global and with the original value.


```python
x = "awesome"

def myfunc():
  x = "fantastic"
  print("Python is " + x)

myfunc()

print("Python is " + x)
```

## The global Keyword

Normally, when you create a variable inside a function, that variable is local, and can only be used inside that function.

To create a global variable inside a function, you can use the global keyword.


```python
def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

Also, use the global keyword if you want to change a global variable inside a function.
To change the value of a global variable inside a function, refer to the variable by using the global keyword.


```python
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

# Python Data Types

## Built-in Data Types

Python has the following data types built-in by default, in these categories:  

    - Text Type         :str  
    - Numeric Types     :int, float, complex  
    - Sequence Types    :list, tuple, range  
    - Mapping Type      :dict  
    - Set Types         :set, frozenset  
    - Boolean Type      :bool  
    - Binary Types      :bytes, bytearray, memoryview  

You can get the data type of any object by using the type() function:


```python
x = 5
print(type(x))
```


```python
x = "Hello World"
print(type(x))

```


```python
x = 20
print(type(x))
```


```python
x = 20.5
print(type(x))
```


```python
x = 1j
print(type(x))
```


```python
x = ["apple", "banana", "cherry"]
print(type(x))
```


```python
x = ("apple", "banana", "cherry")
print(type(x))
```


```python
x = range(6)
print(type(x))
```


```python
x = {"name" : "John", "age" : 36}
print(type(x))
```


```python
x = {"apple", "banana", "cherry"}
print(type(x))
```


```python
x = frozenset({"apple", "banana", "cherry"})
print(type(x))
```


```python
x = True
print(type(x))
```


```python
x = b"Hello"
print(type(x))
```


```python
x = bytearray(5)
print(type(x))
```


```python
x = memoryview(bytes(5))
print(type(x))
```

## Setting the Specific Data Type

If you want to specify the data type, you can use the following constructor functions:


```python
x = str("Hello World")
print(x)
print(type(x))
```


```python
x = int(20)
print(x)
print(type(x))
```


```python
x = float(20.5)
print(x)
print(type(x))
```


```python
x = complex(1j)
print(x)
print(type(x))
```


```python
x = list(("apple", "banana", "cherry"))
print(x)
print(type(x))
```


```python
x = tuple(("apple", "banana", "cherry"))
print(x)
print(type(x))
```


```python
x = range(6)
print(x)
print(type(x))
```


```python
x = dict(name="John", age=36)
print(x)
print(type(x))
```


```python
x = set(("apple", "banana", "cherry"))
print(x)
print(type(x))
```


```python
x = frozenset(("apple", "banana", "cherry"))
print(x)
print(type(x))
```


```python
x = bool(5)
print(x)
print(type(x))
```


```python
x = bytes(5)
print(x)
print(type(x))
```


```python
x = bytearray(5)
print(x)
print(type(x))
```


```python
x = memoryview(bytes(5))
print(x)
print(type(x))
```

# Python Numbers

## Int
Int, or integer, is a whole number, positive or negative, without decimals, of unlimited length.


```python
x = 1
y = 35656222554887711
z = -3255522

print(type(x))
print(type(y))
print(type(z))
```

## Float
Float, or "floating point number" is a number, positive or negative, containing one or more decimals.


```python
x = 1.10
y = 1.0
z = -35.59
print(x)
print(type(x))
print(y)
print(type(y))
print(z)
print(type(z))
```

Float can also be scientific numbers with an "e" to indicate the power of 10.


```python
x = 35e3
y = 12E4
z = -87.7e100

print(x)
print(type(x))
print(y)
print(type(y))
print(z)
print(type(z))
```

## Complex
Complex numbers are written with a "j" as the imaginary part:


```python
x = 3+5j
y = 5j
z = -5j

print(x)
print(type(x))
print(y)
print(type(y))
print(z)
print(type(z))
```

## Type Conversion
You can convert from one type to another with the int(), float(), and complex() methods:


```python
x = 1 # int
y = 2.8 # float
z = 1j # complex

#convert from int to float:
a = float(x)

#convert from float to int:
b = int(y)

#convert from int to complex:
c = complex(x)

print(a)
print(b)
print(c)

print(type(a))
print(type(b))
print(type(c))
```

## Random Number
Python does not have a random() function to make a random number, but Python has a built-in module called random that can be used to make random numbers:


```python
import random

print(random.randrange(1,10))
```

# Python Casting

## Specify a Variable Type

There may be times when you want to specify a type on to a variable. This can be done with casting. Python is an object-orientated language, and as such it uses classes to define data types, including its primitive types.

Casting in python is therefore done using constructor functions:
- int() - constructs an integer number from an integer literal, a float literal (by rounding down to the previous whole number), or a string literal (providing the string represents a whole number)
- float() - constructs a float number from an integer literal, a float literal or a string literal (providing the string represents a float or an integer)
- str() - constructs a string from a wide variety of data types, including strings, integer literals and float literals


```python
x = int(1)   # x will be 1
y = int(2.8) # y will be 2
z = int("3") # z will be 3
```


```python
x = float(1)     # x will be 1.0
y = float(2.8)   # y will be 2.8
z = float("3")   # z will be 3.0
w = float("4.2") # w will be 4.2
```


```python
x = str("s1") # x will be 's1'
y = str(2)    # y will be '2'
z = str(3.0)  # z will be '3.0'
```

# Python Strings

## String Literals
String literals in python are surrounded by either single quotation marks, or double quotation marks.

'hello' is the same as "hello".

You can display a string literal with the print() function:


```python
print("Hello")
print('Hello')
```

    Hello
    Hello
    

## Assign String to a Variable
Assigning a string to a variable is done with the variable name followed by an equal sign and the string:


```python
a = "Hello"
print(a)
```

    Hello
    

## Multiline Strings
You can assign a multiline string to a variable by using three quotes:


```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```

    Lorem ipsum dolor sit amet,
    consectetur adipiscing elit,
    sed do eiusmod tempor incididunt
    ut labore et dolore magna aliqua.
    

Or three single quotes:


```python
a = '''Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.'''
print(a)
```

    Lorem ipsum dolor sit amet,
    consectetur adipiscing elit,
    sed do eiusmod tempor incididunt
    ut labore et dolore magna aliqua.
    

## Strings are Arrays
Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters.

However, Python does not have a character data type, a single character is simply a string with a length of 1.

Square brackets can be used to access elements of the string.


```python
#Get the character at position 1 (remember that the first character has the position 0):
a = "Hello, World!"
print(a[1])
```

    e
    

## Slicing
You can return a range of characters by using the slice syntax.

Specify the start index and the end index, separated by a colon, to return a part of the string.


```python
b = "Hello, World!"
print(b[2:5])
```

    llo
    

## Negative Indexing
Use negative indexes to start the slice from the end of the string:


```python
b = "Hello, World!"
print(b[-5:-2])
```

    orl
    

## String Length
To get the length of a string, use the len() function.


```python
a = "Hello, World!"
print(len(a))
```

    13
    

## String Methods
Python has a set of built-in methods that you can use on strings.


```python
# The strip() method removes any whitespace from the beginning or the end:
a = " Hello, World! "
print(a.strip()) # returns "Hello, World!"
```

    Hello, World!
    


```python
#The lower() method returns the string in lower case:
a = "Hello, World!"
print(a.lower())
```

    hello, world!
    


```python
#The upper() method returns the string in upper case:
a = "Hello, World!"
print(a.upper())
```

    HELLO, WORLD!
    


```python
#The replace() method replaces a string with another string:
a = "Hello, World!"
print(a.replace("H", "J"))
```

    Jello, World!
    


```python
#The split() method splits the string into substrings if it finds instances of the separator:
a = "Hello, World!"
print(a.split(",")) # returns ['Hello', ' World!']
```

    ['Hello', ' World!']
    

## Check String
To check if a certain phrase or character is present in a string, we can use the keywords in or not in.


```python
# Check if the phrase "ain" is present in the following text:
txt = "The rain in Spain stays mainly in the plain"
x = "ain" in txt
print(x)
```

    True
    


```python
# Check if the phrase "ain" is NOT present in the following text:
txt = "The rain in Spain stays mainly in the plain"
x = "ain" not in txt
print(x) 
```

    False
    

## String Concatenation
To concatenate, or combine, two strings you can use the + operator.


```python
# Merge variable a with variable b into variable c:
a = "Hello"
b = "World"
c = a + b
print(c)
```

    HelloWorld
    


```python
# To add a space between them, add a " ":
a = "Hello"
b = "World"
c = a + " " + b
print(c)
```

    Hello World
    

## String Format
We cannot combine strings and numbers like this:


```python
# age = 36
# txt = "My name is John, I am " + age
# print(txt)
```

But we can combine strings and numbers by using the format() method!

The format() method takes the passed arguments, formats them, and places them in the string where the placeholders {} are:


```python
# Use the format() method to insert numbers into strings:
age = 36
txt = "My name is John, and I am {}"
print(txt.format(age))
```

    My name is John, and I am 36
    

The format() method takes unlimited number of arguments, and are placed into the respective placeholders:


```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want {} pieces of item {} for {} dollars."
print(myorder.format(quantity, itemno, price))
```

    I want 3 pieces of item 567 for 49.95 dollars.
    

You can use index numbers {0} to be sure the arguments are placed in the correct placeholders:


```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemno, price))
```

    I want to pay 49.95 dollars for 3 pieces of item 567.
    

## Escape Character
To insert characters that are illegal in a string, use an escape character.

An escape character is a backslash \ followed by the character you want to insert.

An example of an illegal character is a double quote inside a string that is surrounded by double quotes:


```python
# txt = "We are the so-called "Vikings" from the north."
```


```python
# To fix this problem, use the escape character \":
# The escape character allows you to use double quotes when you normally would not be allowed:
txt = "We are the so-called \"Vikings\" from the north."
```


```python
txt = 'It\'s alright.'
print(txt) 
```

    It's alright.
    


```python
txt = "This will insert one \\ (backslash)."
print(txt) 
```

    This will insert one \ (backslash).
    


```python
txt = "Hello\nWorld!"
print(txt) 
```

    Hello
    World!
    


```python
txt = "Hello\rWorld!"
print(txt) 
```

    World!
    


```python
txt = "Hello\tWorld!"
print(txt) 
```

    Hello	World!
    


```python
#This example erases one character (backspace):
txt = "Hello \bWorld!"
print(txt) 
```

    Hello World!
    


```python
#A backslash followed by three integers will result in a octal value:
txt = "\110\145\154\154\157"
print(txt)
```

    Hello
    


```python
#A backslash followed by an 'x' and a hex number represents a hex value:
txt = "\x48\x65\x6c\x6c\x6f"
print(txt) 
```

    Hello
    

## String Methods

Method	Description
    - capitalize():	    Converts the first character to upper case
    - casefold():	    Converts string into lower case
    - center():	        Returns a centered string
    - count():	        Returns the number of times a specified value occurs in a string
    - encode():	        Returns an encoded version of the string
    - endswith():	    Returns true if the string ends with the specified value
    - expandtabs():	    Sets the tab size of the string
    - find():	        Searches the string for a specified value and returns the position of where it was found
    - format():	        Formats specified values in a string
    - format_map():	    Formats specified values in a string
    - index():	        Searches the string for a specified value and returns the position of where it was found
    - isalnum():	    Returns True if all characters in the string are alphanumeric
    - isalpha():	    Returns True if all characters in the string are in the alphabet
    - isdecimal():	    Returns True if all characters in the string are decimals
    - isdigit():	    Returns True if all characters in the string are digits
    - isidentifier():	Returns True if the string is an identifier
    - islower():	    Returns True if all characters in the string are lower case
    - isnumeric():	    Returns True if all characters in the string are numeric
    - isprintable():	Returns True if all characters in the string are printable
    - isspace():	    Returns True if all characters in the string are whitespaces
    - istitle():	    Returns True if the string follows the rules of a title
    - isupper():	    Returns True if all characters in the string are upper case
    - join():	        Joins the elements of an iterable to the end of the string
    - ljust():	        Returns a left justified version of the string
    - lower():	        Converts a string into lower case
    - lstrip():	        Returns a left trim version of the string
    - maketrans():	    Returns a translation table to be used in translations
    - partition():	    Returns a tuple where the string is parted into three parts
    - replace():	    Returns a string where a specified value is replaced with a specified value
    - rfind():	        Searches the string for a specified value and returns the last position of where it was found
    - rindex():	        Searches the string for a specified value and returns the last position of where it was found
    - rjust():	        Returns a right justified version of the string
    - rpartition():	    Returns a tuple where the string is parted into three parts
    - rsplit():	        Splits the string at the specified separator, and returns a list
    - rstrip():	        Returns a right trim version of the string
    - split():	        Splits the string at the specified separator, and returns a list
    - splitlines():	    Splits the string at line breaks and returns a list
    - startswith():	    Returns true if the string starts with the specified value
    - strip():	        Returns a trimmed version of the string
    - swapcase():	    Swaps cases, lower case becomes upper case and vice versa
    - title():	        Converts the first character of each word to upper case
    - translate():	    Returns a translated string
    - upper():	        Converts a string into upper case
    - zfill():	        Fills the string with a specified number of 0 values at the beginning

# Python Booleans

Booleans represent one of two values: True or False.

### Boolean Values
In programming you often need to know if an expression is True or False.  
You can evaluate any expression in Python, and get one of two answers, True or False.  
When you compare two values, the expression is evaluated and Python returns the Boolean answer.


```python
print(10 > 9)
print(10 == 9)
print(10 < 9)
```

    True
    False
    False
    

### When you run a condition in an if statement, Python returns True or False: 


```python
# Print a message based on whether the condition is True or False:
a = 200
b = 33

if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```

    b is not greater than a
    

### Evaluate Values and Variables
The bool() function allows you to evaluate any value, and give you True or False in return,


```python
print(bool("Hello"))
print(bool(15))
```

    True
    True
    


```python
x = "Hello"
y = 15

print(bool(x))
print(bool(y))
```

    True
    True
    

#### Most Values are True
Almost any value is evaluated to True if it has some sort of content.

Any string is True, except empty strings.

Any number is True, except 0.

Any list, tuple, set, and dictionary are True, except empty ones.


```python
print(bool("abc"))
print(bool(123))
print(bool(["apple", "cherry", "banana"]))
```

    True
    True
    True
    

#### Some Values are False
In fact, there are not many values that evaluates to False, except empty values, such as (), [], {}, "", the number 0, and the value None. And of course the value False evaluates to False.


```python
print(bool(False))
print(bool(None))
print(bool(0))
print(bool(""))
print(bool(()))
print(bool([]))
print(bool({}))
```

    False
    False
    False
    False
    False
    False
    False
    

One more value, or object in this case, evaluates to False, and that is if you have an object that is made from a class with a __len__ function that returns 0 or False:


```python
class myclass():
  def __len__(self):
    return 0

myobj = myclass()
print(bool(myobj))
```

    False
    

### Functions can Return a Boolean
You can create functions that returns a Boolean Value:


```python
def myFunction() :
  return True

print(myFunction())
```

    True
    


```python
def myFunction() :
  return True

if myFunction():
  print("YES!")
else:
  print("NO!")
```

    YES!
    


```python
x = 200
print(isinstance(x, int))
```

    True
    

# Python Operators

Operators are used to perform operations on variables and values.

Python divides the operators in the following groups:

- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Identity operators
- Membership operators
- Bitwise operators

### Python Arithmetic Operators


```python
x = 5
y = 3
print(x + y)
```

    8
    


```python
x = 5
y = 3
print(x - y)
```

    2
    


```python
x = 5
y = 3
print(x * y)
```

    15
    


```python
x = 12
y = 3
print(x / y)
```

    4.0
    


```python
x = 5
y = 2
print(x % y)
```

    1
    


```python
x = 2
y = 5
print(x ** y) #same as 2*2*2*2*2
```

    32
    


```python
x = 15
y = 2
print(x // y)
#the floor division // rounds the result down to the nearest whole number
```

    7
    

### Python Assignment Operators


```python
x = 5

print(x)

```

    5
    


```python
x = 5

x += 3

print(x)

```

    8
    


```python
x = 5

x -= 3

print(x)
```

    2
    


```python
x = 5

x *= 3

print(x)
```

    15
    


```python
x = 5

x /= 3

print(x)

```

    1.6666666666666667
    


```python
x = 5

x%=3

print(x)

```

    2
    


```python
x = 5

x//=3

print(x)
```

    1
    


```python
x = 5

x **= 3

print(x)
```

    125
    


```python
x = 5

x &= 3

print(x)
```

    1
    


```python
x = 5

x |= 3

print(x)
```

    7
    


```python
x = 5

x ^= 3

print(x)
```

    6
    


```python
x = 5

x >>= 3

print(x)
```

    0
    


```python
x = 5

x <<= 3

print(x)
```

    40
    

### Python Comparison Operators


```python
x = 5
y = 3
# Equal
print(x == y)

# returns False because 5 is not equal to 3
```

    False
    


```python
x = 5
y = 3
# Not equal
print(x != y)

# returns True because 5 is not equal to 3
```

    True
    


```python
x = 5
y = 3
# Greater than
print(x > y)

# returns True because 5 is greater than 3
```

    True
    


```python
x = 5
y = 3
# Less than
print(x < y)

# returns False because 5 is not less than 3
```

    False
    


```python
x = 5
y = 3
# Greater than or equal to
print(x >= y)

# returns True because five is greater, or equal, to 3
```

    True
    


```python
x = 5
y = 3
# Less than or equal to
print(x <= y)

# returns False because 5 is neither less than or equal to 3
```

    False
    

### Python Logical Operators


```python
x = 5
# Returns True if both statements are true
print(x > 3 and x < 10)

# returns True because 5 is greater than 3 AND 5 is less than 10
```

    True
    


```python
x = 5
# Returns True if one of the statements is true
print(x > 3 or x < 4)

# returns True because one of the conditions are true (5 is greater than 3, but 5 is not less than 4)
```

    True
    


```python
x = 5
# Reverse the result, returns False if the result is true
print(not(x > 3 and x < 10))

# returns False because not is used to reverse the result
```

    False
    

### Python Identity Operators


```python
# Returns True if both variables are the same object
x = ["apple", "banana"]
y = ["apple", "banana"]
z = x
# is
print(x is z)

# returns True because z is the same object as x
# is
print(x is y)

# returns False because x is not the same object as y, even if they have the same content

print(x == y)

# to demonstrate the difference betweeen "is" and "==": this comparison returns True because x is equal to y
```

    True
    False
    True
    


```python
# Returns True if both variables are not the same object
x = ["apple", "banana"]
y = ["apple", "banana"]
z = x
# is not
print(x is not z)

# returns False because z is the same object as x
# is not
print(x is not y)

# returns True because x is not the same object as y, even if they have the same content

print(x != y)

# to demonstrate the difference betweeen "is not" and "!=": this comparison returns False because x is equal to y
```

    False
    True
    False
    

### Python Membership Operators


```python
# Returns True if a sequence with the specified value is present in the object
x = ["apple", "banana"]
# in
print("banana" in x)

# returns True because a sequence with the value "banana" is in the list
```

    True
    


```python
# Returns True if a sequence with the specified value is not present in the object
x = ["apple", "banana"]
# not in
print("pineapple" not in x)

# returns True because a sequence with the value "pineapple" is not in the list
```

    True
    

### Python Bitwise Operators

Bitwise operators are used to compare (binary) numbers:
        - "&"   :AND                   :Sets each bit to 1 if both bits are 1  
        - "|"   :OR                    :Sets each bit to 1 if one of two bits is 1  
        - "^"   :XOR                   :Sets each bit to 1 if only one of two bits is 1  
        - "~"   :NOT                   :Inverts all the bits  
        - "<<"  :Zero fill left shift  :Shift left by pushing zeros in from the right and let the leftmost bits fall off  
        - ">>"  :Signed right shift    :Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off  

# Python Lists

A list is a collection which is ordered and changeable. In Python lists are written with square brackets.


```python
#Create a List:
thislist = ["apple", "banana", "cherry"]
print(thislist)
```

    ['apple', 'banana', 'cherry']
    

### Access Items


```python
# You access the list items by referring to the index number:
# Print the second item of the list:
thislist = ["apple", "banana", "cherry"]
print(thislist[1])
```

    banana
    

#### Negative Indexing

Negative indexing means beginning from the end, -1 refers to the last item, -2 refers to the second last item etc.


```python
# Print the last item of the list:
thislist = ["apple", "banana", "cherry"]
print(thislist[-1])
```

    cherry
    

#### Range of Indexes
You can specify a range of indexes by specifying where to start and where to end the range.  
When specifying a range, the return value will be a new list with the specified items.


```python
# Return the third, fourth, and fifth item:
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])
```

    ['cherry', 'orange', 'kiwi']
    


```python
# This example returns the items from the beginning to "orange":
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[:4])
```

    ['apple', 'banana', 'cherry', 'orange']
    


```python
# his example returns the items from "cherry" and to the end:
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:])
```

    ['cherry', 'orange', 'kiwi', 'melon', 'mango']
    

#### Range of Negative Indexes
Specify negative indexes if you want to start the search from the end of the list:


```python
# This example returns the items from index -4 (included) to index -1 (excluded)
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[-4:-1])
```

    ['orange', 'kiwi', 'melon']
    

### Change Item Value


```python
# To change the value of a specific item, refer to the index number:
# Change the second item:
thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"
print(thislist)
```

    ['apple', 'blackcurrant', 'cherry']
    

### Loop Through a List

You can loop through the list items by using a for loop:


```python
# Print all items in the list, one by one:
thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x)
```

    apple
    banana
    cherry
    

### Check if Item Exists

To determine if a specified item is present in a list use the in keyword:


```python
# Check if "apple" is present in the list:
thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list")
```

    Yes, 'apple' is in the fruits list
    

### List Length

To determine how many items a list has, use the len() function:


```python
# Print the number of items in the list:
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
```

    3
    

### Add Items

To add an item to the end of the list, use the append() method:


```python
# Using the append() method to append an item:
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)
```

    ['apple', 'banana', 'cherry', 'orange']
    

To add an item at the specified index, use the insert() method:


```python
# Insert an item as the second position:
thislist = ["apple", "banana", "cherry"]
thislist.insert(1, "orange")
print(thislist)
```

    ['apple', 'orange', 'banana', 'cherry']
    

### Remove Item

The remove() method removes the specified item:


```python
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)
```

    ['apple', 'cherry']
    

The pop() method removes the specified index, (or the last item if index is not specified):


```python
thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)
```

    ['apple', 'banana']
    

The del keyword removes the specified index:


```python
thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)
```

    ['banana', 'cherry']
    

The del keyword can also delete the list completely:


```python
thislist = ["apple", "banana", "cherry"]
del thislist
```

The clear() method empties the list:


```python
thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)
```

    []
    

### Copy a List

You cannot copy a list simply by typing ```list2 = list1```, because: ```list2``` will only be a reference to ```list1```, and changes made in ```list1``` will automatically also be made in ```list2```.

There are ways to make a copy, one way is to use the built-in List method copy().

Make a copy of a list with the ```copy()``` method:


```python
thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)
```

    ['apple', 'banana', 'cherry']
    

Make a copy of a list with the ```list()``` method:


```python
thislist = ["apple", "banana", "cherry"]
mylist = list(thislist)
print(mylist)
```

    ['apple', 'banana', 'cherry']
    

### Join Two Lists

One of the easiest ways are by using the + operator.


```python
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list3 = list1 + list2
print(list3)
```

    ['a', 'b', 'c', 1, 2, 3]
    

Another way to join two lists are by appending all the items from list2 into list1, one by one:


```python
# Append list2 into list1:
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

for x in list2:
  list1.append(x)

print(list1)
```

    ['a', 'b', 'c', 1, 2, 3]
    


```python
# Use the extend() method to add list2 at the end of list1:
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list1.extend(list2)
print(list1)
```

    ['a', 'b', 'c', 1, 2, 3]
    

It is also possible to use the list() constructor to make a new list.


```python
# Using the list() constructor to make a List:
thislist = list(("apple", "banana", "cherry")) # note the double round-brackets
print(thislist)
```

    ['apple', 'banana', 'cherry']
    

### List Methods

    - append()   :Adds an element at the end of the list
    - clear()    :Removes all the elements from the list
    - copy()     :Returns a copy of the list
    - count()    :Returns the number of elements with the specified value
    - extend()   :Add the elements of a list (or any iterable), to the end of the current list
    - index()    :Returns the index of the first element with the specified value
    - insert()   :Adds an element at the specified position
    - pop()      :Removes the element at the specified position
    - remove()   :Removes the item with the specified value
    - reverse()  :Reverses the order of the list
    - sort()     :Sorts the list

# Python Tuples

A tuple is a collection which is ordered and unchangeable. In Python tuples are written with round brackets.


```python
# Create a Tuple:
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```

    ('apple', 'banana', 'cherry')
    

### Access Tuple Items

You can access tuple items by referring to the index number, inside square brackets:


```python
# Print the second item in the tuple:
thistuple = ("apple", "banana", "cherry")
print(thistuple[1])
```

    banana
    

#### Negative Indexing

Negative indexing means beginning from the end, -1 refers to the last item, -2 refers to the second last item etc.


```python
# Print the last item of the tuple:
thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])
```

    cherry
    

#### Range of Indexes

You can specify a range of indexes by specifying where to start and where to end the range.  
When specifying a range, the return value will be a new tuple with the specified items.


```python
# Return the third, fourth, and fifth item:
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])
```

    ('cherry', 'orange', 'kiwi')
    

#### Range of Negative Indexes

Specify negative indexes if you want to start the search from the end of the tuple:


```python
# This example returns the items from index -4 (included) to index -1 (excluded)
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[-4:-1])
```

    ('orange', 'kiwi', 'melon')
    

### Change Tuple Values

Once a tuple is created, you cannot change its values. Tuples are unchangeable, or immutable as it also is called.

But there is a workaround. You can convert the tuple into a list, change the list, and convert the list back into a tuple.


```python
# Convert the tuple into a list to be able to change it:
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)

print(x)
```

    ('apple', 'kiwi', 'cherry')
    

### Loop Through a Tuple


```python
# Iterate through the items and print the values:
thistuple = ("apple", "banana", "cherry")
for x in thistuple:
  print(x)
```

    apple
    banana
    cherry
    

### Check if Item Exists


```python
# Check if "apple" is present in the tuple:
thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
  print("Yes, 'apple' is in the fruits tuple")
```

    Yes, 'apple' is in the fruits tuple
    

### Tuple Length


```python
# Print the number of items in the tuple:
thistuple = ("apple", "banana", "cherry")
print(len(thistuple))
```

    3
    

### Add Items

Once a tuple is created, you cannot add items to it. Tuples are unchangeable.

### Create Tuple With One Item

To create a tuple with only one item, you have to add a comma after the item, otherwise Python will not recognize it as a tuple.


```python
# One item tuple, remember the commma:
thistuple = ("apple",)
print(type(thistuple))

#NOT a tuple
thistuple = ("apple")
print(type(thistuple))
```

    <class 'tuple'>
    <class 'str'>
    

### Remove Items

Tuples are unchangeable, so you cannot remove items from it, but you can delete the tuple completely:


```python
# The del keyword can delete the tuple completely:
thistuple = ("apple", "banana", "cherry")
del thistuple
# print(thistuple) #this will raise an error because the tuple no longer exists
```

### Join Two Tuples


```python
# Join two tuples:
tuple1 = ("a", "b" , "c")
tuple2 = (1, 2, 3)

tuple3 = tuple1 + tuple2
print(tuple3)
```

    ('a', 'b', 'c', 1, 2, 3)
    

### The tuple() Constructor


```python
# Using the tuple() method to make a tuple:
thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets
print(thistuple)
```

    ('apple', 'banana', 'cherry')
    

### Tuple Methods

    - count()    :Returns the number of times a specified value occurs in a tuple
    - index()    :Searches the tuple for a specified value and returns the position of where it was found


# Python Sets

A set is a collection which is unordered and unindexed. In Python sets are written with curly brackets.


```python
# Create a Set:
thisset = {"apple", "banana", "cherry"}
print(thisset)
```

    {'cherry', 'apple', 'banana'}
    

### Access Items

You cannot access items in a set by referring to an index, since sets are unordered the items has no index.

But you can loop through the set items using a ```for``` loop, or ask if a specified value is present in a set, by using the ```in``` keyword.


```python
# Loop through the set, and print the values:
thisset = {"apple", "banana", "cherry"}
for x in thisset:
  print(x)
```

    cherry
    apple
    banana
    


```python
#Check if "banana" is present in the set:
thisset = {"apple", "banana", "cherry"}
print("banana" in thisset)
```

    True
    

### Change Items

Once a set is created, you cannot change its items, but you can add new items.

### Add Items

To add one item to a set use the ```add()``` method.

To add more than one item to a set use the ```update()``` method.


```python
# Add an item to a set, using the add() method:
thisset = {"apple", "banana", "cherry"}
thisset.add("orange")
print(thisset)
```

    {'cherry', 'apple', 'banana', 'orange'}
    


```python
# Add multiple items to a set, using the update() method:
thisset = {"apple", "banana", "cherry"}
thisset.update(["orange", "mango", "grapes"])
print(thisset)
```

    {'cherry', 'grapes', 'apple', 'orange', 'banana', 'mango'}
    

### Get the Length of a Set


```python
# Get the number of items in a set:
thisset = {"apple", "banana", "cherry"}
print(len(thisset))
```

    3
    

### Remove Item


```python
# Remove "banana" by using the remove() method:
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana")
print(thisset)
# If the item to remove does not exist, remove() will raise an error.
```

    {'cherry', 'apple'}
    


```python
# Remove "banana" by using the discard() method:
thisset = {"apple", "banana", "cherry"}
thisset.discard("banana")
print(thisset)
# If the item to remove does not exist, discard() will NOT raise an error.
```

    {'cherry', 'apple'}
    

You can also use the ```pop()```, method to remove an item, but this method will remove the last item. Remember that sets are unordered, so you will not know what item that gets removed.

The return value of the ```pop()``` method is the removed item.


```python
# Remove the last item by using the pop() method:
thisset = {"apple", "banana", "cherry"}
x = thisset.pop()
print(x)
print(thisset)
# Sets are unordered, so when using the pop() method, you will not know which item that gets removed.
```

    cherry
    {'apple', 'banana'}
    


```python
# The clear() method empties the set:
thisset = {"apple", "banana", "cherry"}
thisset.clear()
print(thisset)
```

    set()
    


```python
# The del keyword will delete the set completely:
thisset = {"apple", "banana", "cherry"}
del thisset
# print(thisset)
```

### Join Two Sets

You can use the ```union()``` method that returns a new set containing all items from both sets, or the ```update()``` method that inserts all the items from one set into another:


```python
# The union() method returns a new set with all items from both sets:
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}
set3 = set1.union(set2)
print(set3)
```

    {1, 'b', 2, 3, 'a', 'c'}
    


```python
# The update() method inserts the items in set2 into set1:
set2 = {1, 2, 3}
set1.update(set2)
print(set1)
```

    {1, 'b', 2, 3, 'a', 'c'}
    

Both ```union()``` and ```update()``` will exclude any duplicate items.

### The set() Constructor


```python
# Using the set() constructor to make a set:
thisset = set(("apple", "banana", "cherry")) # note the double round-brackets
print(thisset)
```

    {'cherry', 'apple', 'banana'}
    

### Set Methods

    - add()                             :Adds an element to the set
    - clear()	                       :Removes all the elements from the set
    - copy()	                        :Returns a copy of the set
    - difference()	                  :Returns a set containing the difference between two or more sets
    - difference_update()	           :Removes the items in this set that are also included in another, specified set
    - discard()	                     :Remove the specified item
    - intersection()	                :Returns a set, that is the intersection of two other sets
    - intersection_update()	         :Removes the items in this set that are not present in other, specified set(s)
    - isdisjoint()	                  :Returns whether two sets have a intersection or not
    - issubset()	                    :Returns whether another set contains this set or not
    - issuperset()	                  :Returns whether this set contains another set or not
    - pop()	                         :Removes an element from the set
    - remove()	                      :Removes the specified element
    - symmetric_difference()	        :Returns a set with the symmetric differences of two sets
    - symmetric_difference_update()	 :inserts the symmetric differences from this set and another
    - union()	                       :Return a set containing the union of sets
    - update()	                      :Update the set with the union of this set and others

# Python Dictionaries

A dictionary is a collection which is unordered, changeable and indexed. In Python dictionaries are written with curly brackets, and they have keys and values.


```python
# Create and print a dictionary:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```

    {'brand': 'Ford', 'year': 1964, 'model': 'Mustang'}
    

### Accessing Items

You can access the items of a dictionary by referring to its key name, inside square brackets:


```python
# Get the value of the "model" key:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]
```


```python
# Get the value of the "model" key:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict.get("model")
print(x)
```

    Mustang
    

### Change Values

You can change the value of a specific item by referring to its key name:


```python
# Change the "year" to 2018:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict["year"])
thisdict["year"] = 2018
print(thisdict["year"])
```

    1964
    2018
    

### Loop Through a Dictionary

You can loop through a dictionary by using a ```for``` loop.

When looping through a dictionary, the return value are the ```keys``` of the dictionary, but there are methods to return the ```values``` as well.


```python
# Print all key names in the dictionary, one by one:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x in thisdict:
  print(x)
```

    brand
    year
    model
    


```python
# Print all values in the dictionary, one by one:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x in thisdict:
  print(thisdict[x])
```

    Ford
    1964
    Mustang
    


```python
# You can also use the values() method to return values of a dictionary:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x in thisdict.values():
  print(x)
```

    Ford
    1964
    Mustang
    


```python
# Loop through both keys and values, by using the items() method:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x, y in thisdict.items():
  print(x, y)
```

    brand Ford
    year 1964
    model Mustang
    

### Check if Key Exists

To determine if a specified key is present in a dictionary use the ```in``` keyword:


```python
# Check if "model" is present in the dictionary:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
if "model" in thisdict:
  print("Yes, 'model' is one of the keys in the thisdict dictionary")
```

    Yes, 'model' is one of the keys in the thisdict dictionary
    

### Dictionary Length


```python
# Print the number of items in the dictionary:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(len(thisdict))
```

    3
    

### Adding Items


```python
# Adding an item to the dictionary is done by using a new index key and assigning a value to it:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)
```

    {'brand': 'Ford', 'year': 1964, 'color': 'red', 'model': 'Mustang'}
    

### Removing Items


```python
# The pop() method removes the item with the specified key name:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
thisdict.pop("model")
print(thisdict)
```

    {'brand': 'Ford', 'year': 1964, 'model': 'Mustang'}
    {'brand': 'Ford', 'year': 1964}
    


```python
# The popitem() method removes the last inserted item (in versions before 3.7, a random item is removed instead):
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
thisdict.popitem()
print(thisdict)
```

    {'brand': 'Ford', 'year': 1964, 'model': 'Mustang'}
    {'year': 1964, 'model': 'Mustang'}
    


```python
# The del keyword removes the item with the specified key name:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
del thisdict["model"]
print(thisdict)
```

    {'brand': 'Ford', 'year': 1964, 'model': 'Mustang'}
    {'brand': 'Ford', 'year': 1964}
    


```python
# The del keyword can delete the dictionary completely:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict
try:
    print(thisdict) #this will cause an error because "thisdict" no longer exists.
except:
    print("Dictionary doest not exist")
```

    Dictionary doest not exist
    


```python
# The clear() method empties the dictionary:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
thisdict.clear()
print(thisdict)
```

    {'brand': 'Ford', 'year': 1964, 'model': 'Mustang'}
    {}
    

### Copy a Dictionary

You cannot copy a dictionary simply by typing ```dict2 = dict1```, because: ```dict2``` will only be a reference to ```dict1```, and changes made in ```dict1``` will automatically also be made in ```dict2```.

There are ways to make a copy, one way is to use the built-in Dictionary method ```copy()```.


```python
# Make a copy of a dictionary with the copy() method:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = thisdict.copy()
print(mydict)
```

    {'brand': 'Ford', 'year': 1964, 'model': 'Mustang'}
    


```python
# Another way to make a copy is to use the built-in function dict().
# Make a copy of a dictionary with the dict() function:
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = dict(thisdict)
print(mydict)
```

    {'brand': 'Ford', 'year': 1964, 'model': 'Mustang'}
    

### Nested Dictionaries


```python
# Create a dictionary that contain three dictionaries:
myfamily = {
  "child1" : {
    "name" : "Emil",
    "year" : 2004
  },
  "child2" : {
    "name" : "Tobias",
    "year" : 2007
  },
  "child3" : {
    "name" : "Linus",
    "year" : 2011
  }
}
print(myfamily)
```

    {'child1': {'year': 2004, 'name': 'Emil'}, 'child2': {'year': 2007, 'name': 'Tobias'}, 'child3': {'year': 2011, 'name': 'Linus'}}
    


```python
# Create three dictionaries, then create one dictionary that will contain the other three dictionaries:
child1 = {
  "name" : "Emil",
  "year" : 2004
}
child2 = {
  "name" : "Tobias",
  "year" : 2007
}
child3 = {
  "name" : "Linus",
  "year" : 2011
}

myfamily = {
  "child1" : child1,
  "child2" : child2,
  "child3" : child3
}
print(myfamily)
```

    {'child1': {'year': 2004, 'name': 'Emil'}, 'child2': {'year': 2007, 'name': 'Tobias'}, 'child3': {'year': 2011, 'name': 'Linus'}}
    

### The dict() Constructor


```python
# It is also possible to use the dict() constructor to make a new dictionary:
thisdict = dict(brand="Ford", model="Mustang", year=1964)
# note that keywords are not string literals
# note the use of equals rather than colon for the assignment
print(thisdict)
```

    {'brand': 'Ford', 'year': 1964, 'model': 'Mustang'}
    

### Dictionary Methods

    - clear()       :Removes all the elements from the dictionary
    - copy()        :Returns a copy of the dictionary
    - fromkeys()    :Returns a dictionary with the specified keys and value
    - get()         :Returns the value of the specified key
    - items()       :Returns a list containing a tuple for each key value pair
    - keys()        :Returns a list containing the dictionary's keys
    - pop()         :Removes the element with the specified key
    - popitem()     :Removes the last inserted key-value pair
    - setdefault()  :Returns the value of the specified key. If the key does not exist:  
                     insert the key, with the specified value
    - update()      :Updates the dictionary with the specified key-value pairs
    - values()      :Returns a list of all the values in the dictionary

# If - Else Statement


```python
# If statement:
a = 33
b = 200
if b > a:
  print("b is greater than a")
```

    b is greater than a
    

### Indentation


```python
a = 33
b = 200
try:
    #if b > a:
    #print("b is greater than a") # you will get an error
    pass
except:
    print("Indentation error")
```

### Elif

The ```elif``` keyword is pythons way of saying "if the previous conditions were not true, then try this condition".


```python
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```

    a and b are equal
    

### Else

The ```else``` keyword catches anything which isn't caught by the preceding conditions.


```python
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```

    a is greater than b
    

### Short Hand If


```python
# One line if statement:
if a > b: print("a is greater than b")
```

    a is greater than b
    

### Short Hand If ... Else


```python
# One line if else statement:
a = 2
b = 330
print("A") if a > b else print("B")
```

    B
    


```python
# One line if else statement, with 3 conditions:
a = 330
b = 330
print("A") if a > b else print("=") if a == b else print("B")
```

    =
    

### And

The ```and ```keyword is a logical operator, and is used to combine conditional statements:


```python
# Test if a is greater than b, AND if c is greater than a:
a = 200
b = 33
c = 500
if a > b and c > a:
  print("Both conditions are True")
```

    Both conditions are True
    

### Or


```python
# Test if a is greater than b, OR if a is greater than c:
a = 200
b = 33
c = 500
if a > b or a > c:
  print("At least one of the conditions is True")
```

    At least one of the conditions is True
    

### Nested If


```python
# You can have if statements inside if statements, this is called nested if statements.
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

    Above ten,
    and also above 20!
    

### The pass Statement

```if``` statements cannot be empty, but if you for some reason have an ```if``` statement with no content, 
put in the ```pass``` statement to avoid getting an error.


```python
a = 33
b = 200

if b > a:
  pass
```

# While Loops

With the ```while``` loop we can execute a set of statements as long as a condition is true.


```python
# Print i as long as i is less than 6:
i = 1
while i < 6:
  print(i)
  i += 1
```

    1
    2
    3
    4
    5
    

### Break Statement


```python
# Exit the loop when i is 3:
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```

    1
    2
    3
    

### Continue Statement


```python
# Continue to the next iteration if i is 3:
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```

    1
    2
    4
    5
    6
    

### The else Statement

With the else statement we can run a block of code once when the condition no longer is true:


```python
# Print a message once the condition is false:
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
```

    1
    2
    3
    4
    5
    i is no longer less than 6
    

# For Loops

A ```for``` loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

This is less like the ```for``` keyword in other programming languages, and works more like an iterator method as found in other object-orientated programming languages.

With the ```for``` loop we can execute a set of statements, once for each item in a list, tuple, set etc.


```python
# Print each fruit in a fruit list:
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
```

    apple
    banana
    cherry
    

The ```for``` loop does not require an indexing variable to set beforehand.

### Looping Through a String

Even strings are iterable objects, they contain a sequence of characters:


```python
# Loop through the letters in the word "banana":
for x in "banana":
  print(x)
```

    b
    a
    n
    a
    n
    a
    

### The break Statement

With the ```break``` statement we can stop the loop before it has looped through all the items:


```python
# Exit the loop when x is "banana":
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
  if x == "banana":
    break
```

    apple
    banana
    


```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    break
  print(x)
```

    apple
    

### The continue Statement

With the continue statement we can stop the current iteration of the loop, and continue with the next:


```python
# Do not print banana:
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x)
```

    apple
    cherry
    

### The range() Function

To loop through a set of code a specified number of times, we can use the ```range()``` function,
The ```range()``` function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and ends at a specified number.


```python
# Using the range() function:
for x in range(6):
  print(x)
```

    0
    1
    2
    3
    4
    5
    

The ```range()``` function defaults to 0 as a starting value, however it is possible to specify the starting value by adding a parameter: ```range(2, 6)```, which means values from 2 to 6 (but not including 6):


```python
# Using the start parameter:
for x in range(2, 6):
  print(x)
```

    2
    3
    4
    5
    

The ```range()``` function defaults to increment the sequence by 1, however it is possible to specify the increment value by adding a third parameter: ```range(2, 30, 3)```:


```python
# Increment the sequence with 3 (default is 1):
for x in range(2, 30, 3):
  print(x)
```

    2
    5
    8
    11
    14
    17
    20
    23
    26
    29
    

### Else in For Loop

The ```else``` keyword in a ```for``` loop specifies a block of code to be executed when the loop is finished:


```python
# Print all numbers from 0 to 5, and print a message when the loop has ended:
for x in range(6):
  print(x)
else:
  print("Finally finished!")
```

    0
    1
    2
    3
    4
    5
    Finally finished!
    

### Nested Loops

A nested loop is a loop inside a loop.

The "inner loop" will be executed one time for each iteration of the "outer loop":


```python
# Print each adjective for every fruit:
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)
```

    red apple
    red banana
    red cherry
    big apple
    big banana
    big cherry
    tasty apple
    tasty banana
    tasty cherry
    

### The pass Statement

```for``` loops cannot be empty, but if you for some reason have a ```for``` loop with no content, put in the ```pass``` statement to avoid getting an error.


```python
for x in [0, 1, 2]:
  pass
```

# Functions

A function is a block of code which only runs when it is called.
You can pass data, known as parameters, into a function.
A function can return data as a result.

### Creating a Function


```python
# In Python a function is defined using the def keyword:
def my_function():
  print("Hello from a function")
```

### Calling a Function


```python
# To call a function, use the function name followed by parenthesis:
def my_function():
  print("Hello from a function")

my_function()
```

    Hello from a function
    

### Arguments

Information can be passed into functions as arguments.

Arguments are specified after the function name, inside the parentheses. You can add as many arguments as you want, just separate them with a comma.

The following example has a function with one argument (fname). When the function is called, we pass along a first name, which is used inside the function to print the full name:


```python
def my_function(fname):
  print(fname + " Refsnes")

my_function("Emil")
my_function("Tobias")
my_function("Linus")
```

    Emil Refsnes
    Tobias Refsnes
    Linus Refsnes
    

### Parameters or Arguments?

From a function's perspective:

A parameter is the variable listed inside the parentheses in the function definition.

An argument is the value that is sent to the function when it is called.

### Number of Arguments

By default, a function must be called with the correct number of arguments. Meaning that if your function expects 2 arguments, you have to call the function with 2 arguments, not more, and not less.


```python
def my_function(fname, lname):
  print(fname + " " + lname)

my_function("Emil", "Refsnes")
```

    Emil Refsnes
    

### Arbitrary Arguments, *args

If you do not know how many arguments that will be passed into your function, add a ```*``` before the parameter name in the function definition.

This way the function will receive a tuple of arguments, and can access the items accordingly:


```python
# If the number of arguments is unknown, add a * before the parameter name:
def my_function(*kids):
  print("The youngest child is " + kids[2])

my_function("Emil", "Tobias", "Linus")
```

    The youngest child is Linus
    

### Keyword Arguments

You can also send arguments with the key = value syntax.

This way the order of the arguments does not matter.


```python
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")
```

    The youngest child is Linus
    

### Arbitrary Keyword Arguments, **kwargs

If you do not know how many keyword arguments that will be passed into your function, add two asterisk: ```**``` before the parameter name in the function definition.

This way the function will receive a dictionary of arguments, and can access the items accordingly:


```python
# If the number of keyword arguments is unknown, add a double ** before the parameter name:
def my_function(**kid):
  print("His last name is " + kid["lname"])

my_function(fname = "Tobias", lname = "Refsnes")
```

    His last name is Refsnes
    

### Default Parameter Value

The following example shows how to use a default parameter value.

If we call the function without argument, it uses the default value:


```python
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("Sweden")
my_function("India")
my_function()
my_function("Brazil")
```

    I am from Sweden
    I am from India
    I am from Norway
    I am from Brazil
    

### Passing a List as an Argument

You can send any data types of argument to a function (string, number, list, dictionary etc.), and it will be treated as the same data type inside the function.

E.g. if you send a List as an argument, it will still be a List when it reaches the function:


```python
def my_function(food):
  for x in food:
    print(x)

fruits = ["apple", "banana", "cherry"]

my_function(fruits)
```

    apple
    banana
    cherry
    

### Return Values

To let a function return a value, use the ```return``` statement:


```python
def my_function(x):
  return 5 * x

print(my_function(3))
print(my_function(5))
print(my_function(9))
```

    15
    25
    45
    

### The pass Statement

```function``` definitions cannot be empty, but if you for some reason have a ```function``` definition with no content, put in the ```pass``` statement to avoid getting an error.


```python
def myfunction():
  pass
```

### Recursion


```python
# Recursion Example
def tri_recursion(k):
  if(k > 0):
    result = k + tri_recursion(k - 1)
    print(result)
  else:
    result = 0
  return result

print("\n\nRecursion Example Results")
tri_recursion(6)
```

    
    
    Recursion Example Results
    1
    3
    6
    10
    15
    21
    




    21



# Lambda Function

A lambda function is a small anonymous function.

A lambda function can take any number of arguments, but can only have one expression.

### Syntax

```lambda arguments : expression```


```python
# A lambda function that adds 10 to the number passed in as an argument, and print the result:
x = lambda a : a + 10
print(x(5))
```

    15
    

Lambda functions can take any number of arguments:


```python
# A lambda function that multiplies argument a with argument b and print the result:
x = lambda a, b : a * b
print(x(5, 6))
```

    30
    


```python
# A lambda function that sums argument a, b, and c and print the result:
x = lambda a, b, c : a + b + c
print(x(5, 6, 2))
```

    13
    

### Why Use Lambda Functions?

The power of lambda is better shown when you use them as an anonymous function inside another function.

Say you have a function definition that takes one argument, and that argument will be multiplied with an unknown number:


```python
# Use that function definition to make a function that always doubles the number you send in:
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)

print(mydoubler(11))
```

    22
    


```python
# Or, use the same function definition to make a function that always triples the number you send in:
def myfunc(n):
  return lambda a : a * n

mytripler = myfunc(3)

print(mytripler(11))
```

    33
    


```python
# Or, use the same function definition to make both functions, in the same program:
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)
mytripler = myfunc(3)

print(mydoubler(11))
print(mytripler(11))
```

    22
    33
    

Use lambda functions when an anonymous function is required for a short period of time.

# Arrays

Python does not have built-in support for Arrays, but Python Lists can be used instead

Arrays are used to store multiple values in one single variable:


```python
# Create an array containing car names:
cars = ["Ford", "Volvo", "BMW"]
```

### Access the Elements of an Array


```python
# Get the value of the first array item:
cars = ["Ford", "Volvo", "BMW"]
x = cars[0]
print(x)
```

    Ford
    


```python
# Modify the value of the first array item:
cars = ["Ford", "Volvo", "BMW"]
x = cars[0]
print(x)
cars[0] = "Toyota"
x = cars[0]
print(x)
```

    Ford
    Toyota
    

### The Length of an Array

Use the ```len()``` method to return the length of an array (the number of elements in an array).


```python
# Return the number of elements in the cars array:
cars = ["Ford", "Volvo", "BMW"]
x = len(cars)
print(x)
```

    3
    

### Looping Array Elements

You can use the for in loop to loop through all the elements of an array.


```python
# Print each item in the cars array:
cars = ["Ford", "Volvo", "BMW"]
for x in cars:
  print(x)
```

    Ford
    Volvo
    BMW
    

### Adding Array Elements


```python
# Add one more element to the cars array:
cars = ["Ford", "Volvo", "BMW"]
for x in cars:
  print(x)
print()
cars.append("Honda")
for x in cars:
  print(x)
```

    Ford
    Volvo
    BMW
    
    Ford
    Volvo
    BMW
    Honda
    

### Removing Array Elements


```python
# Delete the second element of the cars array:
cars = ["Ford", "Volvo", "BMW"]
for x in cars:
  print(x)
print()
cars.pop(1)
for x in cars:
  print(x)
```

    Ford
    Volvo
    BMW
    
    Ford
    BMW
    


```python
# Delete the element that has the value "Volvo":
cars = ["Ford", "Volvo", "BMW"]
for x in cars:
  print(x)
print()
cars.remove("Volvo")
for x in cars:
  print(x)
```

    Ford
    Volvo
    BMW
    
    Ford
    BMW
    

# Classes and Objects

Python is an object oriented programming language.  
Almost everything in Python is an object, with its properties and methods.  
A Class is like an object constructor, or a "blueprint" for creating objects.

### Create a Class

To create a class, use the keyword ```class:```


```python
# Create a class named MyClass, with a property named x:
class MyClass:
  x = 5
```

### Create Object


```python
# Create an object named p1, and print the value of x:
class MyClass:
  x = 5
p1 = MyClass()
print(p1.x)
```

    5
    

### The __init__() Function

All classes have a function called ```__init__()```, which is always executed when the class is being initiated.  
Use the ```__init__()``` function to assign values to object properties, or other operations that are necessary to do when the object is being created:


```python
# Create a class named Person, use the __init__() function to assign values for name and age:
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)
```

    John
    36
    

The ```__init__()``` function is called automatically every time the class is being used to create a new object.

### Object Methods

Objects can also contain methods. Methods in objects are functions that belong to the object.



```python
# Let us create a method in the Person class:
# Insert a function that prints a greeting, and execute it on the p1 object:

class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()
```

    Hello my name is John
    

The ```self``` parameter is a reference to the current instance of the class, and is used to access variables that belong to the class.  
It does not have to be named ```self``` , you can call it whatever you like, but it has to be the first parameter of any function in the class:


```python
# Use the words mysillyobject and abc instead of self:
class Person:
  def __init__(mysillyobject, name, age):
    mysillyobject.name = name
    mysillyobject.age = age

  def myfunc(abc):
    print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()
```

    Hello my name is John
    

### Modify Object Properties


```python
# Set the age of p1 to 40:
p1.age = 40
```

### Delete Object Properties


```python
# Delete the age property from the p1 object:
del p1.age
```

### Delete Objects


```python
# Delete the p1 object:
del p1
```

### The pass Statement

```class``` definitions cannot be empty, but if you for some reason have a ```class``` definition with no content, put in the ```pass``` statement to avoid getting an error.


```python
class Person:
  pass
```

# Inheritance

Inheritance allows us to define a class that inherits all the methods and properties from another class.  
Parent class is the class being inherited from, also called base class.  
Child class is the class that inherits from another class, also called derived class.  

### Create a Parent Class


```python
# Create a class named Person, with firstname and lastname properties, and a printname method:
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:

x = Person("John", "Doe")
x.printname()
```

    John Doe
    

### Create a Child Class

To create a class that inherits the functionality from another class, send the parent class as a parameter when creating the child class:


```python
# Create a class named Student, which will inherit the properties and methods from the Person class:
class Student(Person):
  pass
```

Now the Student class has the same properties and methods as the Person class.


```python
# Use the Student class to create an object, and then execute the printname method:
x = Student("Mike", "Olsen")
x.printname()
```

    Mike Olsen
    

### Add the __init__() Function

So far we have created a child class that inherits the properties and methods from its parent.
We want to add the ```__init__()``` function to the child class (instead of the ```pass``` keyword).


```python
# Add the __init__() function to the Student class:
class Student(Person):
  def __init__(self, fname, lname):
    #add properties etc.
    pass
```

When you add the ```__init__()``` function, the child class will no longer inherit the parent's ```__init__()``` function.

To keep the inheritance of the parent's ```__init__()``` function, add a call to the parent's ```__init__()``` function:


```python
class Student(Person):
  def __init__(self, fname, lname):
    Person.__init__(self, fname, lname)
```

Now we have successfully added the ```__init__()``` function, and kept the inheritance of the parent class, and we are ready to add functionality in the ```__init__()``` function.

### Use the super() Function

Python also has a ```super()``` function that will make the child class inherit all the methods and properties from its parent:


```python
class Student(Person):
  def __init__(self, fname, lname):
    super().__init__(fname, lname)
```

By using the ```super()``` function, you do not have to use the name of the parent element, it will automatically inherit the methods and properties from its parent.

### Add Properties


```python
# Add a property called graduationyear to the Student class:
class Student(Person):
  def __init__(self, fname, lname):
    super().__init__(fname, lname)
    self.graduationyear = 2019
```


```python
# Add a year parameter, and pass the correct year when creating objects:
class Student(Person):
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year

x = Student("Mike", "Olsen", 2019)
```

### Add Methods


```python
# Add a method called welcome to the Student class:
class Student(Person):
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year

  def welcome(self):
    print("Welcome", self.firstname, self.lastname, "to the class of", self.graduationyear)
```

# Iterator

An iterator is an object that contains a countable number of values.

An iterator is an object that can be iterated upon, meaning that you can traverse through all the values.

Technically, in Python, an iterator is an object which implements the iterator protocol, which consist of the methods ```__iter__()``` and ```__next__()```.

### Iterator vs Iterable

Lists, tuples, dictionaries, and sets are all iterable objects. They are iterable containers which you can get an iterator from.  
All these objects have a ```iter()``` method which is used to get an iterator:


```python
# Return an iterator from a tuple, and print each value:
mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)

print(next(myit))
print(next(myit))
print(next(myit))
```

    apple
    banana
    cherry
    


```python
# Strings are also iterable objects, containing a sequence of characters:
mystr = "banana"
myit = iter(mystr)

print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
```

    b
    a
    n
    a
    n
    a
    

### Looping Through an Iterator

We can also use a ```for``` loop to iterate through an iterable object:


```python
# Iterate the values of a tuple:
mytuple = ("apple", "banana", "cherry")

for x in mytuple:
  print(x)
```

    apple
    banana
    cherry
    


```python
# Iterate the characters of a string:
mystr = "banana"

for x in mystr:
  print(x)
```

    b
    a
    n
    a
    n
    a
    

The ```for``` loop actually creates an iterator object and executes the ```next()``` method for each loop.

### Create an Iterator

To create an object/class as an iterator you have to implement the methods ```__iter__()``` and ```__next__()``` to your object.  
The ```__iter__()``` method acts similar, you can do operations (initializing etc.), but must always return the iterator object itself.  
The ```__next__()``` method also allows you to do operations, and must return the next item in the sequence.  


```python
# Create an iterator that returns numbers, starting with 1, and each sequence will increase by one (returning 1,2,3,4,5 etc.):
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    x = self.a
    self.a += 1
    return x

myclass = MyNumbers()
myiter = iter(myclass)

print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
```

    1
    2
    3
    4
    5
    

### StopIteration

The example above would continue forever if you had enough next() statements, or if it was used in a ```for``` loop.

To prevent the iteration to go on forever, we can use the ```StopIteration``` statement.

In the ```__next__()``` method, we can add a terminating condition to raise an error if the iteration is done a specified number of times:


```python
# Stop after 20 iterations:
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    if self.a <= 20:
      x = self.a
      self.a += 1
      return x
    else:
      raise StopIteration

myclass = MyNumbers()
myiter = iter(myclass)

for x in myiter:
  print(x)
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12
    13
    14
    15
    16
    17
    18
    19
    20
    

# Scope

A variable is only available from inside the region it is created. This is called scope.

### Local Scope

A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.


```python
# A variable created inside a function is available inside that function:
def myfunc():
  x = 300
  print(x)

myfunc()
```

    300
    

#### Function Inside Function

As explained in the example above, the variable ```x``` is not available outside the function, but it is available for any function inside the function:


```python
# The local variable can be accessed from a function within the function:
def myfunc():
  x = 300
  def myinnerfunc():
    print(x)
  myinnerfunc()

myfunc()
```

    300
    

### Global Scope

A variable created in the main body of the Python code is a global variable and belongs to the global scope.  
Global variables are available from within any scope, global and local.  


```python
# A variable created outside of a function is global and can be used by anyone:
x = 300
def myfunc():
  print(x)
myfunc()
print(x)
```

    300
    300
    

#### Naming Variables

If you operate with the same variable name inside and outside of a function, Python will treat them as two separate variables, one available in the global scope (outside the function) and one available in the local scope (inside the function):


```python
# The function will print the local x, and then the code will print the global x:
x = 300
def myfunc():
  x = 200
  print(x)
myfunc()
print(x)
```

    200
    300
    

### Global Keyword

If you need to create a global variable, but are stuck in the local scope, you can use the ```global``` keyword.
The ```global``` keyword makes the variable global.


```python
# If you use the global keyword, the variable belongs to the global scope:
def myfunc():
  global x
  x = 300
myfunc()
print(x)
```

    300
    

Also, use the ```global``` keyword if you want to make a change to a ```global``` variable inside a function.


```python
# To change the value of a global variable inside a function, refer to the variable by using the global keyword:
x = 300
def myfunc():
  global x
  x = 200
myfunc()
print(x)
```

    200
    

# Python Modules

Consider a module to be the same as a code library.  
A file containing a set of functions you want to include in your application.  

### Create a Module

To create a module just save the code you want in a file with the file extension ```.py```.


```python
# Save this code in a file named mymodule.py
def greeting(name):
  print("Hello, " + name)
```

### Use a Module

Now we can use the module we just created, by using the ```import``` statement:


```python
# Import the module named mymodule, and call the greeting function:
# import mymodule
mymodule.greeting("Jonathan")
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-94-4a65e1642eb6> in <module>
          1 # Import the module named mymodule, and call the greeting function:
          2 # import mymodule
    ----> 3 mymodule.greeting("Jonathan")
    

    NameError: name 'mymodule' is not defined


When using a function from a module, use the syntax: module_name.function_name.

### Variables in Module

The module can contain functions, as already described, but also variables of all types (arrays, dictionaries, objects etc):


```python
# Save this code in the file mymodule.py
person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```


```python
# Import the module named mymodule, and access the person1 dictionary:
#import mymodule
#a = mymodule.person1["age"]
#print(a)
```

### Naming a Module

You can name the module file whatever you like, but it must have the file extension ```.py```

### Re-naming a Module

You can create an alias when you import a module, by using the ```as``` keyword:


```python
# Create an alias for mymodule called mx:
#import mymodule as mx
#a = mx.person1["age"]
#print(a)
```

### Built-in Modules

There are several built-in modules in Python, which you can import whenever you like.


```python
# Import and use the platform module:
import platform
x = platform.system()
print(x)
```

    Windows
    

### Using the dir() Function

There is a built-in function to list all the function names (or variable names) in a module. The ```dir()``` function


```python
# List all the defined names belonging to the platform module:
import platform
x = dir(platform)
print(x)
```

    ['DEV_NULL', '_UNIXCONFDIR', '_WIN32_CLIENT_RELEASES', '_WIN32_SERVER_RELEASES', '__builtins__', '__cached__', '__copyright__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '__version__', '_default_architecture', '_dist_try_harder', '_follow_symlinks', '_ironpython26_sys_version_parser', '_ironpython_sys_version_parser', '_java_getprop', '_libc_search', '_linux_distribution', '_lsb_release_version', '_mac_ver_xml', '_node', '_norm_version', '_parse_release_file', '_platform', '_platform_cache', '_pypy_sys_version_parser', '_release_filename', '_release_version', '_supported_dists', '_sys_version', '_sys_version_cache', '_sys_version_parser', '_syscmd_file', '_syscmd_uname', '_syscmd_ver', '_uname_cache', '_ver_output', 'architecture', 'collections', 'dist', 'java_ver', 'libc_ver', 'linux_distribution', 'mac_ver', 'machine', 'node', 'os', 'platform', 'popen', 'processor', 'python_branch', 'python_build', 'python_compiler', 'python_implementation', 'python_revision', 'python_version', 'python_version_tuple', 're', 'release', 'subprocess', 'sys', 'system', 'system_alias', 'uname', 'uname_result', 'version', 'warnings', 'win32_ver']
    

### Import From Module

You can choose to import only parts from a module, by using the ```from``` keyword.


```python
# The module named mymodule has one function and one dictionary:
def greeting(name):
  print("Hello, " + name)

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```


```python
# Import only the person1 dictionary from the module:
#from mymodule import person1

print (person1["age"])
```

    36
    

When importing using the ```from``` keyword, do not use the module name when referring to elements in the module. Example: ```person1["age"]```, not ```mymodule.person1["age"]```

# Try Except

The ```try``` block lets you test a block of code for errors.

The ```except``` block lets you handle the error.

The ```finally``` block lets you execute code, regardless of the result of the try- and except blocks.

### Exception Handling

When an error occurs, or exception as we call it, Python will normally stop and generate an error message.

These exceptions can be handled using the ```try``` statement:


```python
# The try block will generate an exception, because x is not defined:
x=1
try:
  print(x)
except:
  print("An exception occurred")
```

    1
    

### Many Exceptions

You can define as many exception blocks as you want, e.g. if you want to execute a special block of code for a special kind of error:


```python
# Print one message if the try block raises a NameError and another for other errors:
try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")
```

    1
    

### Else

You can use the ```else``` keyword to define a block of code to be executed if no errors were raised:


```python
# In this example, the try block does not generate any error:
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")
```

    Hello
    Nothing went wrong
    

### Finally

The ```finally``` block, if specified, will be executed regardless if the try block raises an error or not.


```python
try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")
```

    1
    The 'try except' is finished
    

This can be useful to close objects and clean up resources:


```python
# Try to open and write to a file that is not writable:
"""
try:
  f = open("demofile.txt")
  f.write("Lorum Ipsum")
except:
  print("Something went wrong when writing to the file")
finally:
  f.close()
"""
```




    '\ntry:\n  f = open("demofile.txt")\n  f.write("Lorum Ipsum")\nexcept:\n  print("Something went wrong when writing to the file")\nfinally:\n  f.close()\n'



### Raise an exception

As a Python developer you can choose to throw an exception if a condition occurs.

To throw (or raise) an exception, use the ```raise``` keyword.


```python
# Raise an error and stop the program if x is lower than 0:
x = -1
if x < 0:
  raise Exception("Sorry, no numbers below zero")
```


    ---------------------------------------------------------------------------

    Exception                                 Traceback (most recent call last)

    <ipython-input-116-a18a187e9d99> in <module>
          2 x = -1
          3 if x < 0:
    ----> 4   raise Exception("Sorry, no numbers below zero")
    

    Exception: Sorry, no numbers below zero


The ```raise``` keyword is used to raise an exception.
You can define what kind of error to raise, and the text to print to the user.


```python
# Raise a TypeError if x is not an integer:
x = "hello"
if not type(x) is int:
  raise TypeError("Only integers are allowed")
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-117-1d74fa053013> in <module>
          2 x = "hello"
          3 if not type(x) is int:
    ----> 4   raise TypeError("Only integers are allowed")
    

    TypeError: Only integers are allowed


# User Input

Python 3.6 uses the ```input()``` method.

Python 2.7 uses the ```raw_input()``` method.


```python
username = input("Enter username:")
print("Username is: " + username)
```

    Enter username:abc
    Username is: abc
    

Python stops executing when it comes to the input() function, and continues when the user has given some input.

# String Formatting

To make sure a string will display as expected, we can format the result with the ```format()``` method.

### String format()

The ```format()``` method allows you to format selected parts of a string.

Sometimes there are parts of a text that you do not control, maybe they come from a database, or user input?

To control such values, add placeholders (curly brackets ```{}```) in the text, and run the values through the ```format()``` method:


```python
# Add a placeholder where you want to display the price:
price = 49
txt = "The price is {} dollars"
print(txt.format(price))
```

    The price is 49 dollars
    

You can add parameters inside the curly brackets to specify how to convert the value:


```python
# Format the price to be displayed as a number with two decimals:
txt = "The price is {:.2f} dollars"
```

### Multiple Values


```python
# If you want to use more values, just add more values to the format() method:
quantity = 3
itemno = 567
price = 49
myorder = "I want {} pieces of item number {} for {:.2f} dollars."
print(myorder.format(quantity, itemno, price))
```

    I want 3 pieces of item number 567 for 49.00 dollars.
    

### Index Numbers

You can use index numbers (a number inside the curly brackets ```{0}```) to be sure the values are placed in the correct placeholders:


```python
quantity = 3
itemno = 567
price = 49
myorder = "I want {0} pieces of item number {1} for {2:.2f} dollars."
print(myorder.format(quantity, itemno, price))
```

    I want 3 pieces of item number 567 for 49.00 dollars.
    

Also, if you want to refer to the same value more than once, use the index number:


```python
age = 36
name = "John"
txt = "His name is {1}. {1} is {0} years old."
print(txt.format(age, name))
```

    His name is John. John is 36 years old.
    

### Named Indexes

You can also use named indexes by entering a name inside the curly brackets ```{carname}```, but then you must use names when you pass the parameter values ```txt.format(carname = "Ford")```:


```python
myorder = "I have a {carname}, it is a {model}."
print(myorder.format(carname = "Ford", model = "Mustang"))
```

    I have a Ford, it is a Mustang.
    
