
# 🐍Python
## Preset
- Created by Guido van Rossum in 1990, Python 3 released in 2008
- Emphasizes readability and simplicity
- Official docs: [docs.python.org/3](https://docs.python.org/3)

## Table of Contents

- [Input and Output ](#input-and-output)
- [Variables](#variables)
- [Operators](#operators)
- [Keywords](#kaywords)
- [Data Types](#data-types)
- [Conditional Statements](#conditional-statements)
- [Loops](#loops)
- [Functions](#functions)
- [Different types of Data Structure](#different-types-of-data-structure)
- [Strings](#strings)
- [List](#list)
- [Tuples](#tuples)
- [Dictionary](#dictionary)
- [Sets](#sets)
- [Arrays](arrays)
- [List Comprehension](#list-comprehension)
- [Frozenset](#frozenset)
- [Exception Handling](#exception-handling)
- [File Handling](#file-handling)


## Input and Output 

This document summarizes all major types of input and output declarations in Python for quick reference.

#### 📥 Input Methods

| Type                       | Syntax / Example                                                                 |
|---------------------------|-----------------------------------------------------------------------------------|
| String Input              | `name = input("Enter your name: ")`                                              |
| Integer Input             | `age = int(input("Enter your age: "))`                                           |
| Float Input               | `price = float(input("Enter price: "))`                                          |
| Multiple Int Inputs       | `a, b = map(int, input().split())`                                               |
| List of Ints              | `nums = list(map(int, input().split()))`                                         |
| List of Strings           | `words = input().split()`                                                        |
| Characters List           | `chars = list(input())`                                                          |
| 2D Matrix Input           | `matrix = [list(map(int, input().split())) for _ in range(rows)]`                |
| Command-line Args         | `import sys\\nargs = sys.argv[1:]`                                               |

#### 📤 Output Methods

| Type                       | Syntax / Example                                                                 |
|---------------------------|-----------------------------------------------------------------------------------|
| Basic Print               | `print("Hello")`                                                                 |
| Print Variables           | `print("Name:", name)`                                                           |
| f-string Output           | `print(f"My name is {name}")`                                                    |
| Custom Separator          | `print("A", "B", sep="-")`                                                       |
| No Newline                | `print("Hello", end="")`                                                         |
| Format               | `print("{0} and Portal".format("Geeks"))`                                                         |


#### 📂 File Input/Output

| Type                       | Syntax / Example                                                                 |
|---------------------------|-----------------------------------------------------------------------------------|
| Read File                 | `with open("input.txt") as f: data = f.read()`                                   |
| Write to File             | `with open("file.txt", "w") as f: f.write("text")`                               |
| Append to File            | `with open("file.txt", "a") as f: f.write("more")`                               |
| Read Line by Line         | `for line in open("file.txt"):`                                                  |

#### 🔄 Loop Input

| Type                       | Syntax / Example                                                                 |
|---------------------------|-----------------------------------------------------------------------------------|
| Loop Input List           | `nums = []\\nfor _ in range(n): nums.append(int(input()))`                       |
| Loop 2D Matrix Input      | `for i in range(rows):\\n row = list(map(int, input().split()))\\n matrix.append(row)` |

#### ⚡ List Comprehension

| Type                       | Syntax / Example                                                                 |
|---------------------------|-----------------------------------------------------------------------------------|
| List of Ints              | `[int(x) for x in input().split()]`                                              |
| 2D Matrix Input           | `[list(map(int, input().split())) for _ in range(rows)]`                         |
| List of Squares           | `[x**2 for x in nums]`                                                           |
| Conditional List          | `[x for x in nums if x % 2 == 0]`                                                |

#### 🛡️ Error Handling

| Type                       | Syntax / Example                                                                 |
|---------------------------|-----------------------------------------------------------------------------------|
| Try/Except Input          | `try: val = int(input())\\nexcept ValueError: print("Invalid input")


# Variables

| **Type of Variable Declaration**      | **Description**                        | **Example**                                                                                               | **Output**                                                     |
| ------------------------------------- | -------------------------------------- | --------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| **Basic Variable Declaration**        | Assign value directly; dynamic typing  | `x = 10`<br>`name = "Rajashree"`                                                                          | `x = 10`<br>`name = 'Rajashree'`                               |
| **Multiple Variable Assignment**      | Assign multiple variables in one line  | `a, b, c = 1, 2, 3`<br>`x = y = z = "same"`                                                               | `a = 1, b = 2, c = 3`<br>`x = y = z = 'same'`                  |
| **Type Hinting (Python 3.5+)**        | Declare variable types for readability | `age: int = 25`<br>`name: str = "Rajashree"`                                                              | `age = 25`<br>`name = 'Rajashree'`                             |
| **Constants (By Convention)**         | Values that shouldn't change           | `PI = 3.14159`<br>`MAX_LIMIT = 100`                                                                       | `PI = 3.14159`<br>`MAX_LIMIT = 100`                            |
| **Global and Local Variables**        | Variables inside/outside functions     | `x = 100`<br>`def f(): y = 200`                                                                           | `x is global (accessible outside)`<br>`y is local (only in f)` |
| **Using `global` and `nonlocal`**     | Modify variable scope in functions     | `global count`<br>`nonlocal x` in nested function                                                         | Enables modifying outer/global variables                       |
| **Class and Instance Variables**      | Shared or per-instance values          | `class_var = 10`<br>`self.instance_var = 5`                                                               | `Class variable shared`<br>`Instance variable unique`          |
| **Data Structures as Variables**      | Lists, tuples, sets, dictionaries      | `my_list = [1,2,3]`<br>`my_dict = {"a": 1}`                                                               | `[1, 2, 3]`<br>`{'a': 1}`                                      |
| **NoneType Variable**                 | Variable assigned `None`               | `result = None`                                                                                           | `result = None`                                                |
| **Environment Variables**             | From OS environment                    | `import os`<br>`os.environ['API_KEY'] = 'key'`                                                            | `API_KEY='key'` (in environment)                               |
| **Assign Function to Variable**       | Function stored in a variable          | `def greet(): print("Hello")`<br>`say_hello = greet`<br>`say_hello()`                                     | `Hello`                                                        |
| **Passing Function as Argument**      | Function passed to another function    | `def greet(): return "Hi!"`<br>`def call_function(func): print(func())`<br>`call_function(greet)`         | `Hi!`                                                          |
| **Returning Functions from Function** | Function returns another function      | `def outer(): def inner(): return "I'm the inner function!"`<br>`my_func = outer()`<br>`print(my_func())` | `I'm the inner function!`                                      |
| **Insert Variable into a String**     | Combine variable and string            | `f"My name is {name}"`<br>`"My age is {}".format(age)`<br>`"Age: " + str(age)`                            | `"My name is Rajashree"`<br>`My age is 25`<br>`Age: 25`        |
| **Type Casting – Implicit**           | Python auto-converts types             | `z = 5 + 3.2`                                                                                             | `z = 8.2`                                                      |
| **Type Casting – Explicit**           | Manual conversion                      | `int("10") → 10`<br>`float(5) → 5.0`<br>`str(123) → '123'`<br>`bool(0) → False`                           | `10`, `5.0`, `'123'`, `False`                                  |


# Operators
| **Operator Type** | **Operator** | **Example**      | **Description**    |
| ----------------- | ------------ | ---------------- | ------------------ |
| **Arithmetic**    | `+`          | `2 + 3` → `5`    | Addition           |
|                   | `-`          | `5 - 2` → `3`    | Subtraction        |
|                   | `*`          | `3 * 4` → `12`   | Multiplication     |
|                   | `/`          | `10 / 2` → `5.0` | Division (float)   |
|                   | `//`         | `10 // 3` → `3`  | Floor division     |
|                   | `%`          | `10 % 3` → `1`   | Modulo (remainder) |
|                   | `**`         | `2 ** 3` → `8`   | Exponentiation     |
| Comparison | == | 5 == 5 → True | Equal to |
| | != | 5 != 3 → True | Not equal to |
| | > | 5 > 3 → True | Greater than |
| | < | 2 < 3 → True | Less than |
| | >= | 5 >= 5 → True | Greater than or equal to |
| | <= | 3 <= 4 → True | Less than or equal to |
| Logical | and | True and False → False | Logical AND |
| | or | True or False → True | Logical OR |
| | not | not True → False | Logical NOT |
| Bitwise | & | 5 & 3 → 1 | AND |
| | \| | 5 \| 3 → 7 | OR |
| | ^ | 5 ^ 3 → 6 | XOR |
| | ~ | ~5 → -6 | NOT |
| | << | 2 << 1 → 4 | Left Shift |
| | >> | 4 >> 1 → 2 | Right Shift |
| Assignment | = | a = 5 | Assign value |
| | += | a += 2 → a = a + 2 | Add and assign |
| | -= | a -= 3 → a = a - 3 | Subtract and assign |
| | *= | a *= 2 → a = a * 2 | Multiply and assign |
| | /= | a /= 2 | Divide and assign |
| | //=, %= | a %= 2 | Floor/Modulo assign |
| | **=, &=, |=, ^=, <<=, >>= | Compound assignment |
| Identity | is | a is b | True if same object |
| | is not | a is not b | True if not same object |
| Membership | in | 'a' in 'apple' → True | Is member |
| | not in | 'x' not in 'apple' → True | Not member |
| Modulo | % | 10 % 3 → 1 | Remainder of division |
| Division | / | 10 / 4 → 2.5 | True division |
| | // | 10 // 4 → 2 | Floor division |
| Ternary Operator | x if condition else y | a = 10 if b > 5 else 20 | Conditional expression |
| Operator Overloading | +, -, etc. | class A: def __add__(self, other): ... | Custom behavior for operators in classes |
| OR (Logical) | or | True or False → True | Used to combine conditions |

# Keywords
| Keyword        | Description                               | Example                                  |
|----------------|-------------------------------------------|------------------------------------------|
| `False`        | Boolean value                             | `x = False`                              |
| `None`         | Represents null value                     | `x = None`                               |
| `True`         | Boolean value                             | `x = True`                               |
| `and`          | Logical AND                               | `if a > 0 and b > 0:`                    |
| `as`           | Alias or context manager                  | `import numpy as np`                     |
| `assert`       | Debugging check                           | `assert x > 0`                           |
| `async`        | Declare asynchronous function             | `async def fetch():`                    |
| `await`        | Wait for async result                     | `await fetch()`                          |
| `break`        | Exit loop                                 | `if x == 5: break`                       |
| `class`        | Define a class                            | `class Person:`                          |
| `continue`     | Skip iteration in loop                    | `if x % 2 == 0: continue`                |
| `def`          | Define function                           | `def greet():`                           |
| `del`          | Delete object                             | `del my_list[0]`                         |
| `elif`         | Else if condition                         | `elif x == 2:`                           |
| `else`         | Else condition                            | `else:`                                  |
| `except`       | Handle exception                          | `except ValueError:`                     |
| `finally`      | Run no matter what                        | `finally:`                               |
| `for`          | Looping                                   | `for i in range(5):`                     |
| `from`         | Import specific part                      | `from math import sqrt`                  |
| `global`       | Declare global variable                   | `global counter`                         |
| `if`           | Conditional branching                     | `if x > 0:`                              |
| `import`       | Import module                             | `import os`                              |
| `in`           | Check membership                          | `if 3 in [1,2,3]:`                        |
| `is`           | Identity comparison                       | `if a is b:`                             |
| `lambda`       | Anonymous function                        | `f = lambda x: x + 1`                    |
| `nonlocal`     | Declare outer function variable           | `nonlocal count`                         |
| `not`          | Logical NOT                               | `if not valid:`                          |
| `or`           | Logical OR                                | `if a > 5 or b < 3:`                     |
| `pass`         | Do nothing                                | `if x > 0: pass`                         |
| `raise`        | Raise exception                           | `raise ValueError("Invalid")`           |
| `return`       | Exit function and return value            | `return x + y`                           |
| `try`          | Try block for exception                   | `try:`                                   |
| `while`        | While loop                                | `while x < 5:`                           |
| `with`         | Context manager                           | `with open("file.txt") as f:`           |
| `yield`        | Yield value in generator                  | `yield x`                                |

# Data Types
| Type      | Category      | Description                      | Example                |
| --------- | ------------- | -------------------------------- | ---------------------- |
| `int`     | Primitive     | Integer values                   | `x = 10`               |
| `float`   | Primitive     | Decimal/real numbers             | `x = 10.5`             |
| `complex` | Primitive     | Complex numbers                  | `x = 3 + 4j`           |
| `bool`    | Primitive     | Boolean values: True or False    | `x = True`             |
| `str`     | Primitive     | Sequence of characters (strings) | `x = "Hello"`          |
| `list`    | Non-Primitive | Ordered, mutable collection      | `x = [1, 2, 3]`        |
| `tuple`   | Non-Primitive | Ordered, immutable collection    | `x = (1, 2, 3)`        |
| `set`     | Non-Primitive | Unordered, no duplicates         | `x = {1, 2, 3}`        |
| `dict`    | Non-Primitive | Key-value pairs                  | `x = {"a": 1, "b": 2}` |
| Function       | Purpose                         | Example Input        | Output            |
| -------------- | ------------------------------- | -------------------- | ----------------- |
| `int()`        | Convert to integer              | `int("10")`          | `10`              |
| `float()`      | Convert to float                | `float("3.14")`      | `3.14`            |
| `complex()`    | Convert to complex number       | `complex(2, 3)`      | `(2+3j)`          |
| `bool()`       | Convert to boolean              | `bool(0)`            | `False`           |
| `str()`        | Convert to string               | `str(100)`           | `'100'`           |
| `list()`       | Convert to list                 | `list("abc")`        | `['a', 'b', 'c']` |
| `tuple()`      | Convert to tuple                | `tuple([1, 2])`      | `(1, 2)`          |
| `set()`        | Convert to set                  | `set([1, 2, 2])`     | `{1, 2}`          |
| `dict()`       | Create dictionary from pairs    | `dict([('a',1)])`    | `{'a': 1}`        |
| `type()`       | Get type of variable            | `type(3.14)`         | `<class 'float'>` |
| `isinstance()` | Check data type                 | `isinstance(5, int)` | `True`            |
| `len()`        | Get length of sequence or dict  | `len("hello")`       | `5`               |
| `round()`      | Round a float                   | `round(3.56)`        | `4`               |
| `format()`     | Format string or numbers        | `"{}".format(5)`     | `'5'`             |
| `repr()`       | String representation of object | `repr("abc")`        | `"'abc'"`         |
| `eval()`       | Evaluate expression from string | `eval("3 + 5")`      | `8`               |

# Conditional Statements
| **#** | **Type**                        | **Syntax / Description**                                                                | **Example**                                                                                                                           | **Output**            |
| ----- | ------------------------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
| 1     | **Simple `if`**                 | `if condition:`<br>    `# code`                                                         | `x = 10`<br>`if x > 5:`<br>    `print("x is greater than 5")`                                                                         | `x is greater than 5` |
| 2     | **`if-else`**                   | `if condition:`<br>    `# code`<br>`else:`<br>    `# code`                              | `x = 3`<br>`if x > 5:`<br>    `print("Big")`<br>`else:`<br>    `print("Small")`                                                       | `Small`               |
| 3     | **`if-elif-else`**              | `if cond1:`<br>    `# code`<br>`elif cond2:`<br>    `# code`<br>`else:`<br>    `# code` | `x = 0`<br>`if x > 0:`<br>    `print("Positive")`<br>`elif x == 0:`<br>    `print("Zero")`<br>`else:`<br>    `print("Negative")`      | `Zero`                |
| 4     | **Nested `if`**                 | `if cond1:`<br>    `if cond2:`<br>        `# code`                                      | `x = 15`<br>`if x > 10:`<br>    `if x < 20:`<br>        `print("Between 10 and 20")`                                                  | `Between 10 and 20`   |
| 5     | **One-line if**                 | `if condition: statement`                                                               | `x = 7`<br>`if x > 5: print("x is greater than 5")`                                                                                   | `x is greater than 5` |
| 6     | **One-line if-else**            | `val = a if condition else b`                                                           | `x = 8`<br>`result = "Even" if x % 2 == 0 else "Odd"`<br>`print(result)`                                                              | `Even`                |
| 7     | **Multiple conditions**         | `if cond1 and cond2:`<br>    `# code`                                                   | `x = 10; y = 5`<br>`if x > 5 and y < 10:`<br>    `print("Valid")`                                                                     | `Valid`               |
| 8     | **`if` with `and`**             | `if a and b:`<br>    `# code`                                                           | `is_logged_in = True`<br>`is_admin = True`<br>`if is_logged_in and is_admin:`<br>    `print("Access granted")`                        | `Access granted`      |
| 9     | **`match-case` (Python 3.10+)** | `match variable:`<br>`case value1:`<br>    `# code`<br>`case value2:`<br>    `# code`   | `fruit = "apple"`<br>`match fruit:`<br>`case "apple":`<br>    `print("Red fruit")`<br>`case "banana":`<br>    `print("Yellow fruit")` | `Red fruit`           |
| 10    | **Ternary Operator**            | `value_if_true if condition else value_if_false`                                        | `a, b = 5, 10`<br>`min_val = a if a < b else b`<br>`print(min_val)`                                                                   | `5`                   |                                                                   |

# Loops
| **#** | **Topic**                       | **Explanation**                                    | **Example**                                                                                       | **Output**                       |
| ----- | ------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------- | -------------------------------- |
| 1     | **`for` Loop**                  | Iterates over a sequence (list, string, etc.)      | `for i in [1, 2, 3]: print(i)`                                                                    | `1`<br>`2`<br>`3`                |
| 2     | **For Loop with String**        | Loops through each character                       | `for ch in "Hi": print(ch)`                                                                       | `H`<br>`i`                       |
| 3     | **`range()` with For Loop**     | Iterates over a range of numbers                   | `for i in range(3): print(i)`                                                                     | `0`<br>`1`<br>`2`                |
| 4     | **`range(start, stop, step)`**  | Custom range control                               | `for i in range(2, 10, 3): print(i)`                                                              | `2`<br>`5`<br>`8`                |
| 5     | **`continue` Statement**        | Skips current iteration                            | `for i in range(5): if i==2: continue; print(i)`                                                  | `0`<br>`1`<br>`3`<br>`4`         |
| 6     | **`break` Statement**           | Exits loop early                                   | `for i in range(5): if i==3: break; print(i)`                                                     | `0`<br>`1`<br>`2`                |
| 7     | **`pass` Statement**            | Does nothing (placeholder)                         | `for i in range(2): pass`                                                                         | *(No output)*                    |
| 8     | **For-Else**                    | Runs `else` if loop **doesn't break**              | `for i in range(2): print(i); else: print("Done")`                                                | `0`<br>`1`<br>`Done`             |
| 9     | **For-Else with Break**         | Skips `else` if loop **breaks**                    | `for i in range(3): if i==1: break; print(i); else: print("Done")`                                | `0`                              |
| 10    | **`enumerate()` with For Loop** | Index and item from sequence                       | `for i, v in enumerate(['a','b']): print(i, v)`                                                   | `0 a`<br>`1 b`                   |
| 11    | **Nested For Loop**             | Loop inside a loop                                 | `for i in range(2): for j in range(2): print(i,j)`                                                | `0 0`<br>`0 1`<br>`1 0`<br>`1 1` |
| 12    | **`while` Loop**                | Repeats **as long as** a condition is True         | `i = 0`<br>`while i < 3:`<br>    `print(i)`<br>    `i += 1`                                       | `0`<br>`1`<br>`2`                |
| 13    | **Infinite `while` Loop**       | Condition is always True (use `break` to stop)     | `while True:`<br>    `print("Run")`<br>    `break`                                                | `Run`                            |
| 14    | **`while` with `continue`**     | Skips current iteration                            | `i = 0`<br>`while i < 3:`<br>    `i += 1`<br>    `if i == 2: continue`<br>    `print(i)`          | `1`<br>`3`                       |
| 15    | **`while` with `break`**        | Exits when condition met                           | `i = 0`<br>`while i < 5:`<br>    `if i == 3: break`<br>    `print(i)`<br>    `i += 1`             | `0`<br>`1`<br>`2`                |
| 16    | **`while`-`else`**              | `else` executes if no break                        | `i = 0`<br>`while i < 2:`<br>    `print(i)`<br>    `i += 1`<br>`else:`<br>    `print("Done")`     | `0`<br>`1`<br>`Done`             |
| 17    | **Simulated `do-while` Loop**   | Loop runs **at least once**, then checks condition | `i = 0`<br>`while True:`<br>    `print(i)`<br>    `i += 1`<br>    `if i >= 3:`<br>        `break` | `0`<br>`1`<br>`2`                |


# Functions

| **#** | **Concept**                    | **Explanation**                                             | **Example Code**                                                                                                                                                                                                                   | **Output**                     |
| ----- | ------------------------------ | ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ |
| 1     | **Basic Python Function**      | Defines reusable blocks of code using `def`.                | `def greet():`<br>`    print("Hello!")`<br>`greet()`                                                                                                                                                                               | `Hello!`                       |
| 2     | **Pass Statement in Function** | `pass` is used when the function has no implementation yet. | `def future_function():`<br>`    pass`                                                                                                                                                                                             | *(No output)*                  |
| 3     | **Global and Local Variables** | Local vars exist inside a function; global vars outside.    | `x = 10`<br>`def show():`<br>`    x = 5`<br>`    print("Local x:", x)`<br>`show()`<br>`print("Global x:", x)`                                                                                                                      | `Local x: 5`<br>`Global x: 10` |
| 4     | **Recursion in Python**        | A function calling itself to solve smaller subproblems.     | `def factorial(n):`<br>`    if n == 1:`<br>`        return 1`<br>`    return n * factorial(n - 1)`<br>`print(factorial(5))`                                                                                                        | `120`                          |
| 5     | **\*args in Function**         | Pass variable number of non-keyworded arguments.            | `def add(*numbers):`<br>`    total = 0`<br>`    for num in numbers:`<br>`        total += num`<br>`    return total`<br>`print(add(1, 2, 3))`                                                                                      | `6`                            |
| 6     | **\*\*kwargs in Function**     | Pass variable number of keyworded arguments.                | `def print_info(**kwargs):`<br>`    for key, value in kwargs.items():`<br>`        print(key, ":", value)`<br>`print_info(name="Raj", age=25)`                                                                                     | `name : Raj`<br>`age : 25`     |
| 7     | **'self' as Default Argument** | Refers to the instance of the class in object methods.      | `class Person:`<br>`    def greet(self):`<br>`        print("Hello from instance")`<br>`p = Person()`<br>`p.greet()`                                                                                                               | `Hello from instance`          |
| 8     | **First-Class Function**       | Functions passed as arguments, returned, or assigned.       | `def shout(text):`<br>`    return text.upper()`<br>`def greet(func):`<br>`    print(func("hello"))`<br>`greet(shout)`                                                                                                              | `HELLO`                        |
| 9     | **Lambda Function**            | Small anonymous function using lambda. <br>  `Syntax = lambda arguments:expression `                   | `square = lambda x: x * x`<br>`print(square(5))`                                                                                                                                                                                   | `25`                           |
| 10    | **Map Function**               | Applies a function to every item of an iterable.<br>`Syntax = map(function,iterable)`         | `nums = [1, 2, 3, 4]`<br>`squared = list(map(lambda x: x*x, nums))`<br>`print(squared)`                                                                                                                                            | `[1, 4, 9, 16]`                |
| 11    | **Reduce Function**            | Applies rolling computation to items (from functools).<br>`syntax = from functools import reduce reduce(function,iterable) `    | `from functools import reduce`<br>`nums = [1, 2, 3, 4]`<br>`product = reduce(lambda x, y: x * y, nums)`<br>`print(product)`                                                                                                        | `24`                           |
| 12    | **Filter Function**            | Filters elements based on a condition.<br>`syntax = filter(function,iterable) `                     | `nums = [1, 2, 3, 4, 5]`<br>`even = list(filter(lambda x: x % 2 == 0, nums))`<br>`print(even)`                                                                                                                                     | `[2, 4]`                       |
| 13    | **Inner Function**             | Function defined inside another function.                   | `def outer():`<br>`    def inner():`<br>`        print("Inner function")`<br>`    inner()`<br>`outer()`                                                                                                                            | `Inner function`               |
| 14    | **Decorators**                 | Wraps a function to extend its behavior.                    | `def decorator(func):`<br>`    def wrapper():`<br>`        print("Before")`<br>`        func()`<br>`        print("After")`<br>`    return wrapper`<br>`@decorator`<br>`def say_hello():`<br>`    print("Hello")`<br>`say_hello()` | `Before`<br>`Hello`<br>`After` |


# Different types of Data Structure
🧱 Built-in Data Structures
| **Data Structure**            | **Type** | **Description**                       | **Example (code line by line)**                                                               |
| ----------------------------- | -------- | ------------------------------------- | --------------------------------------------------------------------------------------------- |
| **List**                      | Built-in | Ordered, mutable, allows duplicates   | my\_list = \[1, 2, 3, 4]<br>my\_list.append(5)<br>print(my\_list)  # Output: \[1, 2, 3, 4, 5] |
| **Tuple**                     | Built-in | Ordered, immutable, allows duplicates | my\_tuple = (1, 2, 3)<br>print(my\_tuple\[0])  # Output: 1                                    |
| **Set**                       | Built-in | Unordered, mutable, no duplicates     | my\_set = {1, 2, 2, 3}<br>print(my\_set)  # Output: {1, 2, 3}                                 |
| **FrozenSet**                 | Built-in | Immutable version of set              | frozen = frozenset(\[1, 2, 3])<br>print(frozen)  # Output: frozenset({1, 2, 3})               |
| **Dictionary (dict)**         | Built-in | Key-value pairs, mutable              | my\_dict = {'a': 1, 'b': 2}<br>print(my\_dict\['a'])  # Output: 1                             |
| **String**                    | Built-in | Immutable sequence of characters      | text = "hello"<br>print(text\[1])  # Output: e                                                |
| **Array (from array module)** | Module   | Efficient list for numeric data       | from array import array<br>arr = array('i', \[1, 2, 3])<br>print(arr\[0])  # Output: 1        |

📚 User-defined Data Structures

| **Data Structure**     | **Description**             | **Example (line by line)**                                                                                                                         |
| ---------------------- | --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Stack (LIFO)**       | Last In First Out           | stack = \[]<br>stack.append(1)<br>stack.append(2)<br>stack.pop()  # Output: 2                                                                                        |
| **Queue (FIFO)**       | First In First Out          | from collections import deque<br>queue = deque()<br>queue.append(1)<br>queue.popleft()  # Output: 1                                                                  |
| **Linked List**        | Nodes connected in sequence | class Node:<br>  def **init**(self, data):<br>    self.data = data<br>    self.next = None<br>head = Node(1)<br>head.next = Node(2)<br>print(head.data)  # Output: 1 |
| **Doubly Linked List** | Each node has prev and next | Similar to linked list, but with `prev` pointer too                                                                                                                  |
| **Tree**               | Hierarchical structure      | class TreeNode:<br>  def **init**(self, value):<br>    self.value = value<br>    self.left = None<br>    self.right = None                                           |
| **Graph**              | Nodes connected by edges    | graph = {<br>  'a': \['b', 'c'],<br>  'b': \['a', 'd'],<br>  'c': \['a'],<br>}<br>print(graph\['a'])  # Output: \['b', 'c']                                          |

🏗️ Advanced Data Structures 
| **Data Structure**             | **Module**    | **Example**                                                                                                                    |
| ------------------------------ | ------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **deque (Double-ended queue)** | `collections` | from collections import deque<br>dq = deque(\[1, 2, 3])<br>dq.appendleft(0)<br>print(dq)  # Output: deque(\[0, 1, 2, 3])       |
| **defaultdict**                | `collections` | from collections import defaultdict<br>d = defaultdict(int)<br>d\['a'] += 1<br>print(d\['a'])  # Output: 1                     |
| **OrderedDict**                | `collections` | from collections import OrderedDict<br>od = OrderedDict()<br>od\['a'] = 1<br>print(od)                                         |
| **Counter**                    | `collections` | from collections import Counter<br>c = Counter("hello")<br>print(c)  # Output: Counter({'l': 2, 'h': 1, 'e': 1, 'o': 1})       |
| **NamedTuple**                 | `collections` | from collections import namedtuple<br>Point = namedtuple('Point', 'x y')<br>p = Point(1, 2)<br>print(p.x)  # Output: 1         |
| **Heap (Priority Queue)**      | `heapq`       | import heapq<br>heap = \[3, 1, 4]<br>heapq.heapify(heap)<br>heapq.heappush(heap, 2)<br>print(heapq.heappop(heap))  # Output: 1 |

# Strings

| **Topic**                                   | **Description**                             | **Example Code**                                                                       | **Output**                             |
| ------------------------------------------- | ------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------- |
| **1. String Slicing**                       | Extract a portion using `[start:stop:step]` | `text = "Python"`<br>`print(text[1:4])`                                                | `yth`                                  |
|                                             | Negative indexing                           | `print(text[-4:-1])`                                                                   | `tho`                                  |
| **2. f-Strings**                            | Embed variables inside strings              | `name = "Raj"`<br>`age = 25`<br>`print(f"My name is {name} and I am {age} years old")` | `My name is Raj and I am 25 years old` |
| **3. String Comparison**                    | Compare strings using `==`, `<`, `>`        | `a = "apple"`<br>`b = "banana"`<br>`print(a == b)`<br>`print(a < b)`                   | `False`<br>`True`                      |
| **4. Useful String Functions**              | `.lower()` to lowercase                     | `"HeLLo".lower()`                                                                      | `hello`                                |
|                                             | `.upper()` to uppercase                     | `"python".upper()`                                                                     | `PYTHON`                               |
|                                             | `.strip()` to remove whitespace             | `" hello ".strip()`                                                                    | `hello`                                |
|                                             | `.replace()` to replace characters          | `"hi world".replace("hi", "hello")`                                                    | `hello world`                          |
|                                             | `.find()` to find index                     | `"hello".find("e")`                                                                    | `1`                                    |
|                                             | `.startswith()` to check prefix             | `"hello".startswith("he")`                                                             | `True`                                 |
|                                             | `.endswith()` to check suffix               | `"test.py".endswith(".py")`                                                            | `True`                                 |
| **5. Convert int to string**                | Use `str()` function                        | `num = 123`<br>`s = str(num)`<br>`print(s)`                                            | `123`                                  |
| **6. Convert string to int**                | Use `int()` function                        | `s = "456"`<br>`num = int(s)`<br>`print(num + 1)`                                      | `457`                                  |
| **7. String Concatenation**                 | Using `+` operator                          | `a = "Hi"`<br>`b = "There"`<br>`print(a + b)`                                          | `HiThere`                              |
| **8. Split string into list of characters** | Use `list()`                                | `text = "hello"`<br>`print(list(text))`                                                | `['h', 'e', 'l', 'l', 'o']`            |
| **9. Iterate over characters**              | Use a for loop                              | `for c in "dog":`<br>`    print(c)`                                                    | `d`<br>`o`<br>`g`                      |
| **10. String to List**                      | Using `split()` method                      | `s = "a b c"`<br>`print(s.split())`                                                    | `['a', 'b', 'c']`                      |
| **11. List to String**                      | Use `"".join()`                             | `lst = ['a', 'b', 'c']`<br>`print("".join(lst))`                                       | `abc`                                  |
| **12. String Comparison**                   | Again, for clarity                          | `print("abc" == "ABC")`                                                                | `False`                                |
| **13. String Formatting**                   | `.format()` method                          | `"{} is {}".format("Python", "cool")`                                                  | `Python is cool`                       |
|                                             | `%` operator formatting                     | `"Score: %d" % 90`                                                                     | `Score: 90`                            |
| **14. String Methods**                      | `.title()` capitalizes each word            | `"my name".title()`                                                                    | `My Name`                              |
|                                             | `.capitalize()` first letter capital        | `"hello".capitalize()`                                                                 | `Hello`                                |
| **15. String Exercise**                     | Reverse a string                            | `s = "apple"`<br>`print(s[::-1])`                                                      | `elppa`                                |
| **16. Escape Characters**                   | Use `\\` for backslash                      | `print("Backslash: \\\\")`                                                             | `Backslash: \\`                        |
|                                             | `\'` single quote inside single quotes      | `print('It\\'s fine')`                                                                 | `It's fine`                            |
|                                             | `\"` double quote inside double quotes      | `print("He said, \\\"Hi\\\"")`                                                         | `He said, "Hi"`                        |
|                                             | `\t` tab space                              | `print("Name:\tRaj")`                                                                  | `Name:	Raj`                            |
|--
| **Raw strings `r"string"`**                               | Raw strings treat backslashes `\` as literal characters, useful for Windows paths and regex patterns. |
|                                                           | `path = r"C:\Users\Raj\Documents"`                                                                    |
|                                                           | `print(path)` # Output: C:\Users\Raj\Documents                                                        |
|                                                           | `print("C:\\Users\\Raj\\Documents")` # same output                                                    |
| **Multiline strings `"""string"""`**                      | Used to create strings spanning multiple lines, preserving line breaks and indentation.               |
|                                                           | `text = """This is line 1`                                                                            |
|                                                           | `This is line 2`                                                                                      |
|                                                           | `This is line 3"""`                                                                                   |
|                                                           | `print(text)`                                                                                         |
|                                                           | Output:                                                                                               |
|                                                           | `This is line 1`                                                                                      |
|                                                           | `This is line 2`                                                                                      |
|                                                           | `This is line 3`                                                                                      |
| **String encoding and decoding `.encode()`, `.decode()`** | Strings are Unicode; `.encode()` converts to bytes; `.decode()` converts bytes back to strings.       |
|                                                           | `s = "Hello"`                                                                                         |
|                                                           | `b = s.encode("utf-8")`                                                                               |
|                                                           | `print(b)` # b'Hello'                                                                                 |
|                                                           | `s2 = b.decode("utf-8")`                                                                              |
|                                                           | `print(s2)` # Hello                                                                                   |
| **Regular expressions with `re` module**                  | Used for pattern matching and text processing with powerful regex features.                           |
|                                                           | `import re`                                                                                           |
|                                                           | `text = "The rain in Spain"`                                                                          |
|                                                           | `result = re.findall(r"\bS\w+", text)`  # Finds words starting with 'S'                               |
|                                                           | `print(result)` # \['Spain']                                                                          |
| **Immutable nature of strings**                           | Strings cannot be changed after creation. Any modification returns a new string.                      |
|                                                           | `s = "hello"`                                                                                         |
|                                                           | `# s[0] = 'H'  # Error: TypeError`                                                                    |
|                                                           | `s2 = "H" + s[1:]`                                                                                    |
|                                                           | `print(s2)` # Hello                                                                                   |
| **String translation and mapping `.translate()`**         | Replaces characters according to a translation table created by `.maketrans()`.                       |
|                                                           | `table = str.maketrans("aeiou", "12345")`  # Map vowels to digits                                     |
|                                                           | `s = "hello world"`                                                                                   |
|                                                           | `print(s.translate(table))` # h2ll4 w4rld                                                             |


# List

| **Category**                   | **Program Type**                                      | **Example Code**                               | **Output**                                     |
| ------------------------------ | ----------------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| **List Creation**              | Create List with Elements                             | `my_list = [1, 2, 3, 4, 5]`                    | `[1, 2, 3, 4, 5]`                              |
|                                | Empty List                                            | `empty_list = []`                              | `[]`                                           |
|                                | Using range()                                         | `range_list = list(range(1, 6))`               | `[1, 2, 3, 4, 5]`                              |
| **List Add/Append**            | Append Element                                        | `my_list.append(6)`                            | `[1, 2, 3, 4, 5, 6]`                           |
|                                | Insert at Index                                       | `my_list.insert(2, 10)`                        | `[1, 2, 10, 3, 4, 5, 6]`                       |
|                                | Extend List                                           | `my_list.extend([7, 8])`                       | `[1, 2, 10, 3, 4, 5, 6, 7, 8]`                 |
| **List Removal**               | Remove by Value                                       | `my_list.remove(2)`                            | `[1, 10, 3, 4, 5, 6, 7, 8]`                    |
|                                | Remove by Index                                       | `del my_list[0]`                               | `[10, 3, 4, 5, 6, 7, 8]`                       |
|                                | Pop Element                                           | `last = my_list.pop()`                         | `last = 8`, list now `[10, 3, 4, 5, 6, 7]`     |
| **List Count**                 | Count Occurrences                                     | `my_list.count(3)`                             | `1`                                            |
|                                | Length of List                                        | `len(my_list)`                                 | `6`                                            |
| **List Checking**              | Element Exists                                        | `if 4 in my_list:`<br>`    print("Exists")`    | `Exists`                                       |
|                                | List is Empty                                         | `if not my_list:`<br>`    print("Empty")`      | *(No output if list not empty)*                |
| **List with Dict**             | List of Dicts                                         | `users = [{'name': 'Alice'}, {'name': 'Bob'}]` | `[{'name': 'Alice'}, {'name': 'Bob'}]`         |
|                                | Access Value                                          | `print(users[0]['name'])`                      | `Alice`                                        |
| **List of List**               | Create 2D List                                        | `matrix = [[1, 2], [3, 4]]`                    | `[[1, 2], [3, 4]]`                             |
|                                | Access Element                                        | `val = matrix[1][0]`                           | `3`                                            |
| **List with Set**              | Convert List to Set                                   | `my_set = set(my_list)`                        | `{10, 3, 4, 5, 6, 7}` (order varies)           |
|                                | Remove Duplicates                                     | `unique = list(set(my_list))`                  | List of unique elements (order varies)         |
| **List with Tuple**            | List of Tuples                                        | `pairs = [(1, 'a'), (2, 'b')]`                 | `[(1, 'a'), (2, 'b')]`                         |
|                                | Access Tuple Element                                  | `print(pairs[0][1])`                           | `a`                                            |
| **List Methods**               | Sort List                                             | `my_list.sort()`                               | Sorted list                                    |
|                                | Reverse List                                          | `my_list.reverse()`                            | Reversed list                                  |
|                                | Index of Element                                      | `my_list.index(3)`                             | Index of `3` in list (e.g., `1`)               |
|                                | Clear List                                            | `my_list.clear()`                              | `[]`                                           |
| **List Slicing**               | Slice Elements                                        | `slice = my_list[1:4]`                         | Sublist from index 1 to 3                      |
|                                | Reverse with Slicing                                  | `reversed_list = my_list[::-1]`                | List reversed                                  |
| **List Comprehensions**        | Creating lists using concise syntax                   | `[x*x for x in range(5)]`                      | `[0, 1, 4, 9, 16]`                             |
| **Nested List Comprehensions** | Comprehensions inside comprehensions                  | `[[i*j for j in range(3)] for i in range(4)]`  | `[[0, 0, 0], [0, 1, 2], [0, 2, 4], [0, 3, 6]]` |
| **List Copying**               | Shallow vs deep copy                                  | `copy_list = my_list[:]` or `import copy`      | A copy of the list                             |
| **List Iteration**             | Looping through list elements                         | `for item in my_list: print(item)`             | Prints each item on a new line                 |
| **List Filtering**             | Using `filter()` or list comprehension with condition | `[x for x in my_list if x > 3]`                | List with elements > 3                         |
| **Sorting with Key Function**  | Sorting with custom keys                              | `my_list.sort(key=lambda x: x%2)`              | List sorted by even/odd                        |
| **List to String Conversion**  | Joining list elements into a string                   | `",".join(["a", "b", "c"])`                    | `"a,b,c"`                                      |
| **Enumerate**                  | Get index and value during iteration                  | `for idx, val in enumerate(my_list):`          | Prints index and value pairs                   |
| **List Unpacking**             | Assign multiple list elements to variables            | `a, b, *rest = [1, 2, 3, 4]`                   | `a=1, b=2, rest=[3,4]`                         |
| **Memory Considerations**      | Understanding list memory usage and efficiency        | Use `sys.getsizeof()` to check                 | Returns memory size in bytes                   |
| **Using `any()` and `all()`**  | Check conditions across list elements                 | `any(x > 5 for x in my_list)`                  | `True` or `False`                              |
| **List Flattening**            | Convert nested lists into a single list               | Using loops or itertools                       | Flattened single list                          |
| **Using `zip()` with Lists**   | Combine multiple lists element-wise                   | `list(zip(list1, list2))`                      | List of tuples                                 |
| **List Performance Tips**      | When to use lists vs other data structures            | For example, prefer sets for membership checks | *Advisory, no output*                          |


# Tuples

| **Topic**                    | **Description**                                            | **Example Code (line by line)**                                  | **Output**                                                   |
| ---------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------ |
| Creating tuples              | How to create tuples including empty and multiple values   | `t1 = ()`<br>`t2 = (1, 2, 3)`<br>`t3 = 4, 5, 6`                  | `()`<br>`(1, 2, 3)`<br>`(4, 5, 6)`                           |
| Single-element tuple         | Creating a tuple with only one element needs a comma       | `t = (7,)`<br>`print(type(t))`                                   | `<class 'tuple'>`                                            |
| Accessing elements           | Access tuple elements by index                             | `t = (10, 20, 30)`<br>`print(t[0])`                              | `10`                                                         |
| Negative indexing            | Access elements from the end                               | `print(t[-1])`                                                   | `30`                                                         |
| Slicing tuples               | Extract a portion of the tuple                             | `print(t[1:3])`                                                  | `(20, 30)`                                                   |
| Tuple unpacking              | Assign tuple elements to variables                         | `a, b, c = t`<br>`print(a, b, c)`                                | `10 20 30`                                                   |
| Ignoring values in unpacking | Use underscore to ignore certain elements during unpacking | `a, _, c = t`                                                    | *(No output unless printed)*                                 |
| Nested tuples                | Tuples inside tuples and accessing nested elements         | `nested = (1, (2, 3), 4)`<br>`print(nested[1][0])`               | `2`                                                          |
| Immutable nature             | Tuples cannot be changed after creation                    | `t[0] = 10  # Raises error`                                      | `TypeError: 'tuple' object does not support item assignment` |
| Tuple methods                | Use built-in methods like count and index                  | `t = (1, 2, 2, 3)`<br>`print(t.count(2))`<br>`print(t.index(3))` | `2`<br>`3`                                                   |
| Tuple concatenation          | Combine two tuples into one                                | `t1 = (1, 2)`<br>`t2 = (3, 4)`<br>`t3 = t1 + t2`                 | `(1, 2, 3, 4)`                                               |
| Repeating tuples             | Repeat the elements of a tuple multiple times              | `t = (1, 2) * 3`                                                 | `(1, 2, 1, 2, 1, 2)`                                         |
| Tuple length                 | Get the number of elements in a tuple                      | `print(len(t))`                                                  | `6`                                                          |
| Check element in tuple       | Check if an element exists in the tuple                    | `print(3 in t)`                                                  | `True`                                                       |
| Iterating over tuples        | Loop through tuple elements                                | `for item in t:`<br>`    print(item)`                            | Prints each element on a new line (e.g., 1\n2\n3)            |
| Tuple as dictionary key      | Tuples can be used as keys in dictionaries (immutable)     | `d = { (1, 2): "value" }`                                        | `{'(1, 2)': 'value'}` (dictionary created)                   |
| Tuple conversion             | Convert lists to tuples and vice versa                     | `list_t = list(t)`<br>`tuple_l = tuple([1, 2, 3])`               | List: `[1, 2, 3]`<br>Tuple: `(1, 2, 3)`                      |
| Tuple vs List differences    | Tuples are immutable; lists are mutable                    | (Explanation only - no code needed)                              | *(No output)*                                                |
| Using tuples in functions    | Pass tuples as arguments and return values                 | `def f(t):`<br>`    return t[0]`<br>`print(f((10, 20)))`         | `10`                                                         |
| Tuple with mixed data types  | Tuples can hold different data types                       | `t = (1, "hello", 3.14, True)`                                   | `(1, 'hello', 3.14, True)`                                   |

# Dictionary

| **Topic**                        | **Description**                                                                              | **Code Example**                                                                                                             | **Output**                                                 |
| -------------------------------- | -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| Dictionary Comprehension         | Create dictionaries using expressions in a concise way                                       | `squares = {x: x*x for x in range(1,6)}`<br>`print(squares)`                                                                 | `{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}`                         |
|                                  | Conditional comprehension                                                                    | `even_squares = {x: x*x for x in range(1,11) if x % 2 == 0}`<br>`print(even_squares)`                                        | `{2: 4, 4: 16, 6: 36, 8: 64, 10: 100}`                     |
| Dictionary Methods               | Common methods like `keys()`, `values()`, `items()`, `get()`, `pop()`, `update()`, `clear()` | `d = {'a':1, 'b':2}`<br>`print(d.keys())`<br>`print(d.get('a'))`<br>`d.update({'c':3})`<br>`print(d)`                        | `dict_keys(['a', 'b'])`<br>`1`<br>{'a': 1, 'b': 2, 'c': 3} |
| Dictionary Creation              | Different ways to create dictionaries                                                        | `d1 = {}`<br>`d2 = dict()`<br>`d3 = dict(a=1, b=2)`<br>`d4 = dict([('x',10), ('y',20)])`                                     | *(No output, dictionaries created)*                        |
| Dictionary Add/Append            | Add or update key-value pairs                                                                | `d = {}`<br>`d['key'] = 'value'`<br>`d.update({'new_key': 100})`<br>`print(d)`                                               | `{'key': 'value', 'new_key': 100}`                         |
| Dictionary Removal               | Remove keys using `pop()`, `popitem()`, `del`, `clear()`                                     | `d = {'a':1,'b':2}`<br>`d.pop('a')`<br>`del d['b']`<br>`d.clear()`<br>`print(d)`                                             | `{}`                                                       |
| Dictionary Access                | Access values by key, with or without default values                                         | `d = {'a':1}`<br>`print(d['a'])`<br>`print(d.get('b', 'Not Found'))`                                                         | `1`<br>`Not Found`                                         |
| Dictionary Conversion            | Convert dictionary keys, values or items to lists, sets, tuples                              | `d = {'a':1, 'b':2}`<br>`keys_list = list(d.keys())`<br>`values_set = set(d.values())`                                       | `['a', 'b']`<br>`{1, 2}`                                   |
| Dictionary with Lists            | Store lists as values or create dictionary from lists                                        | `d = {'nums': [1,2,3]}`<br>`print(d['nums'])`<br>`keys = ['a','b']`<br>`values = [10, 20]`<br>`d2 = dict(zip(keys, values))` | `[1, 2, 3]`<br>`{'a': 10, 'b': 20}`                        |
| Dictionary with String/Tuple/Set | Use strings, tuples or sets as keys or values                                                | `d = {('x', 'y'): 1}`<br>`print(d[('x','y')])`<br>`d2 = {frozenset([1,2]): 'set_key'}`                                       | `1`                                                        |
| Merge Dictionaries               | Combine dictionaries using `update()` or \` operator (Python 3.9+)                           | `d1 = {'a':1}`<br>`d2 = {'b':2}`<br>`d1.update(d2)`<br>`print(d1)`<br>`d3 = d1 \| d2`                                        | `{'a': 1, 'b': 2}`<br>`{'a': 1, 'b': 2}`                   |
| Nested Dictionaries              | Dictionaries inside dictionaries                                                             | `d = {'person': {'name': 'Alice', 'age': 25}}`<br>`print(d['person']['name'])`                                               | `Alice`                                                    |
| Check Key Existence              | Use `in` operator                                                                            | `d = {'a':1}`<br>`if 'a' in d:`<br>   `print('Key exists')`                                                                  | `Key exists`                                               |
| Iterate Over Dictionary          | Loop through keys, values, or items                                                          | `for k in d:`<br>   `print(k, d[k])`<br>`for k,v in d.items():`<br>   `print(k,v)`                                           | Prints key-value pairs                                     |
| Copy Dictionary                  | Copy dictionary with `copy()` or `dict()`                                                    | `d1 = {'a':1}`<br>`d2 = d1.copy()`<br>`print(d2)`                                                                            | `{'a': 1}`                                                 |
| Default Dictionary               | Use `collections.defaultdict` to avoid key errors                                            | `from collections import defaultdict`<br>`dd = defaultdict(int)`<br>`dd['x'] += 1`<br>`print(dd)`                            | `defaultdict(<class 'int'>, {'x': 1})`                     |

# Sets
| **Topic**                                | **Explanation**                                                                                    | **Example**                                                            | **Output**           |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | -------------------- |
| **What is a Set?**                       | A set is an unordered collection of unique elements.                                               | `my_set = {1, 2, 3} print(my_set)`                                     | {1, 2, 3}            |
| **Creating a Set**                       | Use `{}` with comma-separated values or `set()` function.                                          | `set1 = {1, 2, 3} set2 = set([4, 5, 6]) print(set1) print(set2)`       | {1, 2, 3} {4, 5, 6}  |
| **Empty Set**                            | `{}` creates an empty dict, so use `set()` for empty set.                                          | `empty = set() print(empty)`                                           | set()                |
| **Adding Elements**                      | Use `.add()` method to add one element.                                                            | `s = {1, 2} s.add(3) print(s)`                                         | {1, 2, 3}            |
| **Updating Set**                         | Use `.update()` to add multiple elements from iterable.                                            | `s = {1, 2} s.update([3, 4]) print(s)`                                 | {1, 2, 3, 4}         |
| **Removing Elements**                    | `.remove(elem)` removes elem, raises error if not found. `.discard(elem)` removes elem if present. | `s = {1, 2, 3} s.remove(2) print(s) s.discard(4) print(s)`             | {1, 3} {1, 3}        |
| **Set Operations: Union**                | Combines all unique elements from both sets.                                                       | `a = {1, 2} b = {2, 3} print(a.union(b))`                              | {1, 2, 3}            |
| **Set Operations: Intersection**         | Elements common to both sets.                                                                      | `a = {1, 2, 3} b = {2, 3, 4} print(a.intersection(b))`                 | {2, 3}               |
| **Set Operations: Difference**           | Elements in first set but not in second.                                                           | `a = {1, 2, 3} b = {2, 3} print(a.difference(b))`                      | {1}                  |
| **Set Operations: Symmetric Difference** | Elements in either set but not both.                                                               | `a = {1, 2, 3} b = {2, 3, 4} print(a.symmetric_difference(b))`         | {1, 4}               |
| **Subset and Superset**                  | `.issubset()` checks if all elements of one set are in another. `.issuperset()` is reverse.        | `a = {1, 2} b = {1, 2, 3} print(a.issubset(b)) print(b.issuperset(a))` | True True            |
| **Set Comprehension**                    | Create sets with comprehensions like lists.                                                        | `squares = {x*x for x in range(5)} print(squares)`                     | {0, 1, 4, 9, 16}     |
| **Frozen Set**                           | Immutable version of set, cannot add or remove elements.                                           | `f = frozenset([1, 2, 3]) print(f)`                                    | frozenset({1, 2, 3}) |
| **Iterating Over Set**                   | Loop through elements in any order.                                                                | `s = {1, 2, 3} for elem in s: print(elem)`                             | 1 2 3 (in any order) |
| **Length of Set**                        | Use `len()` to get the number of elements.                                                         | `s = {1, 2, 3} print(len(s))`                                          | 3                    |
| **Check Membership**                     | Use `in` keyword to check if element is in set.                                                    | `s = {1, 2, 3} print(2 in s) print(5 in s)`                            | True False           |

# Array

| Topic                                                | Explanation & Code Example                                                                                                                                              | Output                                                            |
| ---------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| Declaring an Array in Python                         | Python has `array` module for typed arrays. Example: `import array as arr a = arr.array('i', [1, 2, 3]) print(a)`                                                       | array('i', \[1, 2, 3])                                            |
| Difference between Array and List in Python          | Arrays are typed, lists are heterogeneous and more flexible. Example: `import array as arr a = arr.array('i', [1,2]) l = [1, 'two', 3.0] print(type(a)) print(type(l))` | `<class 'array.array'>` `<class 'list'>`                          |
| Python Array length                                  | Use `len()` function. Example: `import array as arr a = arr.array('i', [10,20,30]) print(len(a))`                                                                       | 3                                                                 |
| Numpy Arrays                                         | Powerful numeric arrays with more features. Example: `import numpy as np a = np.array([1,2,3]) print(a) print(type(a))`                                                 | `[1 2 3]` `<class 'numpy.ndarray'>`                               |
| Python Unpack Array                                  | Unpack elements to variables. Example: `import array as arr a = arr.array('i', [5,10,15]) x, y, z = a print(x) print(y) print(z)`                                       | 5 10 15                                                           |
| Python remove Array item                             | Use `remove()` or `pop()`. Example: `import array as arr a = arr.array('i', [1,2,3,2]) a.remove(2) print(a) a.pop(1) print(a)`                                          | array('i', \[1, 3, 2]) array('i', \[1, 2])                        |
| How to add element to Array in Python                | Use `append()` or `insert()`. Example: `import array as arr a = arr.array('i', [1,2,3]) a.append(4) print(a) a.insert(1, 5) print(a)`                                   | array('i', \[1, 2, 3, 4]) array('i', \[1, 5, 2, 3, 4])            |
| Find element in Array in Python                      | Use `in` keyword. Example: `import array as arr a = arr.array('i', [1,2,3]) print(2 in a) print(5 in a)`                                                                | True False                                                        |
| Find Common elements in two Arrays in Python         | Convert to sets and intersect. Example: `import array as arr a = arr.array('i', [1,2,3]) b = arr.array('i', [2,3,4]) common = set(a).intersection(b) print(common)`     | {2, 3}                                                            |
| How to pass an Array to a Function in Python         | Pass as parameter normally. Example: `import array as arr def print_array(ar): for i in ar: print(i) a = arr.array('i', [1,2,3]) print_array(a)`                        | 1 2 3                                                             |
| How to create String Array in Python                 | Use lists for strings. Example: `str_array = ["apple", "banana", "cherry"] print(str_array)`                                                                            | \['apple', 'banana', 'cherry']                                    |
| Multidimensional Arrays                              | Use nested lists or numpy. Example numpy: `import numpy as np a = np.array([[1,2],[3,4]]) print(a)`                                                                     | `[[1 2] [3 4]]`                                                   |
| Array Slicing                                        | Extract parts of array. Example: `import array as arr a = arr.array('i', [10,20,30,40]) print(a[1:3])`                                                                  | array('i', \[20, 30])                                             |
| Array Iteration                                      | Loop over elements. Example: `import array as arr a = arr.array('i', [1,2,3]) for i in a: print(i)`                                                                     | 1 2 3                                                             |
| Array Concatenation                                  | Combine arrays. Example: `import array as arr a = arr.array('i', [1,2]) b = arr.array('i', [3,4]) c = arr.array('i', a + b) print(c)`                                   | array('i', \[1, 2, 3, 4])                                         |
| Array Sorting                                        | Sort elements in place. Example: `import array as arr a = arr.array('i', [3,1,2]) a = arr.array('i', sorted(a)) print(a)`                                               | array('i', \[1, 2, 3])                                            |
| Array Copying                                        | Use slicing or `copy` module. Example: `import array as arr import copy a = arr.array('i', [1,2,3]) b = a[:] c = copy.deepcopy(a)`                                      | No visible output, but `b` and `c` are independent copies of `a`. |
| Memory Usage of Arrays vs Lists                      | Arrays use less memory as they store homogeneous data, lists are flexible but use more memory (no direct code example).                                                 | *No output (conceptual explanation)*                              |
| Array Broadcasting (Numpy specific)                  | Numpy allows operations on different shapes. Example: `import numpy as np a = np.array([1,2,3]) b = 5 print(a + b)`                                                     | `[6 7 8]`                                                         |
| Array Reshaping (Numpy specific)                     | Change shape without changing data. Example: `import numpy as np a = np.array([1,2,3,4,5,6]) b = a.reshape(2,3) print(b)`                                               | `[[1 2 3] [4 5 6]]`                                               |
| Array Data Types and Typecodes (array module)        | `'i'` for int, `'f'` for float etc. Example: `import array as arr a = arr.array('f', [1.0, 2.0, 3.0]) print(a)`                                                         | array('f', \[1.0, 2.0, 3.0])                                      |
| Performance Comparison: Array vs List vs Numpy Array | Numpy arrays are fastest for numeric computations, arrays (`array` module) save memory vs lists but less flexible.                                                      | *No output (conceptual comparison)*                               |
| Using List Comprehensions to Create Arrays           | Create arrays/lists concisely. Example: `squares = [x*x for x in range(5)] print(squares)`                                                                              | \[0, 1, 4, 9, 16]                                                 |
| Array Filtering                                      | Extract elements meeting condition. Example: `a = [1,2,3,4,5] filtered = [x for x in a if x > 2] print(filtered)`                                                       | \[3, 4, 5]                                                        |
| Handling Empty Arrays                                | Initialize empty arrays. Example: `import array as arr a = arr.array('i', []) print(a)`                                                                                 | array('i')                                                        |
| Error Handling with Arrays                           | Catch errors like `IndexError`. Example: `import array as arr a = arr.array('i', [1,2]) try: print(a[3]) except IndexError: print("Index out of range")`                | Index out of range                                                |


# List Comprehension

| **Topic**                     | **Explanation**                                  | **Example**                                                                                             | **Output**                                 |
| ----------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| **Basic Syntax**              | Short way to create a new list from an iterable. | `numbers = [1, 2, 3, 4, 5] square = [x * x for x in numbers] print(square)`                             | \[1, 4, 9, 16, 25]                         |
| **With Condition (if)**       | Include condition to filter elements.            | `numbers = [1, 2, 3, 4, 5] even = [x for x in numbers if x % 2 == 0] print(even)`                       | \[2, 4]                                    |
| **With if-else**              | Apply transformation based on condition.         | `nums = [1, 2, 3, 4, 5] labels = ['Even' if x % 2 == 0 else 'Odd' for x in nums] print(labels)`         | \['Odd', 'Even', 'Odd', 'Even', 'Odd']     |
| **Nested List Comprehension** | For 2D lists or matrix operations.               | `matrix = [[1, 2], [3, 4]] flat = [num for row in matrix for num in row] print(flat)`                   | \[1, 2, 3, 4]                              |
| **Multiple if Conditions**    | Filter with multiple conditions.                 | `nums = [1, 2, 3, 4, 5, 6] filtered = [x for x in nums if x > 2 if x < 6] print(filtered)`              | \[3, 4, 5]                                 |
| **Using Functions**           | Call functions inside list comprehension.        | `def square(x): return x * x nums = [1, 2, 3] squares = [square(n) for n in nums] print(squares)`       | \[1, 4, 9]                                 |
| **With Strings**              | List comprehension on strings.                   | `text = "hello" chars = [c.upper() for c in text] print(chars)`                                         | \['H', 'E', 'L', 'L', 'O']                 |
| **Flatten Nested List**       | Useful for converting 2D to 1D.                  | `nested = [[1, 2], [3, 4], [5, 6]] flat = [item for sublist in nested for item in sublist] print(flat)` | \[1, 2, 3, 4, 5, 6]                        |
| **List of Tuples**            | Create tuples directly.                          | `result = [(x, x**2) for x in range(5)] print(result)`                                                  | \[(0, 0), (1, 1), (2, 4), (3, 9), (4, 16)] |
| **Using enumerate()**         | Get index and value.                             | `names = ['Alice', 'Bob'] indexed = [f'{i}-{name}' for i, name in enumerate(names)] print(indexed)`     | \['0-Alice', '1-Bob']                      |
| **Set Comprehension**         | Same as list comp but with `{}`                  | `nums = [1, 2, 2, 3] unique = {x for x in nums} print(unique)`                                          | {1, 2, 3}                                  |
| **Dict Comprehension**        | Create dictionaries using comprehension.         | `keys = ['a', 'b'] vals = [1, 2] mydict = {k: v for k, v in zip(keys, vals)} print(mydict)`             | {'a': 1, 'b': 2}                           |
| **Using range()**             | Common with numbers.                             | `squares = [x * x for x in range(5)] print(squares)`                                                    | \[0, 1, 4, 9, 16]                          |
| **With multiple loops**       | Use nested loops in one line.                    | `pairs = [(x, y) for x in [1, 2] for y in [3, 4]] print(pairs)`                                         | \[(1, 3), (1, 4), (2, 3), (2, 4)]          |
| **Filter None or Empty**      | Clean up data.                                   | `data = ['a', '', None, 'b'] cleaned = [d for d in data if d] print(cleaned)`                           | \['a', 'b']                                |
| **Conditional Replace**       | Replace specific values.                         | `nums = [0, 1, 2, 0, 3] replaced = [x if x != 0 else -1 for x in nums] print(replaced)`                 | \[-1, 1, 2, -1, 3]                         |


# Frozenset

| Topic                                         | Description                                                  | Example Code                                                                                   | Output                                             |
| --------------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| **1. Creating a frozenset**                   | Convert iterable (list, tuple, set, string) into a frozenset | `fs = frozenset([1, 2, 3, 2])`<br>`print(fs)`                                                  | `frozenset({1, 2, 3})`                             |
| **2. Empty frozenset**                        | Create an empty frozenset                                    | `empty_fs = frozenset()`<br>`print(empty_fs)`                                                  | `frozenset()`                                      |
| **3. From string**                            | Each character becomes an element                            | `fs = frozenset("abcabc")`<br>`print(fs)`                                                      | `frozenset({'c', 'a', 'b'})`                       |
| **4. Set vs Frozenset**                       | Set is mutable, frozenset is immutable                       | `s = set([1, 2])`<br>`fs = frozenset([1, 2])`<br>`s.add(3)`<br>`# fs.add(3)` ← Error           | `s = {1, 2, 3}`<br>`# AttributeError for fs.add()` |
| **5. Membership testing**                     | Check if item exists                                         | `fs = frozenset([1, 2, 3])`<br>`print(2 in fs)`<br>`print(5 in fs)`                            | `True`<br>`False`                                  |
| **6. Iterating**                              | Use a loop to access elements                                | `fs = frozenset([10, 20, 30])`<br>`for i in fs:`<br>`    print(i)`                             | `10`<br>`20`<br>`30` (order may vary)              |
| **7. Length**                                 | Use `len()` function                                         | `fs = frozenset([1, 2, 3])`<br>`print(len(fs))`                                                | `3`                                                |
| **8. Set operations - Union**                 | Combine elements                                             | `a = frozenset([1, 2])`<br>`b = frozenset([2, 3])`<br>`print(a.union(b))`                      | `frozenset({1, 2, 3})`                             |
| **9. Set operations - Intersection**          | Common elements                                              | `a = frozenset([1, 2, 3])`<br>`b = frozenset([2, 3, 4])`<br>`print(a.intersection(b))`         | `frozenset({2, 3})`                                |
| **10. Set operations - Difference**           | Items in one not in the other                                | `a = frozenset([1, 2, 3])`<br>`b = frozenset([3, 4])`<br>`print(a.difference(b))`              | `frozenset({1, 2})`                                |
| **11. Set operations - Symmetric Difference** | Items in either but not both                                 | `a = frozenset([1, 2, 3])`<br>`b = frozenset([2, 3, 4])`<br>`print(a.symmetric_difference(b))` | `frozenset({1, 4})`                                |
| **12. Subset check**                          | Check if A is subset of B                                    | `a = frozenset([1, 2])`<br>`b = frozenset([1, 2, 3])`<br>`print(a.issubset(b))`                | `True`                                             |
| **13. Superset check**                        | Check if A is superset of B                                  | `a = frozenset([1, 2, 3])`<br>`b = frozenset([2])`<br>`print(a.issuperset(b))`                 | `True`                                             |
| **14. Disjoint check**                        | No common elements                                           | `a = frozenset([1, 2])`<br>`b = frozenset([3, 4])`<br>`print(a.isdisjoint(b))`                 | `True`                                             |
| **15. Hashable nature**                       | Can be used as dict key                                      | `d = {frozenset([1, 2]): "value"}`<br>`print(d)`                                               | `{frozenset({1, 2}): 'value'}`                     |
| **16. Immutable proof**                       | Cannot modify                                                | `fs = frozenset([1, 2])`<br>`# fs.add(3)`<br>`# fs.remove(2)`                                  | `AttributeError` for both                          |

# Exception Handling
| **Topic**                                            | **Description**                                                                               | **Example**                                                                                                                                               | **Example Output**                                                                             |
| ---------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **1. What is Exception?**                            | Exceptions are errors detected during execution. Python uses try-except blocks to catch them. | `python try:   a = 10 / 0 except ZeroDivisionError:   print("Cannot divide by zero") `                                                                    | Cannot divide by zero                                                                          |
| **2. Try and Except Block**                          | Wraps code that may raise an error in `try` and handles it in `except`.                       | `python try:   x = int("hello") except ValueError:   print("Invalid conversion") `                                                                        | Invalid conversion                                                                             |
| **3. Catching Specific Exception**                   | You can handle specific exceptions like `ZeroDivisionError`, `ValueError`.                    | `python try:   a = 5 / 0 except ZeroDivisionError:   print("Zero division occurred") `                                                                    | Zero division occurred                                                                         |
| **4. Catching Multiple Exceptions**                  | Handle multiple exceptions using multiple `except` blocks.                                    | `python try:   a = int("abc")   b = 5 / 0 except ValueError:   print("ValueError caught") except ZeroDivisionError:   print("ZeroDivisionError caught") ` | ValueError caught                                                                              |
| **5. Catching Multiple Exceptions in Single Except** | Use a tuple to catch multiple exceptions in one `except`.                                     | `python try:   a = int("abc") except (ValueError, TypeError):   print("Caught ValueError or TypeError") `                                                 | Caught ValueError or TypeError                                                                 |
| **6. Using Else Clause**                             | `else` runs if no exception occurs.                                                           | `python try:   a = 10   print("No error") except:   print("Error") else:   print("Executed successfully") `                                               | No error  Executed successfully                                                                |
| **7. Finally Block**                                 | `finally` always executes regardless of exception.                                            | `python try:   a = 10 / 0 except ZeroDivisionError:   print("Caught an error") finally:   print("Cleanup code") `                                         | Caught an error  Cleanup code                                                                  |
| **8. Raising Exceptions**                            | Use `raise` to throw exceptions manually.                                                     | `python age = -5 if age < 0:   raise ValueError("Age can't be negative") `                                                                                | ValueError: Age can't be negative                                                              |
| **9. Custom Exception Class**                        | You can define your own exception types.                                                      | `python class MyError(Exception):   pass try:   raise MyError("Custom error") except MyError as e:   print(e) `                                           | Custom error                                                                                   |
| **10. Try with Multiple Except, Else, Finally**      | Combine `try`, multiple `except`, `else`, and `finally`.                                      | `python try:   a = int(input("Enter a number: ")) except ValueError:   print("Invalid input") else:   print("Valid number") finally:   print("Done") `    | (Input dependent)                                                                              |
| **11. Nested Try Block**                             | You can use a try block inside another try.                                                   | `python try:   try:     a = 10 / 0   except ZeroDivisionError:     print("Inner exception") except:   print("Outer exception") `                          | Inner exception                                                                                |
| **12. Exception with Arguments**                     | You can pass custom messages to exceptions.                                                   | `python try:   raise Exception("Something went wrong") except Exception as e:   print("Error:", e) `                                                      | Error: Something went wrong                                                                    |
| **13. Accessing Exception Details**                  | Exception details can be accessed via the object.                                             | `python try:   x = int("abc") except ValueError as e:   print("Exception type:", type(e))   print("Message:", e) `                                        | Exception type: `<class 'ValueError'>`  Message: invalid literal for int() with base 10: 'abc' |
| **14. Re-raising Exception**                         | Use `raise` without arguments to re-raise a caught exception.                                 | `python try:   try:     a = 1 / 0   except ZeroDivisionError:     print("Handled here")     raise except:   print("Re-raised and caught again") `         | Handled here  Re-raised and caught again                                                       |
| **15. Assertions and Exceptions**                    | `assert` raises `AssertionError` if condition is False.                                       | `python x = -1 assert x >= 0, "Negative not allowed" `                                                                                                    | AssertionError: Negative not allowed                                                           |

### Built-in Exception

| Topic                | Description                                                                                  | Example                                                                                                                   | Example Output                                                         |
| -------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `IndexError`         | Raised when trying to access an index that is out of range in a sequence (list, tuple, etc). | `python\nlst = [1, 2, 3]\nprint(lst[5])  # Accessing index 5 which does not exist\n`                                      | `IndexError: list index out of range`                                  |
| `KeyError`           | Raised when a dictionary key is not found.                                                   | `python\nd = {'a': 1, 'b': 2}\nprint(d['c'])  # 'c' key doesn't exist\n`                                                  | `KeyError: 'c'`                                                        |
| `TypeError`          | Raised when an operation or function is applied to an object of inappropriate type.          | `python\nresult = '2' + 2  # Cannot add string and int directly\n`                                                        | `TypeError: can only concatenate str (not "int") to str`               |
| `ValueError`         | Raised when a function receives an argument of correct type but inappropriate value.         | `python\nint('abc')  # Cannot convert 'abc' string to int\n`                                                              | `ValueError: invalid literal for int() with base 10: 'abc'`            |
| `ZeroDivisionError`  | Raised when division or modulo by zero occurs.                                               | `python\nx = 10 / 0  # Division by zero\n`                                                                                | `ZeroDivisionError: division by zero`                                  |
| `AttributeError`     | Raised when attribute reference or assignment fails.                                         | `python\nx = 10\nx.append(5)  # int object has no 'append' method\n`                                                      | `AttributeError: 'int' object has no attribute 'append'`               |
| `ImportError`        | Raised when import statement fails to find the module or name.                               | `python\nimport non_existent_module  # Module not found\n`                                                                | `ModuleNotFoundError: No module named 'non_existent_module'`           |
| `NameError`          | Raised when a local or global name is not found.                                             | `python\nprint(my_var)  # 'my_var' is not defined\n`                                                                      | `NameError: name 'my_var' is not defined`                              |
| `StopIteration`      | Raised to signal that an iterator has no more items.                                         | `python\nit = iter([1, 2])\nprint(next(it))\nprint(next(it))\nprint(next(it))  # Third next() causes error\n`             | `StopIteration`                                                        |
| `FileNotFoundError`  | Raised when a file or directory is requested but doesn’t exist.                              | `python\nopen('nofile.txt')  # File doesn't exist\n`                                                                      | `FileNotFoundError: [Errno 2] No such file or directory: 'nofile.txt'` |
| `IndentationError`   | Raised when there is an incorrect indentation.                                               | `python\ndef foo():\nprint("Hi")  # Missing indentation on print\n`                                                       | `IndentationError: expected an indented block`                         |
| `RuntimeError`       | Raised when an error is detected that doesn’t fall in any other category.                    | `python\ndef foo():\n    raise RuntimeError("Something went wrong")\nfoo()\n`                                             | `RuntimeError: Something went wrong`                                   |
| `OverflowError`      | Raised when the result of an arithmetic operation is too large to be represented.            | `python\nimport math\nmath.exp(1000)  # Very large exponentiation\n`                                                      | `OverflowError: math range error`                                      |
| `MemoryError`        | Raised when an operation runs out of memory.                                                 | `python\n# Trying to create a huge list that won't fit in memory\nx = [1] * (10**10)  # May raise MemoryError\n`          | `MemoryError` (if system runs out of memory)                           |
| `SyntaxError`        | Raised when the parser encounters a syntax error.                                            | `python\nexec('if True print("Hi")')  # Missing colon\n`                                                                  | `SyntaxError: invalid syntax`                                          |
| `IndentationError`   | Raised for incorrect indentation in code.                                                    | `python\ndef test():\nprint("Hello")  # No indentation inside function\n`                                                 | `IndentationError: expected an indented block`                         |
| `KeyboardInterrupt`  | Raised when the user hits the interrupt key (Ctrl+C).                                        | `python\nimport time\ntry:\n    time.sleep(10)\nexcept KeyboardInterrupt:\n    print("Interrupted!")\n`                   | `Interrupted!` (if user presses Ctrl+C)                                |
| `FloatingPointError` | Raised when a floating point operation fails.                                                | `python\nimport math\nmath.sqrt(-1)  # Will raise ValueError normally, but FloatingPointError possible in some configs\n` | (Usually `ValueError` for sqrt(-1))                                    |
| `AssertionError`     | Raised when an assert statement fails.                                                       | `python\nassert 2 + 2 == 5, "Math is broken!"  # Assertion fails\n`                                                       | `AssertionError: Math is broken!`                                      |
| `EOFError`           | Raised when input() hits end-of-file condition without reading any data.                     | `python\ninput()  # Ctrl+D on Unix or Ctrl+Z on Windows causes EOFError\n`                                                | `EOFError: EOF when reading a line`                                    |

### User defined Exception

| Topic                                      | Description                                                                                           | Example                                                                                                                                                                                                                                                                             | Example Output                  |
| ------------------------------------------ | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| What are User Defined Exceptions?          | Custom exceptions created by users to handle specific errors not covered by built-in exceptions.      | `python class MyError(Exception): pass try: raise MyError("Custom error occurred") except MyError as e: print(e) `                                                                                                                                                                  | Custom error occurred           |
| How to define a User Defined Exception     | Inherit from the base `Exception` class and optionally add custom methods or attributes.              | `python class MyError(Exception): def __init__(self, message): self.message = message def __str__(self): return self.message try: raise MyError("Error raised!") except MyError as e: print(e) `                                                                                    | Error raised!                   |
| Raising a User Defined Exception           | Use the `raise` keyword followed by an instance of the custom exception class to throw the exception. | `python class NegativeValueError(Exception): pass def check_value(x): if x < 0: raise NegativeValueError("Negative value!") try: check_value(-5) except NegativeValueError as e: print(e) `                                                                                         | Negative value!                 |
| Catching a User Defined Exception          | Use a `try-except` block to catch the specific user defined exception and handle it gracefully.       | `python class MyException(Exception): pass try: raise MyException("Something went wrong") except MyException as e: print("Caught:", e) `                                                                                                                                            | Caught: Something went wrong    |
| Adding Custom Attributes to Exception      | User exceptions can have additional attributes to store more error information.                       | `python class ValidationError(Exception): def __init__(self, message, code): self.message = message self.code = code def __str__(self): return f"{self.message} (Error code: {self.code})" try: raise ValidationError("Invalid input", 400) except ValidationError as e: print(e) ` | Invalid input (Error code: 400) |
| Using User Defined Exceptions in Functions | Functions can raise user exceptions to signal errors to the caller.                                   | `python class InputError(Exception): pass def process_input(val): if not isinstance(val, int): raise InputError("Expected integer") try: process_input("abc") except InputError as e: print("Error:", e) `                                                                          | Error: Expected integer         |
| Best Practices for User Defined Exceptions | Name exceptions ending with `Error` and inherit from `Exception` or its subclasses for clarity.       | `python class FileFormatError(Exception): pass # Raise when file format is wrong `                                                                                                                                                                                                  | (No output unless raised)       |

# File Handling

| Topic                                         | Description                                                                              | Example                                                                                            | Example Output                        |
| --------------------------------------------- | ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------- |
| **File Handling Basics**                      | Opening, closing, reading, writing files using built-in `open()` function                | `f = open("file.txt", "r")`<br>`content = f.read()`<br>`f.close()`                                 | (Content of file.txt printed)         |
| **File Modes**                                | Modes like "r" (read), "w" (write), "a" (append), "x" (create), "b" (binary), "t" (text) | `open("file.txt", "w")` # write mode creates or overwrites                                         | Creates or overwrites file.txt        |
| **Reading Files - read()**                    | Reads whole file content as string                                                       | `with open("file.txt") as f:`<br>`  data = f.read()`                                               | Entire file content                   |
| **Reading Files - readline()**                | Reads one line at a time from a file                                                     | `with open("file.txt") as f:`<br>`  line = f.readline()`                                           | One line from file                    |
| **Reading Files - readlines()**               | Reads all lines into a list                                                              | `with open("file.txt") as f:`<br>`  lines = f.readlines()`                                         | List of all lines                     |
| **Writing Files - write()**                   | Write string data to a file                                                              | `with open("file.txt", "w") as f:`<br>`  f.write("Hello world")`                                   | File content: Hello world             |
| **Writing Files - writelines()**              | Write list of strings to a file                                                          | `lines = ["First\n", "Second\n"]`<br>`with open("file.txt", "w") as f:`<br>`  f.writelines(lines)` | File with two lines                   |
| **Appending to Files**                        | Add content to end of file using mode "a"                                                | `with open("file.txt", "a") as f:`<br>`  f.write("Appended line\n")`                               | Content appended at end               |
| **Creating Files - mode 'x'**                 | Create file, raise error if file exists                                                  | `f = open("newfile.txt", "x")`                                                                     | New file created or FileExistsError   |
| **File Context Manager**                      | Use `with` statement for auto closing files                                              | `with open("file.txt") as f:`<br>`  data = f.read()`                                               | File auto-closed after block          |
| **os Module - File Info**                     | Get file properties (size, permissions, etc.)                                            | `import os`<br>`print(os.path.getsize("file.txt"))`                                                | File size in bytes                    |
| **os Module - Rename File**                   | Rename or move a file                                                                    | `os.rename("old.txt", "new.txt")`                                                                  | File renamed                          |
| **os Module - Remove File**                   | Delete a file                                                                            | `os.remove("file.txt")`                                                                            | File deleted                          |
| **os Module - List Directory**                | List files and folders inside a directory                                                | `print(os.listdir("."))`                                                                           | List of current directory files       |
| **os Module - Current Directory**             | Get or change current working directory                                                  | `print(os.getcwd())`<br>`os.chdir("/path/to/dir")`                                                 | Shows path or changes working dir     |
| **pathlib Module - Path Object**              | Object-oriented file system paths handling                                               | `from pathlib import Path`<br>`p = Path("file.txt")`                                               | Path object representing file.txt     |
| **pathlib - Check Exists**                    | Check if path/file exists                                                                | `p.exists()`                                                                                       | True or False                         |
| **pathlib - Read Text**                       | Read entire file content as string                                                       | `p.read_text()`                                                                                    | File content as string                |
| **pathlib - Write Text**                      | Write string content to file                                                             | `p.write_text("Hello pathlib!")`                                                                   | Writes content to file                |
| **Directory Management - Make Dir**           | Create new directory                                                                     | `os.mkdir("newdir")`                                                                               | Directory created                     |
| **Directory Management - Remove Dir**         | Delete directory (must be empty)                                                         | `os.rmdir("newdir")`                                                                               | Directory removed                     |
| **Directory Management - Recursive Make Dir** | Create directory recursively including parents                                           | `os.makedirs("parent/child")`                                                                      | Nested directories created            |
| **Directory Management - Walk Directory**     | Iterate through directory tree                                                           | `for root, dirs, files in os.walk("."):`<br>`  print(root, dirs, files)`                           | Prints all dirs and files recursively |
