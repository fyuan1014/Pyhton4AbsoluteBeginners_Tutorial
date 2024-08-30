# Pyhton4AbsoluteBeginners_Tutorial
This is a tutorial for absolute beginners to learn Python. Nowadays, Python is not only the tool used by current data scientists/engineers, and machine learning/AI/software engineers, but also widely and popularly used across various industries and research fields. For instance, social scientists, urban analyst, and mechanical, civil, and environmental engineers can use Python for their daily work log data analysis, and graduate research assistants/postdoc researchers can use Python for the data analytics part of their research projects. Utilizing Python can significantly reduce manual efforts for your daily work and research as long as you are dealing with data, particularly big data. Given the increasing popularity of Python, this tutorial is now introduced to absolute Python beginners!

Before starting using common Python libraries such as pandas, numpy, matplotlib, etc., there are six main concepts in Python that beginners may start with, including data types, variables, conditional logic, loops, functions, and comprehensions. With a good understanding of them, you will get a solid foundation in Python and can step further in using popular and fancy Python libraries and developing your own functions, modules, and library. Now, let's get started with this tutorial!

This tutorial is particularly useful for users planning to step into Python world but without prior coding experiences, such as new graduate students (not from CS/CE/DS/EE/ECE/MATH etc.) who just started their PhD programs and will conduct research involved with big data, and those working in traditional industry (e.g., non-tech industry) who are considering either daily work method transition from traditional analysis tool such as Excel to an open-source tool like Python or even a career transition into a data-/tech-related industry.

## Chapter 0. Python Installation
Let’s start with Python installation. Here is a brief guideline to install Python in your computer. <br>
1) From this website (https://www.python.org/downloads/), you can download the latest Python version according to your system such as Windows, Linux/UNIX, macOS, and Other.
2) You can install Python after the download and follow the default settings/instructions to install Python into your computer.
3) After the installation, the IDLE shell should be ready in your system as well. You may try searching IDLE in your computer program for verifying the installation. Figure 1 shows a screenshot of how the user interface of IDLE looks like. With IDLE, you can start coding with Python!<br>
 <br> <img width="355" alt="Figure 1  Screenshot of IDLE interface" src="https://github.com/user-attachments/assets/92fba48f-7d18-4bc1-8f85-f2ae62de427d">
<br>Figure 1. Screenshot of IDLE interface.png

