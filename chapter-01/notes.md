<div id="Top" />

### Expressions
- They are the fundamental form of instruction in Python. 
- Valid expressions are always evaluated by python to a single value which can be any type from *strings*, to *objects*.
- They are composed of a myriad of combinations of values, i.e. 42, 21, 2022, and operations, i.e. addition ( + ), and multiplication ( * ).

<p style="font-size: 14px; margin: 0; font-weight: bold;">Table 1.1 Math Operations According to Precedence</p>

| Operator | Operation        | Example  | Result |
|----------|------------------|----------|--------|
| **       | Exponent         | 8 ** 2   | 16     |
| %        | Modulus          | 10 % 3   | 1      |
| //       | Floored Division | 21 // 10 | 2      |
| /        | Division         | 12 / 3   | 4      |
| *        | Multiplication   | 9 * 9    | 81     |
| -        | Subtraction      | 100 - 100| 0      |
| +        | Addition         | 40 + 2   | 42     |
 
- Basically, the order in which python evaluates expressions that incorporate different combinations of mathematical operations is aligned to that of mathematics. It follows that one can manipulate this order of evaluating operations using a parenthesis `()` like in mathematics.
- Some operators can behave differently based on the types of values it is operating.
	- The `+` symbol can act as the *addition operator* to evaluate the result of adding two integers, two floats, or a combination of the two to produce the sum.
	```python
	>>> 4 + 3
	7
	```
	- The `+` symbol can also act as the *string concatenation operator* where it adds two strings together to produce a longer combination of the strings being operated.
	```python
	>>> "Loid " + "Forger"
	'Loid Forger'
	```
	- However, adding a string and an integer together will produce an error.
	```python
	>>> 40 + "2"
	Traceback (most recent call last):
		File "<stdin>", line 1, in <module>
	TypeError: can only concatenate str (not "int") to str
	```
	- The `*` operator can act as the *multiplication operator* to evaluate the result of multiplying two integers, two floats, or a combination of the two to produce the quotient.
	```python
	>>> 10 * 10
	100
	```
	- The `*` operator can also act as the *string replication operator* which will evaluate into a single string value that is the original string repeated a number of times equal to the integer.
	```python
	>>> "Daifuku" * 3
	'DaifukuDaifukuDaifuku'
	``` 
	- However, multiplying a string and a float will produce an error. This is expected because there are various nuances attributed to the idea of obtaining a replication of a string a fractional number of times. Think about how would you define `"Hello" * pi`?
	```python
	>>> "Daifuku" * 3.0
	Traceback (most recent call last):
	  File "<stdin>", line 1, in <module>
	TypeError: can't multiply sequence by non-int of type 'float'
	```
	- An error will also be produced when multiplying two strings together. This is expected because it doesn't make sense to replicate a string by a string number of times.
- This is due to the fact that Python does not convert either the string or the integer into any other value explicitly. One has to convert either `"40"` into an integer or `2` into a string in order for the `+` symbol to act as either the addition operator or the string concatenation operator. In other words, adding a string and an integer in Python is ungramattical.
```python
>>> 2 + 2
4

>>> "2" + "2"
'22'

>>> "I" + " love" + " peanuts."
'I love peanuts.'
```
-  Whitespaces between integers and operations alike are insignificant, but the initial indentation in any line of code is significant.
```python
>>> 40 + 2
42

>>>40      +      2
42
>>>             40 + 2

File "<stdin>", line 1
	40 + 2
    ^
IndentationError: unexpected indent
```

### Data Types

- Every value in Python belongs to exactly one built-in data type.
- Common python data types:
  
| Data type | Examples                |
| --------- | ----------------------- |
| Integers  | -1, 0, 1                |
| Floats    | -1.0, 0.0, 1.0          |
| Strings   | "Hello, World!", "2022" | 
- Python has other built-in data types such as `lists`, `tuple`, `dict`, `set`, `bool`, `functions` and `NoneType` among others.

### Variables
- A variable is a container inside a computer's memory that is associated with a symbolic name or an identifier.
- It can store any single value. So a variable can either contain a `string`, `int`, `tuple`, `dict`, and `NoneType` among others.
- A variable is initialized the moment a value has been stored in it. One can store values into a variable using an assignment statement which consists of an `identifier`, the `=` symbol, and the value to be stored. In the example below, we have an identifier, `anime` followed by the `=` symbol which instructs Python to store the string of `"Magic Kaito 1412"` into the variable.
```python
>>> anime = "Magic Kaito 1412"
'Magic Kaito 1412'
```
- The values stored inside variables can be overwritten by a more recent assignment to that variable.
```python
>>> anime = "Magic Kaito 1412"
>>> anime
'Magic Kaito 1412'

>>> anime = "Detective Conan"
>>> anime
'Detective Conan'
```
- The number of identifiers there can be is limitless. Any programmer can name their variables anything they want or have their own naming conventions for a specific project. However, there are restrictions that Python has implemented which dictate whether a potential identifier for a variable is valid or invalid.
	- The identifier cannot contain a space. It must be continuous.
	- The identifier can only contain valid letters, numbers, and the underscore `_` character.
	- The identifier cannot begin with a number.
