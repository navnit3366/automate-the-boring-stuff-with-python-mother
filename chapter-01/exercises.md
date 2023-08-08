1. Which of the following are operators, and which are values?
```python
* # operator | string replicator or multiplication
"Hello" # value | string
-88.8 # value | float
- # operator | subtraction
/ # operator | Division
+ # operator | Addition
5 # value | integer
```

2. Which of the following is a variable, and which is a string?
```python
spam # variable
"spam" # string
```

3. Name the first three common data types.

| Data type | Example    |
| ----------| ---------- |
| Integer   | `21`, `2022`    | 
| Float | `21.0`, `2022.75`   |
| String | `"21"`, `"2022"`  |

4. What is an expression made up of? What do all expressions do?
	- Expressions are composed of a combination of values, operators, and variables. They all evaluate into a single value that belongs to a single data type.

5. This chapter introduced assignment statements, like `spam = 10`. What is the difference between an expression and a statement?
	- An expression is the fundamental unit of a program. They are composed of values, operators, and variables that evaluate into a single value. A statement, on the other hand, is composed of multiple expressions and represents an action or command that creates a noticeable change i.e. printing a string onto the screen.

6. What does the variable `bacon` contain after the following code runs?
	```python
	>>> bacon = 20
	>>> bacon + 1
	```
	- The `bacon` still contains the integer `20` since there are no reassignments or no statements that overwrote the value contained in the variable `bacon`.

7. What should the following two expressions evaluate to?
	```python
	>>> "spam" + "spamspam"

	>>> "spam" * 3*
	```
	- The first expression will evaluate as "spamspamspam".
	- The second expression will also evaluate as "spamspamspam".
	- They are both expressions that evaluate into the same string value of "spamspamspam". The first expression made use of the string concatenation operator `+` while the second expression uses the string replicator `*`.

8. Why is `eggs` is a valid variable identifier while `100` is invalid?
	- The reason for this is that `eggs` follow the specifications outlined by Python on what is considered a valid variable. Whilst `100` is not as it violates the rule that valid variable identifiers must never start with a number. Although, variable identifiers can contain a number.

9. What three functions can be used to get the integer, floating-point number, and string version of a value?
	- The `str()` function can be used to convert an object into its string form.
	- The `int()` function can be used to convert an object into its integer form.
	- The `float()` function can be used to convert an object into its floating-point number form.

10. Why does the expression `"I have eaten " + 99 + " burritos."` cause an error? How can you fix it?
	- The error is due to the fact that the addition of a string to an integer is ungrammatical in Python. To fix this, one must use the `str()` function to obtain the string form of the integer `99` before using string concatenation can be done. We cannot use the `int()` or `float()` functions to convert the string `"I have eaten "` and `" burritos."` as they do not have an equivalent integer or floating-point number form.
	```python
	>>> "I have eaten " + str(99) + " burritos."
	"I have eaten 99 burritos."
	```

**BONUS**
- The `round()` function is another built-in Python function that accepts an integer value and a precision parameter.
	- It rounds the integer value to the precision specified by the second argument. If the second argument is omitted, then the `round()` function returns the nearest integer to the input.
```python
>>> round(3.14159, 3)
3.142

>>> round(3.14159)
3
```