## Chapter 1. Data Types
### 1.1 Numeric
Python supports two main numeric data types including integer ('int') and float ('float'), where 'int' represents whole numbers without a fractional component and 'float' denotes numbers with a fractional component. <br> 
<br>Here is an example code for these data types:
```python
#1 Integer example
a = 3
print("Integer:", a)
print("Type of a:", type(a))
```
```python 
#Expected output of integer example:
Integer: 3
Type of a: <class 'int'>
```
```python 
#2 Float example
b = 3.14
print("Float:", b)
print("Type of b:", type(b))
```
```python 
#Expected output of float example:
Float: 3.14
Type of b: <class 'float'>
```
### 1.2 String
A string is a sequence of characters enclosed in quotes (single or double), and you can access a particular character by their index within a string. <br>
<br>Here is a sample code for the string type:
```python
#1 String example
s_single = 'Hello, World!'
s_double = "Hello, World!"
print("String:", s_single)
print("Type of s_single:", type(s_single))
print("String:", s_double)
print("Type of s_double:", type(s_double))
```
```python
#Expected output from string examples
String: Hello, Python!
Type of s_single: <class 'str'>
String: Hello, Python!
Type of s_double: <class 'str'>
```
```python 
#2 Accessing elements in a string by index
first_char = s_single[0] # Python index starts with 0
end_char = s_single[-1]
first_five_chars = s_single[0:5] # Here you can use ':' to denote the range of index where you want to get the characters
print("First character:", first_char)
print("End character:", end_char)
print("First five characters:", first_five_chars)
```
```python 
#Expected output from accessing elements by index
First character: H
End character: !
First five characters: Hello
```
### 1.3 Boolean
Python Boolean type is one of the built-in data types provided by Python, which represents one of the two values i.e. 'True' or 'False'. Generally, it is used to represent the truth values of the expressions. <br>
<br>Here is a sample code for the Boolean type:
```python
#1 Boolean example
x = True
y = False
print("Boolean x:", x)
print("Boolean y:", y)
print("Type of x:", type(x))
print("Type of y:", type(y))
```
```python
#Expected output from Boolean example
Boolean x: True
Boolean y: False
Type of x: <class 'bool'>
Type of y: <class 'bool'>
```
There are several ways to convert a value to a Boolean value i.e., True or False, including using Python bool() function, from the expression, and integers and floats as Booleans. <br>
<br> Here are the sample codes by using these methods to generate Boolean values.
```python
#2 built-in method bool()
##2.1 Returns False as a is not equal to b
a = 1
b = 10
print(bool(a==b))
##2.2 Returns False as a is None
a = None
print(bool(a))
##2.3 Returns False as a is an empty sequence
a = ()
print(bool(a))
##2.4 Returns False as a is an empty mapping
a = {}
print(bool(a))
##2.5 Returns False as a is 0
a = 0
print(bool(a))
#2.6 Returns True as a is a non-empty string
a = 'LovePython!'
print(bool(a))
```
```python 
#Expected output from bool() function
False #a does not equal to b
False #a is None
False #a is an empty sequence
False #a is an empty mapping
False #a is 0
True #a ('LovePython!') is not an empty sequence
```
```python
#3 from the expression
a = 1
b = 10
print(a==b)
c = 1
print(a==c)
```
```python 
#Expected output from the expression
False #a does not equal to b
True #a equals to c
```
```python
#4 Integers and floats as Booleans
## Integers, floating-point number, or complex number having zero as a value is considered as False,
## while if they are having none-zero value as any positive or negative number then it is considered as True
a = 0
print(bool(a))
b = 10
print(bool(b))
c = -12.3
print(bool(c))
```
```python 
#Expected output from the expression
False
True
True
```
### 1.4 Sequence data type
This section introduces the sequence data types including list, tuple, and range. A Python list is an ordered collection of items that can be of different types. Lists are mutable, meaning their content can be changed. A tuple is like a list, but it's immutable, meaning its content cannot be changed once assigned, which is the main difference between a list and a tuple in Python. A range is a sequence of numbers, and is commonly used for looping a specific number of times such as in a for loop. <br>
<br>Here are sample codes for these sequence types.
```python
#1 List example
list_example = [1, 2, 3, "Python", 4.5]
print("List:", list_example)
print("Type of list_example:", type(list_example))
```
```python 
#Expected output from list example
List: [1, 2, 3, 'Python', 4.5]
Type of list_example: <class 'list'>
```
```python 
#2 Accessing and modifying elements by index in a list
print("First element:", list_example[0])
list_example[1] = "changeAsExample"
print("Modified list:", list_example)
```
```python 
#Expected output from accessing and modifying elements by index
First element: 1
Modified list: [1, 'changeAsExample', 3, 'Python', 4.5]
```
```python
#1 Tuple example
tuple_example = (1, 2, 3, "Python", 4.5)
print("Tuple:", tuple_example)
print("Type of tuple_example:", type(tuple_example))
```
```python 
#Expected output from tuple example
Tuple: (1, 2, 3, 'Python', 4.5)
Type of tuple_example: <class 'tuple'>
```
```python 
#2 Accessing elements by index 
print("First element:", tuple_example[0])
```
```python 
#Expected output from Accessing elements by index
First element: 1
```
```python 
#3 Trying to modify elements by index in a tuple
tuple_example[1] = "changeAsExample"
```
```python
#Expected output from trying to modify elements: TypeError: 'tuple' object does not support item assignment
#This reflects the immutable characteristic of tuple: content cannot be changed once assigned
```
```python
#4 Range example
range_example = range(3)
print("Range:", range_example) 
print("Range elements by list:", list(range_example))  # Convert to list to see the elements
print("Type of range_example:", type(range_example))
```
```python
#Expected output from range example
Range: range(0, 3)
Range elements by list: [0, 1, 2]
Type of range_example: <class 'range'>
```
```python 
#5 Using range in a loop, which be further introduced in Chapter 4
for i in range_example:
    print("Iteration:", i)
```
```python 
# Expected output from range in a loop
Iteration: 0
Iteration: 1
Iteration: 2
```
### 1.5 Dictionary