- Variable identifiers are case-sensitive. This implies that spam, Spam, SPAM, and SpAm are all different and valid identifiers for a variable.
- Whatever identifiers one uses for their variables, one rule that must be upheld at all times is that the variable name must be descriptive of the value that it contains. This way, managing multiple variables in one's programs will be easier as one knows what values each variable hold just from reading the identifier.

### Dissecting the First Program
```python

# This program greets the user and asks for the user's name.
  
  
print("Hello, World!")


# Ask for a name
print("What is your name? ")
user_name = input()


print("It is good to meet you, " + user_name + ".")

# Obtain and display the length of the user's name
print("The length of your name is: ")
print(len(user_name))


# Ask for the user's age
print("What is your age?")
user_age = input()


print("You will be " + str(int(user_age) + 1) + " in a year.")
```

**Comments**
- The following line is called a comment:
```python
# This program greets the user and asks for the user's name.
```
- To create comments, the `#` symbol is used to precede any line. The characters afterwards will be treated as comments and will have a certain style depending on one's code editor or theme.
- Python ignores comments when executing any source code.
- Comments are used to write information that can be helpful to anyone reading one's code including oneself. 
	- They contain information about what the succeeding line of code does, or what the entire program is about. 
	- One can also use comments to write personal notes or other reminders.
	- However, it is good practice to not oversaturate any source code with comments as this will make it harder to read through the code which is the essence of the program itself. Therefore, keep comments succinct and informative.
- Comments can also be used to debug one's source code. If one's program is encountering errors, one can *comment out* lines of code as see if the error persists or not.
- Blank lines are also ignored by Python and can be incorporated into one's source code to add space between lines of code to make it easier to read. However, as with anything in life, do it with moderation. There is no point in scrolling through dozens of empty new lines if one's source code only consists of two lines of code.

**The `print()` Function**
- It is a built-in Python function that displays the value supplied inside its parenthesis onto the screen.
- The line below means "Print out the string "Hello, World!"."
```python
print("Hello, World!")
Hello, World!
```
- When Python executes this line, it is said that Python is *calling* the print function and the string `"Hello, World"` is being *passed* to the function as an `argument`.
- The print function does not display the quotes surrounding the string. They are merely markers for where the string value begins and ends.

**The `input()` Function**
- It is a built-in Python function that waits for and accepts input from the keyboard. The function ends when the user presses the `ENTER` key.
- It always converts the input into its string form and *returns* this value.
- In the line of code below, the `input()` function waits for the user's input and the `ENTER` key before evaluating the input into a string equal to the user input and assigning it to the variable with the identifier of `user_name`.
```python
user_name = input()
```

**The `len()` Function**
- It is a built-in Python function that outputs the length of an `iterable` value as an integer value.
- In the line of code below, the iterable value is the string stored in the variable `user_name`.
```python
user_name = "Loid Forger"
len(user_name) # 11
```
- If the value stored in `user_name` is `"Judz"`, then the `len(user_name)` would evaluate into the integer value of `4` since there are 4 letters that make up the length of my name. This value is then passed into the `print()` function which displays it onto the screen. Keep in mind that white spaces are considered as characters by Python and will therefore contribute to its length.

**Type Conversion Functions**
- The `str()` function will accept any object which will then be converted into its string form.
```python
str(2022) # "2022"
```
- The `int()` function will accept any object which will then be converted to its integer form.
```python
int("2022") # 2022

int(False) # 0

int(2.01) # 2
```
- The `float()` function will accept any object which will then be converted to its float form.
```python
float("2022") # 2022.0

float(True) # 1.0

float(10) # 10.0
```
- These functions are useful for when you want to operate between string, integer, and float data types i.e. When one wants to add the `str` `"40"` to the `int` `2`, then one can use the `int()` function to convert `"40"` into its integer form of `40` use the addition operator to obtain the integer `42`. One can also use the `str()` function to convert `2` into its string form, `2`, and use the string concatenation operator to obtain the string value of `"402"`.
- The functions `str()`, `int()`, and `float()` will return an error if they are passed with invalid arguments.
```python
>>> int("99.99")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '99.99'
```
- The reason for this is that in order to convert the string `"99.99"` into its integer form, one must first convert this into its float form `99.99` using the `float()` function and use the `int()` function to convert it into its integer form which is `99`. This process is not carried out implicitly by Python which is why an error occurs.
```python
>>> int(float("99.99"))
99
```
- Do note that although the string form of a number is completely different from its integer and float forms, an integer can be equal to its floating point form similar in mathematics. Python makes this distinction because strings are text, while floats and integers are numbers.
```python

>>> "42" == 42
False

>>> "42" == 42.0
False

>>> 42 == 42.000000
True

>>> 42 == 42.01
False
```


[⬆ Top](#Top)