Dictionary is used to store data values in key:value pairs. A dictionary is a collection which is ordered (As of Python version 3.7, dictionaries are ordered. In Python 3.6 and earlier, dictionaries are unordered.), changeable and do not allow duplicates. Keys must be unique and immutable, while values can be of any type. <br>
<br>Here is a sample codes for the dictionary type
```python
#1 Dictionary example
dict_example = {"name": "Alice", "age": 25, "city": "Boston"}
print("Dictionary:", dict_example)
print("Type of dict_example:", type(dict_example))
```
```python
#Expected output from dictionary example
Dictionary: {'name': 'Alice', 'age': 25, 'city': 'Boston'}
Type of dict_example: <class 'dict'>
```
```python
#2 Get a list of keys
key_list = dict_example.keys()
print("All keys in dict_example:", key_list)
```
```python
#Expected output from getting list of keys in a dictionary
All keys in dict_example: dict_keys(['name', 'age', 'city'])
```
```python
#3 Accessing values by keys by two methods
print("Name:", dict_example["name"])
print("Name:", dict_example.get("name"))
```
```python
#Expected output from accessing values by keys
Name: Alice
Name: Alice
```
```python
#4 Adding and modifying elements
dict_example["age"] = 26
dict_example["country"] = "USA"
print("Modified dictionary:", dict_example)
```
```python
#Expected output from adding and modifying elements
Modified dictionary: {'name': 'Alice', 'age': 26, 'city': 'Boston', 'country': 'USA'}
```
```python
#5 Measure the number of elements (key:value paris)
print(len(dict_example)) # after dict_example was modified, where 'country' key and its corresponding value was added.
```
```python
#Expected output from length measurement
4
```
```python
#6 Values in dictionary items can be of any data type (e.g., list, boolean, etc.)
dict_example['list_example'] = ['red','green','blue']
dict_example['boolean_example'] = True
print(dict_example)
```
```python
#Expected output from various data types for dictionary values
{'name': 'Alice', 'age': 26, 'city': 'Boston', 'country': 'USA', 'list_example': ['red', 'green', 'blue'], 'boolean_example': True}
```
```python
#7 Create dictionary with dict() function
create_dict_example = dict(name="Alice", age=25, city="Boston")
print(create_dict_example)
```
```python
#Expected output from dict() function
{'name': 'Alice', 'age': 25, 'city': 'Boston'}
```
### 1.6 Set
Set is commonly used to store multiple items in a single variable (written with curly brackets) and one of 4 built-in data types in Python used to store collections of data (other three types: List, Tuple, and Dictionary). A set is a collection which is unordered, unchangeable (Set items are unchangeable, but you can remove items and add new items), and unindexed. <br>
<br> Here is a sample code for set
```python
#1 Set examples
set_example_1 = {1, 2, 3, 4, 4, 5}
set_example_2 = {1, 2, 3, 4, 5}
print("Set example 1:", set_example_1)
print("Set example 2:", set_example_2)
print("Type of set_example_1:", type(set_example_1))
print("Type of set_example_2:", type(set_example_2))
```
```python
#Expected output from set examples
Set example 1: {1, 2, 3, 4, 5}
Set example 2: {1, 2, 3, 4, 5} # this print is the same that for set_example_1, as set does not allow duplicates
Type of set_example_1: <class 'set'>
Type of set_example_2: <class 'set'>
```
```python
#2 Adding and removing elements
set_example_1.add(6) # add element 6 into the set_example_1
set_example_1.remove(3) # remove element 3 into the set_example_1
print("Modified set:", set_example_1)
```
```python
#Expected output from adding and removing elements
Modified set: {1, 2, 4, 5, 6}
```
```python
#3 Access elements form a set
# a loop will be needed as there is no index within a set (after addition and removal of elements in set_example_1)
for element in set_example_1:
    print(element)
```
```python
#Expected output from accessing elements in a set
1
2
4
5
6
```
```python
#4 Join sets
set_join_1 = {"a", "b", "c", 1}
set_join_2 = {1, 2, 3, 'b'}
# different joins:
# union() and update() methods joins all items from both sets
# intersection() method keeps ONLY the duplicates from both/all sets
# difference() method keeps the items from the first set that are not in the other set(s) to be joined
# symmetric_difference() method keeps all items EXCEPT the duplicates from all the joined sets

joined_set_1 = set_join_1.union(set_join_2)
joined_set_2 = set_join_1.intersection(set_join_2)
joined_set_3 = set_join_1.difference(set_join_2)
joined_set_4 = set_join_1.symmetric_difference(set_join_2)

print('Joined set by union:', joined_set_1)
print('Joined set by intersection:', joined_set_2)
print('Joined set by difference:', joined_set_3)
print('Joined set by symmetric_difference:', joined_set_4)
```
```python
#Expected output from join sets
Joined set by union: {1, 2, 'c', 3, 'b', 'a'}
Joined set by intersection: {1, 'b'}
Joined set by difference: {'c', 'a'}
Joined set by symmetric_difference: {2, 3, 'c', 'a'}
```

### 1.7 NoneType
The NoneType object, representing the absence of a value, is a special type in Python, i.e., type for the None object in Python. It has the only value as None. <br>
<br>Here is a code sample for None type in Python.
```python
#1 NoneType example
x = None
print("Value of x:", x)
print("Type of x:", type(x))
```
```python
#Expected output from NoneType example
Value of x: None
Type of x: <class 'NoneType'>
```
```python
#2 Checking if a variable is None
if x is None:
    print("x is None")
```
```python
#Expected output from checking if a variable is None
x is None
```
```python
#3 Use of NoneType in if condition (to be further introduced in Chapter 3 Conditional Logic)
if x:
    print(1)
else:
    print(10)
```
```python
#Expected outcome from NoneType in if condition
10
```
## Chapter 2. Variables
### 2.1 Variables assignment & output
A Python variable can be denoted as a container for storing a data value. As there is no command for Python to declare a variable, a variable will be created when you first assign value with it. <br>
<br> Here is a code sample for variable creation, assignment, and output.
```python
#1 Variable creation and assignment examples
x = 5  # Creating and assigning an integer to variable x
y = 3.14  # Creating and assigning a float to variable y
name = "Tony"  # Creating and assigning a string to variable name
is_active = True  # Creating and assigning a Boolean to variable is_active
a, b, c = "red", "green", "blue" # Creating and assigning multiple values to multiple variables a, b, c
d = e = f = "red" # Creating and assigning the same value to multiple variables d, e, f

# Printing variables
print("x =", x)
print("y =", y)
print("name =", name)
print("is_active =", is_active)
print("a, b, c:", a, b, c)
print("d, e, f:", d, e, f)
```
```python
#Expected output from Printing variables
x = 5
y = 3.14
name = Tony
is_active = True
a, b, c: red green blue
d, e, f: red red red
```
```python
#2 Checking types of variables
print("Type of x:", type(x))
print("Type of y:", type(y))
print("Type of name:", type(name))
print("Type of is_active:", type(is_active))
```
```python
#Expected output from checking types of variables
Type of x: <class 'int'>
Type of y: <class 'float'>
Type of name: <class 'str'>
Type of is_active: <class 'bool'>
```
### 2.2 Overwriting variables
In Python, you can overwrite a variable by assigning it with a new value, which can be of the same type or a different type. The previous value is replaced, and the variable now holds the new value. <br>
<br>Here is a sample code for the overwriting variable in Python
```python
#1 Overwriting example & process
## Initial assignment
x = 1
print("Initial value of x:", x)

## Overwriting with a new integer
x = 10
print("After overwriting x with a new integer:", x)

## Overwriting with a different type (float)
x = 10.1
print("After overwriting x with a float:", x)

## Overwriting with a string
x = "Python"
print("After overwriting x with a string:", x)

## Overwriting with a Boolean
x = True
print("After overwriting x with a Boolean:", x)
```
```python
# Expected output from overwriting example & process
Initial value of x: 1
After overwriting x with a new integer: 10
After overwriting x with a float: 10.1
After overwriting x with a string: Python
After overwriting x with a Boolean: True
```
## Chapter 3. Conditional Logic
### 3.1 Boolean expression
Section 1.3 has introduced the Boolean from the expressions. Boolean Expressions: These are expressions that return either True or False based on the evaluation of comparison operators such as <, >, ==, !=, <=, and >=. This section just lists several examples of Boolean values created from the comparison expressions, which can be further used as conditions in the conditional logic.
```python
#1 Boolean expression examples
var_1 = 1
var_2 = 10
## Checking if var_1 is less than var_2
is_less_than = var_1 < var_2
print("Is var_1 less than var_2?", is_less_than)

## Checking if var_1 is equal to var_2
is_equal = var_1 == var_2
print("Is var_1 equal to var_2?", is_equal)

## Checking if var_1 is greater than var_2
is_greater_than = var_1 > var_2
print("Is var_1 greater than var_2?", is_greater_than)
```
```python
#Expected output from Boolean expression examples
Is var_1 less than var_2? True
Is var_1 equal to var_2? False
Is var_1 greater than var_2? False
```
### 3.2 Boolean operations
Boolean operations can be used to combine multiple Boolean expressions in the conditional logic. Python supports the several Boolean operations including 1) and: returns True if both expressions are true; 2) or: returns True if at least one expression is true; and 3) not: returns the opposite of the Boolean value. <br>
<br> Here shows several examples for the mentioned Boolean operations.
```python
# Boolean operation examples
boolean_var_1 = True
boolean_var_2 = False

#1 AND operation
result_and = boolean_var_1 and boolean_var_2
print("Result by boolean_var_1 and boolean_var_2:", result_and)
```
```python
#Expected output from AND operation
Result by boolean_var_1 and boolean_var_2: False
```
```python
#2 OR operation
result_or = boolean_var_1 or boolean_var_2
print("Result by boolean_var_1 or boolean_var_2:", result_or)
```
```python
#Expected output from OR operation
Result by boolean_var_1 or boolean_var_2: True
```
```python
#3 NOT operation
result_not = not boolean_var_1
print("Result by not boolean_var_1:", result_not)
```
```python
#Expected output from NOT operation
Result by not boolean_var_1: False
```
```python
#4 Combining multiple Boolean expressions
boolean_var_3 = 1
boolean_var_4 = 10
combined_result = (boolean_var_3 < boolean_var_4) and (boolean_var_3 > 5)
print("Is boolean_var_3 < boolean_var_4 and boolean_var_3 > 5?", combined_result)
```
```python
#Expected output from combining operation
Is boolean_var_3 < boolean_var_4 and boolean_var_3 > 5? False
```
### 3.3 Conditional statements with Boolean
Conditional statements in Python allow to execute specific blocks of code based on certain conditions. The logic conditions are generally expressed by a single Boolean expression or the operations of multiple Boolean expressions. The most common conditional statements are if, elif, and else. An "if statement" is written by using the 'if' keyword; the 'elif' keyword in Python denoting that "if the previous conditions were not true, then try this condition"; and 'else' refers to anything which isn't caught by the preceding conditions from 'if' and 'elif' statements. <br>
<br> Here are several examples for such conditional statements with Boolean expression (operations).
```python
#1 Boolean operation as condition statement
boolean_var_1 = True
boolean_var_2 = False
if boolean_var_1: # It starts with checking 'if' statement, when 'if' statement is True, it will print boolean_var_1
    print('boolean_var_1:',boolean_var_1)
else: # When 'if' statement is False, it will execute this code to print boolean_var_2
    print('boolean_var_2:',boolean_var_2)
```
```python
#Expected output from a single Boolean expression as condition statement
boolean_var_1: True
```
```python
#2 AND operation as condition statement
result_and = boolean_var_1 and boolean_var_2
if result_and:
    print('boolean_var_1:',boolean_var_1)
else:
    print('boolean_var_2:',boolean_var_2)
```
```python
#Expected output from AND operation as condition statement
boolean_var_2: False
```
```python
#3 OR operation as condition statement
result_or = boolean_var_1 or boolean_var_2
if result_or:
    print('boolean_var_1:',boolean_var_1)
else:
    print('boolean_var_2:',boolean_var_2)
```
```python
#Expected output from OR operation as condition statement
boolean_var_1: True
```
```python
#4 NOT operation as condition statement
result_not = not boolean_var_1
if result_not:
    print('boolean_var_1:',boolean_var_1)
else:
    print('boolean_var_2:',boolean_var_2)
```
```python
#Expected output from NOT operation as condition statement
boolean_var_2: False
```
```python
#5 Combining multiple Boolean expressions as condition statement, and adding elif condition
boolean_var_3 = 1
boolean_var_4 = 10
combined_result = (boolean_var_3 < boolean_var_4) and (boolean_var_3 > 5)

if combined_result: # It starts with checking 'if' statement, when 'if' statement is True, it will print boolean_var_1
    print('boolean_var_1:',boolean_var_1)
elif result_or: # When 'if' statement is False, it goes to check this 'elif' condition, and will print boolean_var_3 when 'elif' statement is True
    print('boolean_var_3:', boolean_var_3)
else: # When both 'if' and 'elif' statements are False, it will execute this code to print boolean_var_2
    print('boolean_var_2:',boolean_var_2)
```
```python
#Expected output from combining operation as condition statement
boolean_var_3: 1
```
## Chapter 4. Loops
### 4.1 for loop
The for loop, as one of the most common control flow structures in Python, is used to iterate over a sequence (such as a list, tuple, string, or range) and execute a block of code for each item in the sequence. <br>
<br> Here are some code examples for the for loop.
```python
#1 For loop to iterate over a list
number_list = [1, 2, 3, 4, 5]
for number in number_list:
    print("Current number:", number)
```
```python
#Expected output from for loop over a list
Current number: 1
Current number: 2
Current number: 3
Current number: 4
Current number: 5
```
```python
#2 For loop to iterate over a string
string_example = "Python"
for char in string_example:
    print("Current character:", char)
```
```python
#Expected output from for loop over a string
Current character: P
Current character: y
Current character: t
Current character: h
Current character: o
Current character: n
```
```python
#3 For loop to iterate over a Dictionary
person_dict = {"name": "Alice", "age": 25, "city": "New York"}
##3.1 For loop to iterate over dictionary keys
for key in person_dict:
    print("Key:", key, "Value:", person_dict[key])
##3.2 Alternatively, we can get both key and value
for key, value in person_dict.items():
    print(f"{key}: {value}")
```
```python
# Expected output from for loop over a Dictionary
## iterate over dictionary keys
Key: name Value: Alice
Key: age Value: 25
Key: city Value: New York
## get both key and value
name: Alice
age: 25
city: New York
```
```python
#4 For loop to iterate over a range (see code sample in section 1.4) and set (see code sample in section 1.6)

#5 The loop control (break, continue and pass) statements in for loop
##5.1 Break statement: to can stop the loop before it has looped through all the items
for i in range(1, 6):
    if i == 3:
        break  # Exit the loop when i is 3
    print("i =", i)
##5.2 Continue statement: to stop the current iteration of the loop, and continue with the next
for i in range(1, 6):
    if i == 3:
        continue  # Skip the iteration when i is 3
    print("i =", i)
##5.3 Pass statement: to do nothing and is often used as a placeholder where code is required syntactically
for i in range(1, 6):
    if i == 3:
        pass  # Placeholder, does nothing
    print("i =", i)
```
```python
#Expected output from for break and continue statements
## break statement
i = 1
i = 2
## continue statement
i = 1
i = 2
i = 4
i = 5
## pass statement
i = 1
i = 2
i = 3
i = 4
i = 5
```
### 4.2 while loop
The while loop in Python repeatedly executes a block of code as long as a given condition is True, which is useful how many times to repeat a block of code is unknow in advance. <br>
<br>Here shows several examples to use while loop.
```python
#1 Basic while loop example
i = 1
## While loop to print numbers from 1 to 5
while i <= 5:
    print("i =", i)
    i += 1  # Increment the counter to avoid an infinite loop
```
```python
#Expected output from basic while loop example
i = 1
i = 2
i = 3
i = 4
i = 5
```
```python
#2  The loop control (break, continue and pass) statements in while loop
## break statement
i = 1
while i < 5:
    print("i =", i)
    if i == 3:
        break  # Exit the loop when i equals 3
    i += 1
## continue statement
i = 0
while i < 5:
    i += 1
    if i == 3:
        continue  # Skip the rest of the code block when i equals 3
    print("i =", i)
```
```python
#Expected output from break and continue statements in while loop
## break statement
i = 1
i = 2
i = 3
## continue statement
i = 1
i = 2
i = 4
i = 5
```
### 4.3 Nested loop
A nested loop is a loop inside a loop, where the "inner loop" will be executed one time for each iteration of the "outer loop". <br>
<br> Here is an example for using nested loop. One thing to note is that nested loop can lead to performance issues and slow down the execution of a program.
```python
# nested loop example
for i in range(1, 3):  # Outer loop
    for j in range(1, 3):  # Inner loop
        print(i,j)
```
```python
#Expected output
1 1
1 2
2 1
2 2
```

### 4.4 Enumerate
Python has built-in function enumerate() allowing to loop over a sequence (like a list, tuple, or string) while also keeping track of the index of each item. This can be particularly useful when both the index and the item itself during each iteration of the loop are needed to be accessible. <br>
<br>Here are some examples for using enumerate()
```python
#1 Using enumerate with a list
fruit_list = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruit_list):
    print(f"Index {index}: {fruit}")
```
```python
#Expected output from enumerate with a list
Index 0: apple
Index 1: banana
Index 2: cherry
```
```python
#2 Using enumerate with a string
string_example = "Python"
for index, char in enumerate(string_example):
    print(f"Character {char} at Index {index}")
```
```python
#Expected output from enumerate with a string
Character P at Index 0
Character y at Index 1
Character t at Index 2
Character h at Index 3
Character o at Index 4
Character n at Index 5
```
## Chapter 5. Function
Python function refers to a reusable block of code that performs a specific task, which helps make code modular, organized, and easier to manage. <br>
### 5.1 Defining and calling functions
This section introduces how to define a function, and how to call Python built-in and self-defined functions with both keywords & positional arguments. <br>
<br> Let's see several example codes for this demonstration.
```python
#1 Define a function
## Use the def keyword, followed by the function name and parentheses where to put defined parameters
##1.1 define a function without any parameters
def print_hello_world(): # keyword def, function name as print_hello_world and a parentheses, and no defined parameters in this function
    print("Hello World!")
##1.2 define a funtion with parameters
def add_numbers(x,y): # parameters x and y are in the parentheses
    addition = x + y
    return addition
```
```python
#Expected outcome from defining a function
# Nothing is here, as a function won't be executed until they are called!
```
```python
##2 Call a function
##2.1 call a function without any parameters
print_hello_world()
##2.2 call a function with parameters
### by keyword arguments
z1 = add_numbers(x=1,y=2) # here we use keyword argument x and y as defined in the add_numbers function
print("Sum of 1 and 2 by calling add_numbers with keyword argument: ", z1)
### by positional arguments
z2 = add_numbers(1,2) # here we use positional arguments 1 for x's position and 2 for y's position as defined in the add_numbers function
print("Sum of 1 and 2 by calling add_numbers with positional argument: ", z2)
##2.3 calling the same function for same type but different tasks
z3 = add_numbers(7,8)
z4 = add_numbers(237,856)
print("Task 1 of calling add_numbers:", z3)
print("Task 2 of calling add_numbers:", z4)
```
```python
#Expected outcome from calling a funciton
Hello World!
Sum of 1 and 2 by calling add_numbers with keyword argument:  3
Sum of 1 and 2 by calling add_numbers with positional argument:  3
Task 1 of calling add_numbers: 15
Task 2 of calling add_numbers: 1093
```

### 5.2 Lambda function
Python's lambda function is a small, anonymous function defined using the lambda keyword, which can take any number of arguments, but can only have one expression. The power of lambda functions mainly include 1) useful for writing quick, simple, and short functions that are used on-the-fly; 2) when a small function is in need for a specific task without cluttering the code with additional named functions. <br>
<br> Here list several examples of using lambda function within Python.
```python
# format to use initiate a lambda function is "lambda arguments : expression"
#1 Basic Lambda Function
##1.1 add function
add = lambda x : x + 10
print(add(1))
##1.2 lambda function within defined function
def lambda_use_func(n):
  return lambda x : x * n
### use lambda_use_func(n) to build a function to compute the 2 times a variable
double_function = lambda_use_func(2) #with lambda_use_func(2) we build a function with parameter as x and compute its product with 2
print(double_function(5))
triple_function = lambda_use_func(3) #with lambda_use_func(3) we build a function with parameter as x and compute its product with 3
print(triple_function(5))
### By here, we can see using lambda function within a defined function can help reduce the number of using def to define different functions
### we can use one function (e.g., lambda_use_func(n)) to create the functions to build other specific functions such as double_function and triple_function
### with that, lambda function helps make our code more concise and simple
```
```python
#Expected output from lambda function examples
11
10
15
```
### 5.3 Import external functions, modules, and libraries 
Python has a rich ecosystem of libraries and modules that can be imported and used in your own programs. Let's take a popular module math as an example! <br>
```python
#1 Importing the sqrt function (external function) from the math module
from math import sqrt
result_1 = sqrt(16)
print(result_1)
```
```python
#Expected output from sqrt function
4.0
```
```python
#2 Importing the entire math module
import math
result_2 = math.sqrt(25)
print(result_2)
```
```python
#Expected output from math module
5.0
```
## Chapter 6. Comprehensions 
Comprehensions in Python allow the creation of new collections by iterating over sequences and applying conditions or transformations in a single, readable line of code, which are generally faster and more concise than traditional loops. <br>
<br>Let's see several examples of code for the list and dictionary comprehensions.
### 6.1 List comprehensions
List comprehensions are used to create new lists by applying an expression to each element in an existing iterable (like a list, tuple, or range), which can include conditions to filter elements. <br>
```python
# basic format for list comprehension is: [expression for item in iterable]
## expression: The value to be added to the new list;
## item: The variable that represents each element in the iterable
## iterable: The collection being iterated over (e.g., a list, tuple, or range)

#1 list comprehension without conditions
## Traditional way using a loop
list_example_tradition = []
for x in range(10):
    list_example_tradition.append(x*2)
## List comprehension
list_example_comprehension = [x*2 for x in range(10)]

print('List from traditional loop: ', list_example_tradition)
print('List from list comprehension: ', list_example_comprehension)
```
```python
#Expected output from list comprehension without conditions
## we got same results from both traditional and list comprehension, while list comprehension is more concise and faster than traditional loop.
List from traditional loop:  [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
List from list comprehension:  [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```
```python
#2 list comprehension with conditions
list_example_comprehension_condition = [x*2 for x in range(10) if x%2==0] # we add a if condition so that only even number will be used to create the list_example_comprehension_condition
print('List from list comprehension with conditions: ', list_example_comprehension_condition)
```
```python
#Expected output from list comprehension with conditions
List from list comprehension with conditions:  [0, 4, 8, 12, 16]
```
### 6.2 Dictionary comprehensions
Dictionary comprehensions work similarly to list comprehensions but are used to create dictionaries. Instead of creating a list, key-value pairs will be created in a dictionary. <br>
```python
# basic format for Dictionary comprehension is: {key_expression: value_expression for item in iterable}
## key_expression: The expression that defines the key for each item.
## value_expression: The expression that defines the value for each item.
## item: The variable that represents each element in the iterable.

#1 Dictionary comprehension example
## Traditional way using a loop
dictionary_example_tradition = {}
for x in range(5):
    dictionary_example_tradition[x] = x*2
## List comprehension
dictionary_example_comprehension = {x: x*2 for x in range(5)}

print('Dictionary from traditional loop: ', dictionary_example_tradition)
print('Dictionary from dictionary comprehension: ', dictionary_example_comprehension)
```
```python
#Expected output from dictionary comprehension example
Dictionary from traditional loop:  {0: 0, 1: 2, 2: 4, 3: 6, 4: 8}
Dictionary from dictionary comprehension:  {0: 0, 1: 2, 2: 4, 3: 6, 4: 8}
```
```python
#2 Swapping Keys and Values with dictionary comprehension
## Original dictionary
fruit_to_color = {
    'apple': 'red',
    'banana': 'yellow',
    'grape': 'purple'
}

## Swapping keys and values
color_to_fruit = {color: fruit for fruit, color in fruit_to_color.items()}

print("Original dictionary: ", fruit_to_color)
print("Dictionary after swapping keys and values: ", color_to_fruit)

#Expected outcome from swapping Keys and Values with dictionary comprehension
Original dictionary:  {'apple': 'red', 'banana': 'yellow', 'grape': 'purple'}
Dictionary after swapping keys and values:  {'red': 'apple', 'yellow': 'banana', 'purple': 'grape'}
```
