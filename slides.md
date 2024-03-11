---
# try also 'default' to start simple
theme: ./theme
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: https://cover.sli.dev
# some information about your slides, markdown enabled
title: "Crash course: Data Science with Python and R - Python (Part 1)"
# info: |
#   ## Slidev Starter Template
#   Presentation slides for developers.

#   Learn more at [Sli.dev](https://sli.dev)
# apply any unocss classes to the current slide
# class: text-center
# https://sli.dev/custom/highlighters.html
# highlighter: shiki
# https://sli.dev/guide/drawing
# drawings:
#   persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: fade-in
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
layout: quote
---

# Crash course: Data Science with Python and R

<style>
h1 {color: #0065BD}
</style>

Python (Part 1)

<span style="color: #888888;">Adapted from Dr. Raoul Rothfeld's slides</span>

<div class="pt-12">
Cheng Lyu & Dr. Mohamed Abouelela<br>
Technical University of Munich<br>
TUM School of Engineering and Design<br>
Chair of Transportation Systems Engineering<br>
Munich, 11.03.2024
</div>

<img src="/assets/tum-sketch.png" width="350" class="fixed bottom-10 right-10 -z-10" />

<TumLogo />
<TumBarBottom />

<!--
Welcome
-->

---
layout: default
---

# Course Overview

## Lecture time and format:
- Monday to Thursday from 10:00 to 12:00 (CET) via Zoom (video web conference)
- After each lecture, a recording of the lecture will be available on-demand via Moodle
- For communication, we use Zoom, Moodle, and GitLab (all are TUM services)
- Interactive lecture with integrated exercises

## Objectives:
- Assuming that many students have never programmed, provide basic programming understanding and functional coding ability (in contrast to object-oriented programming and software engineering)
- Enable simple data analytics and visualizations, and provide a basis for further self-learning

<TumLogo />
<TumBarBottom />



---
layout: image
image: /images/top-programming-languages-2023.webp
backgroundSize: contain
---

# 


---
layout: image-caption
name: "Popularity of Programming Languages"
image: /images/top-programming-languages-2023.webp
imageCaption: "Source: <a href='https://octoverse.github.com/'>GitHub Octoverse</a>"
---


Some language categories:
- General-purpose (e.g. **Python**, Java, C#)
- Statistical/mathematical (e.g. **R**, Matlab, SAS)
- Web-functionality (e.g. JavaScript, PHP, Ruby)
- Lower-level (e.g. C++, C, Assembly)
- ...

<TumLogo />
<TumBarBottom />



---
layout: default
---

# Where is <span class="pretty-title">Python</span> mostly used?

- **Data Analysis**: Data wrangling, data visualization
- **Scientific Computing**: Numerical simulations, optimization
- **Artificial Intelligence & Machine Learning**: Predictive models, neural networks
- **Automation & Scripting**: Task automation, system administration
- Web Development: Web frameworks, web apps
- Desktop Applications: Cross-platform GUIs
- Game Development: Game engines, indie games


<TumLogo />
<TumBarBottom />


<style>
.pretty-title {
  font-weight: 800;
  background-color: #2B90B6;
  background-image: linear-gradient(130deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>





---
layout: default
---

# Necessary Tools for the Course

An installation guide can be found on the Moodle page of the course.

Tools that you will need to have installed:

- Python (programming language): https://www.python.org/downloads/
- Anaconda (environment manager): https://www.anaconda.com/products/distribution 
- Visual Studio Code (code editor): https://code.visualstudio.com 
- Git (code versioning, optional): https://git-scm.com/downloads 

<div style="display: flex; justify-content: center; align-items: center">
  <img src="/images/tools-python.png" alt="Python" style="height: 170px; padding: 20px;" />
  <img src="/images/tools-conda.png" alt="Anaconda" style="height: 170px; padding: 20px;" />
  <img src="/images/tools-git.png" alt="Git" style="height: 170px; padding: 20px;" />
</div>

<TumLogo />
<TumBarBottom />



---

# Terminal, GUI, IDE and Code Editor

<v-clicks>

- <simple-icons-gnometerminal class="text-gray-600"/> Terminal/console: text-based interfaces for human-computer interaction (HCI).
- <carbon-gui /> Graphical user interface (GUI): visual interfaces for HCI that allow point-and-click interaction.
- <simple-icons-intellijidea class="text-gray-600"/> Integrated development environment (IDE): GUIs that combine all tools to write, test, and execute programmes.
- <simple-icons-visualstudiocode class="text-gray-600"/> Code editor: a simpler version of an IDE, with fewer features, but faster and more lightweight.
</v-clicks>

<div style="display: flex; justify-content: center; align-items: center;">
  <span v-click="1"><img src="/images/soft-terminal.png" alt="Python" style="width: auto; height: 150px; padding: 5px;" /></span>
  <span v-click="2"><img src="/images/soft-gui.png" alt="Anaconda" style="width: auto; height: 150px; padding: 5px;" /></span>
  <span v-click="3"><img src="/images/soft-ide.png" alt="Git" style="width: auto; height: 150px; padding: 5px;" /></span>
  <span v-click="4"><img src="/images/soft-editor.png" alt="Git" style="width: auto; height: 150px; padding: 5px;" /></span>
</div>

<TumLogo />
<TumBarBottom />


---
layout: image-caption
name: "Terminal, GUI, IDE and Code Editor"
image: /images/soft-spyder.png
imageCaption: "Spyder"
---

**Integrated development environment (IDE)**: GUIs that combine all tools to write, test, and execute programmes. Most IDEs are language- and purpose-specific, e.g.:
- *Spyder*: (open-source) data science for Python
- *PyCharm*: (commercial) general-purpose/software development for Python
- *DataSpell*: (commercial) data science with Jupyter notebooks of Python

<TumLogo />
<TumBarBottom />


---
layout: image-caption
name: "Terminal, GUI, IDE and Code Editor"
image: /images/soft-editor.png
imageCaption: "Visual Studio Code"
---

**Code Editor**: GUIs similar to IDEs that combine all tools to write, test, and execute programmes. Compared with IDEs, editors are not language- and purpose-specific, allowing users to work on multiple tasks simultaneously.
- *Visual Studio Code*: (open-source) 
- *Atom*: (open-source) 
- *Sublime Text*: (commercial) 

<TumLogo />
<TumBarBottom />








---

# First Line in Python

- Open the **terminal** (e.g. Command Prompt, PowerShell, Terminal).
- Launch the **Python interpreter** by typing `python` and pressing <kbd>Enter</kbd>.

```bash
python
```

- Now we are in the <span v-mark.highlight.yellow>interactive Python interpreter</span>.
- **Greet the world** with a simple line of code!
- Press <kbd>Enter</kbd> to execute the code.

```python
print("Hello world!")
```

- Strings in Python are enclosed in either single or double quotes.
- Want to **get out of the Python interpreter**?

```python
exit()
```

<TumLogo />
<TumBarBottom />



---

# First Line in Python

The interactive Python interpreter can also accept input from the user.

- Launch the **Python interpreter**.
- Use the `input()` function to prompt the user for input.
 
```python
name = input("What is your name? ")
print("Hello,", name)
```

- The `input()` function returns a _string_.
- The `print()` function can take multiple arguments, separated by commas.


<TumLogo />
<TumBarBottom />




---

# Basic Arithmetic Operations

- Launch the **Python interpreter**.
- Simple arithmetic operations, including addition, subtraction, multiplication, and division, can be directly performed in the Python interpreter.
- The answer will be displayed immediately after pressing <kbd>Enter</kbd> in the interactive interpreter.

```python
2 + 3
```

- Compound operations can also be performed in a natural way.
```python
5 - 2 * 3 + 8 / (2 - 1)
```

- **Exponentiation**, **modulo**, and **integer division** are also supported.
```python
2**3, 10 % 3, 10 // 3
```

<TumLogo />
<TumBarBottom />



---
preload: true
---

# Variables

**Variables** are used to store data.

- In Python, variables are created when a value is **assigned** to them.
```python
name = "Alice"
length = 123456789
radius = 12.5
```

- The variable name can contain letters, numbers, and underscores, but cannot start with a number.
- Variable names are **case-sensitive**, and should NOT be the same as **Python keywords**.
   - `name`, `Name123`,`__name__`, `__Name__`, `__123Name`,
   - <span v-mark.cross.red>`123Name`, `name@123`, `Name-123`, `and`, `def`</span>
- The value of a variable can be changed at any time.

```python
name = "Bob"
length = length + 100
radius *= 2
```

<TumLogo />
<TumBarBottom />




---

# Variables

- There is no constant in Python, but by convention, variable names in **UPPERCASE** are considered as constants.
```python
PI = 3.14159265359
```

- What happens when creating a variable in Python?
  - A **memory space** is allocated to store the value.
  - The **value** is stored in the memory space.
  - The **variable name** is associated with the memory space.

```python
old_name = "Alice"
new_name = old_name
old_name = "Bob"
print(new_name)
```

<TumLogo />
<TumBarBottom />




---


# Data Types

Although not explicitly declared, variables in Python do have **data types**.

**Basic built-in data types**:
<v-clicks>

- **Integers**: whole numbers, e.g. `1, -2, 0, 1230, 456789`
  - Special: `0b1010` (binary), `0o123` (octal), `0x1A` (hexadecimal)
  - Separators: `1_000_000`
- **Float**: numbers with a decimal point, e.g. `1.0, 2.01, 999.999`
  - Scientific notation: `1e3` ($1 \times 10^3$), `1.23e-4` ($1.23 \times 10^{-4}$)
- **Complex**: numbers with a real and an imaginary part, e.g. `1 + 2j, 3.2 - 0.4j`
  - Both parts are floats, and the imaginary part is denoted by `j` or `J`
</v-clicks>

<TumLogo />
<TumBarBottom />


---


# Data Types

Although not explicitly declared, variables in Python do have **data types**.

**Basic built-in data types**:
<v-clicks>

- <span class="text-gray-400">**Integers**, **Float**, **Boolean**</span>
- **Boolean**: `True` or `False`
  - Comparison: `==`, `!=`, `<`, `>`, `<=`, `>=`
  - Logical: `and`, `or`, `not`
  - Bitwise: `&`, `|`, `^`, `~`, `<<`, `>>`
  - Identity & Membership: `is`, `is not`, `in`, `not in`
- **None**: a special type representing the absence of a value
</v-clicks>

<TumLogo />
<TumBarBottom />



---


# Data Types

Although not explicitly declared, variables in Python do have **data types**.

**Basic built-in data types**:
<v-clicks>

- <span class="text-gray-400">**Integers**, **Float**, **Boolean**, **None**</span>
- **String**: text, e.g. `"Hello", "world", '123'`
  - Escape characters: `"\t", "\\", "\'", "\"", "\n", "\r"`, (seldom used: `"\b", "\f", "\110", "\x48"`)
  - Raw strings: `r"Hello\nworld"`
  - Multiline strings: ...
  - f-strings: `f"Hello {name}!"`
</v-clicks>


<TumLogo />
<TumBarBottom />

<!-- 
```
\x48\x65\x6c\x6c\x6f: hello
'Age: %s. Gender: %s' % (25, True)
'growth rate: %d %%' % 7
'Hello, {0}, 成绩提升了 {1:.1f}%'.format('小明', 17.125)
print(f'{a=:.3f}') a=123.312
print(f'{b=:_}') b=1_231_234_321
print(f'{a=:12}') a=    123.3123
print(f'{a=:12.0f}') a=         123
```
-->



---

# Data Types

- Conversion between data types is possible.
  - `int()`: convert a numeric string or float to an integer
  - `float()`: convert a numeric string or integer to a float
  - `str()`: convert any data type to a string
  - `bool()`: convert any data type to a boolean
- The data type of a variable can be checked using the `type()` function.

```python
a = 123
b = 123.0
c = "123"
d = 2 + 3j
print(type(a), type(b), type(c), type(d.imag))
```

<TumLogo />
<TumBarBottom />



---

# Data Types

Strings are sequences of characters, and can be manipulated in various ways.

<v-clicks>

- **Indexing**: access individual characters using square brackets.
```python
s = "Hello hello hello "
print(s[0], s[1], s[-1], s[-2])
```

- **Slicing**: access a range of characters using square brackets.
```python
print(s[1:3], s[:3], s[2:], s[:], s[::2], s[-5::-1])
```

- **Concatenation**: combine strings using the `+` operator.
```python
print(s + " world!")
```

- **Repetition**: repeat a string using the `*` operator.
```python
print(s * 3)
```
</v-clicks>

<TumLogo />
<TumBarBottom />



---

# Data Types

Strings are sequences of characters, and can be manipulated in various ways.

<v-clicks>

- **Length**: get the length of a string using the `len()` function.
```python
print(len(s))
```

- **Membership**: check if a character or a substring is in a string using the `in` and `not in` operators.
```python
print("H" in s, "H" not in s, "h" in s)
```

- **Case**: change the case of a string using the `upper()`, `lower()`, `title()`, `capitalize()`, `swapcase()` methods.
```python
print(s.upper(), s.lower(), s.title(), s.capitalize(), s.swapcase())
```

- **Strip**: remove leading and trailing whitespace using the `strip()`, `lstrip()`, `rstrip()` methods.
```python
s = "  Hello  "
print(s.strip(), s.lstrip(), s.rstrip())
```
</v-clicks>


<TumLogo />
<TumBarBottom />



---

# Data Types

Strings are sequences of characters, and can be manipulated in various ways.

<v-clicks>

- **Replace**: replace a substring with another using the `replace()` method.
```python
print(s.replace("Hello", "Python"))
```

- **Split**: split a string into a list of substrings using the `split()` or `partition()` method.
```python
s = "Hello, world!"
print(s.split(","), s.partition(","))
```

- **Join**: join a list of strings into a single string using the `join()` method.
```python
s = ["Hello", "world!"]
print(" ".join(s))
```

- **Fill**: fill a string to a certain length using the `ljust()`, `rjust()`, and `center()` methods.
```python
s = "Hello"
print(s.center(20, "*"), s.ljust(20, "*"), s.rjust(20, "*")
```
</v-clicks>

<TumLogo />
<TumBarBottom />



---

# Data Types

Other string manipulation methods:

- **Search**: find the index of a substring using the `find()` and `index()` methods.
```python
s = "Hello, world!"
print(s.find("l"), s.index("l"))
```

- **Count**: count the occurrences of a substring using the `count()` method.
```python
print(s.count("l"))
```

- **Starts/Ends**: check if a string starts or ends with a substring using the `startswith()` and `endswith()` methods.
```python
print(s.startswith("Hello"), s.endswith("Python"))
```

- **Check**: check if a string is alphanumeric, lowercase, etc., using various `is...` methods.
```python
print(s.isalpha(), s.islower(), s.isspace(), s.istitle(), s.isupper())
```

<TumLogo />
<TumBarBottom />


---

# Data Types

Strings have a rich set of methods for manipulation because they contain a collection of sub-elements. A similar class of data types is **container**.

**Container data types**:
<v-clicks>

- **List**: a collection of elements, e.g. `[1, 2, 3, "a", "b", "c"]`
  - Indexing, slicing, concatenation, repetition, length, membership, etc.
  - Methods: `append()`, `extend()`, `insert()`, `remove()`, `pop()`, `clear()`, `index()`, `count()`, `sort()`, `reverse()`, etc.
- **Tuple**: an immutable collection of elements, e.g. `(1, 2, 3, "a", "b", "c")`
  - Indexing, slicing, concatenation, repetition, length, membership, etc.
  - Methods: `count()`, `index()`
</v-clicks>

<TumLogo />
<TumBarBottom />


---

# Data Types

Strings have a rich set of methods for manipulation because they contain a collection of sub-elements. A similar class of data types is **container**.

**Container data types**:
<v-clicks>

- <span class="text-gray-400">**List**, **Tuple**</span>
- **Set**: an unordered collection of unique elements, e.g. `{1, 2, 3, "a", "b", "c"}`
  - Membership, length, etc.
  - Methods: `add()`, `remove()`, `pop()`, `clear()`, `union()`, `intersection()`, `difference()`, `symmetric_difference()`, etc.
- **Dictionary**: a collection of key-value pairs, e.g. `{"name": "Alice", "age": 25}`
  - Indexing, length, membership, etc.
  - Methods: `keys()`, `values()`, `items()`, `get()`, `pop()`, `popitem()`, `clear()`, `update()`, etc.
</v-clicks>

<TumLogo />
<TumBarBottom />





---


# Coding with an Editor / IDE

Interactive Python interpreter is good for quick tests, but not for writing and saving code.

- Open a **code editor / IDE** (e.g. Visual Studio Code).
- **Greet the world** again with a simple line of code.

```python
name = "Alice"
greeting = f"Hello, {name}!"
print(greeting)
```

- Try to **execute the code** in the terminal or directly in the code editor / IDE.
```bash
python hello.py
```

<TumLogo />
<TumBarBottom />







---

# It's Conditional...

There are occasions when we want to execute different code based on different conditions.

- **if** statement: execute a block of code if a condition is true.
- **else** statement: execute a block of code if the same condition is false.
- **elif** statement: execute a block of code if the previous condition is false and the new condition is true.

```python {all|2,4}
grade = 85
if grade >= 50:
    print("Pass")
else:
    print("Fail")
```

- The code above can be suppressed using the **ternary operator**.

```python
result = "Pass" if grade >= 50 else "Fail"
print(result)
```

<TumLogo />
<TumBarBottom />


---

# It's Conditional...

- Chaining `if` and `else` statements follows a sequential order.
- Where are the mistakes in the following code?

```python {all|4,6,8,10,12,14}
# An earthquake with a force of 6.3 on the richter scale occurred
richter = 6.3

if richter >= 3.5:
    print("Felt but no destruction")
if richter >= 4.5:
    print("Damage to poorly built buildings")
elif richter >= 6.0:
    print("Some buildings collapse")
elif richter >= 7.0:
    print("Many buildings destroyed")
elif richter >= 8.0:
    print("Most structures fall")
else:
    print("Not noticed")
```

- `#` is used to denote a **comment**, which is not executed.

<TumLogo />
<TumBarBottom />


---

# It's Conditional...

- **Nested if** statements are also possible.

```python
temperature = 25
raining = False
if temperature > 20:
    if not raining:
        print("Go for a walk")
    else:
        print("Stay at home")
else:
    print("Stay at home")
```

- **Indentation** is crucial -- sometimes a nightmare -- in Python to define the scope of the code block.
- Indentation is usually **4 spaces**, but can be 2 or 8 spaces, or a tab.

<TumLogo />
<TumBarBottom />


---

# It's Conditional...

- Since Python 3.10, the **match** statement is introduced to simplify the conditional logic for simple cases.
- Not recommended in most cases due to potential inconsistency and incompatibility.

```python
error_code = 404
match error_code:
    case 200:
        print("OK")
    case 404:
        print("Not Found")
    case 500:
        print("Internal Server Error")
    case _:
        print("Unknown Error")
```

<TumLogo />
<TumBarBottom />




---

# Loops

Loops allow code to be executed repeatedly (i.e. in iterations). 

- **for** loop: execute a block of code for each element in a sequence.

```python
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    print(number)
```

- **while** loop: execute a block of code as long as a condition is true.

```python
number = 1
while number <= 5:
    print(number)
    number += 1
```

<TumLogo />
<TumBarBottom />


---

# Loops

You can skip or stop both `for` and `while` loops from within loops for more control.

- **continue** statement: skip the rest of the code in the current iteration and move to the next iteration.

```python
for number in range(10):
    if number % 2 == 0:
        continue
    print(number)
```

- **break** statement: stop the loop from executing and move to the next block of code.

```python
for number in range(10):
    if number == 5:
        break
    print(number)
```

<TumLogo />
<TumBarBottom />


---

# Loops

Tricks for loops:

- **else** statement: execute a block of code when the loop is finished without being stopped by a `break` statement.

```python {all|2-3}
for number in range(10):
    if number == 5:
        break
    print(number)
else:
    print("Loop finished")
```

<div v-click="1">
  <ul>
    <li>Try to comment out the highlighted line and see what happens.</li>
  </ul>
</div>

<div v-click="2">
<ul>
  <li><span style="font-weight: bold;">List comprehension</span>: list comprehension provides a more efficient way of looping.</li>
</ul>

```python
squares = [number**2 for number in range(10)]
print(squares)
```
</div>

<TumLogo />
<TumBarBottom />

<!-- 
if possible, you should always avoid using loops in Python, and use built-in functions or list comprehensions instead.

We say this is a more "Pythonic" way of doing things.
-->

---

# Loops

Useful generators for loops:

- **range()** function: generate a sequence of integers.

```python
for number in range(5, 10, 2):
    print(number)
```

- **enumerate()** function: generate a sequence of index-value pairs.

```python
for index, value in enumerate(["a", "b", "c"]):
    print(index, value)
```

- **zip()** function: generate a sequence of element-wise pairs.

```python
for a, b in zip([1, 2, 3], ["a", "b", "c"]):
    print(a, b)
```

<TumLogo />
<TumBarBottom />




---

# Functions

Repeated code can be encapsulated into a function for reuse.

- **Functions** are blocks of reusable code that can be called to perform a specific task.
- Similar to functions in mathematics, a function has the input (i.e., **argument**) and the output (i.e., **return value**).

```python
def greet(name):
    return f"Hello, {name}!"
```

- **Default values** can be set for arguments.
- Functions can be called with **positional arguments** or **keyword arguments**.
```python
def show_info(name, age=30, height=1.75):
    return f"{name} is {age} years old and {height:.2f} meters tall."

print(show_info("Alice"))
print(show_info("Bob", 25))
print(show_info(height=1.80, name="Charlie"))
```

<TumLogo />
<TumBarBottom />



---

# Functions

- Arguments can be **positional-only**, **keyword-only**, or **positional-or-keyword**.

```python
def show_info(old_name, new_name, /, age, city, *, height, weight):
    return f"{old_name} is now {new_name}, {age} years old,"
           f" from {city}, {height:.2f} meters tall,"
           f" and {weight:.2f} kg heavy."

print(show_info("Alice", "Bob", 25, city="Munich", height=1.80, weight=70))
```

- Sometimes you don't know how many arguments will be passed to a function.

```python
def get_info(name, *args, **kwargs):
    print(f"Hey, {name}!")
    print(args)
    print(kwargs)

get_info("Alice", 30, 1.75, city="Munich", weight=70)
```

<TumLogo />
<TumBarBottom />


---

# Functions

- Functions can return multiple values.
- Variables inside a function are **local** by default, and cannot be accessed outside.

```python
def get_info(a, b, c):
    return a, b, c

name, age, height = get_info("Alice", 30, 1.75)
print(a, b, c)
print(name, age, height)
```

<TumLogo />
<TumBarBottom />


---

# Functions

- A function can call itself inside, which is called **recursion**.

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

print(factorial(5))
```

- A special function called **lambda** can be used to create small anonymous functions.
- Similar to mathematical functions, Python functions can be nested.

```python
f = lambda x: x**2
g = lambda x, y: x + y
print(f(3))
print(f(g(3)))
```

<TumLogo />
<TumBarBottom />


---

# Functions

Python has a rich set of built-in functions.

**Commonly used built-in functions**:
<v-clicks>

- <span class="text-gray-400">`print()`, `input()`, `len()`, `type()`, `zip()`, `enumerate()`, `range()`, `int()`, `float()`, `str()`, `bool()`</span>
- `list()`, `tuple()`, `set()`, `dict()`: create a list, tuple, set, or dictionary
- `sum()`, `max()`, `min()`, `abs()`, `round()`, `pow()`, `divmod()`, ...: mathematical operations
- `sorted()`, `reversed()`, `map()`, `filter()`, `all()`, `any()`, ...: sequence operations
</v-clicks>

Check the [official documentation](https://docs.python.org/3/library/functions.html) for more built-in functions.

<TumLogo />
<TumBarBottom />


---

# Expanding your Toolbox!

Python has a rich set of libraries/modules for various purposes.

- **Libraries/modules** are code packages that you can load within your script in order to reuse functions that other programmers have already developed and made available.
- Python comes with some **internal libraries** (see https://docs.python.org/3/library/).
- **External libraries** can be installed by yourself through package managers like `pip` or `conda`.

<TumLogo />
<TumBarBottom />


---

# Expanding your Toolbox!

Modules can be loaded using the `import` statement.

**Commonly used internal libraries**:
<v-clicks>

- **`math`**: mathematical functions and constants

```python
import math
print(math.pi) # constant
print(math.sqrt(2), math.sin(3.2), math.log(10)) # functions
```

- **`random`**: random number generation

```python
import random
print(random.random(), random.randint(1, 10), random.choice(["a", "b", "c"]))
```

- **`datetime`**: date and time manipulation

```python
import datetime
print(datetime.datetime.now(), datetime.date.today())
```

</v-clicks>

<TumLogo />
<TumBarBottom />


---

# Expanding your Toolbox!

**Commonly used internal libraries**:
<v-clicks>

- **`iterools`**: functions creating iterators for efficient looping

```python
import itertools
print(list(itertools.permutations([1, 2, 3], 2)))
```

- **`functools`**: higher-order functions and operations on callable objects

```python
import functools
print(functools.reduce(lambda x, y: x * y, [1, 2, 3, 4]))
```

- **`collections`**: container datatypes

```python
import collections
print(collections.Counter("hello"))
```

</v-clicks>

<TumLogo />
<TumBarBottom />



---

# Expanding your Toolbox!

**Commonly used internal libraries**:
<v-clicks>

- **`os`**: operating system interfaces

```python
import os
print(os.getcwd(), os.listdir(), os.path.exists("hello.py"))
```

- **`sys`**: system-specific parameters and functions

```python
import sys
print(sys.version, sys.platform, sys.argv)
```

- **`argparse`**: command-line parsing

```python
import argparse
parser = argparse.ArgumentParser()
parser.add_argument("name")
args = parser.parse_args()
print(args.name)
```

</v-clicks>

<TumLogo />
<TumBarBottom />



---

# Working with Files

Python has built-in functions for file operations.

- **`open()`** function: open a file and return a file object.
- **`read()`** method: read the entire file content.
- **`readline()`** method: read a single line from the file.
- **`readlines()`** method: read all lines from the file and return a list.
- **`close()`** method: close the file.
```python
file = open("hello.txt", "r") # `r` for reading, `w` for writing, `a` for appending
first_line = file.readline()
content = file.read()
file.close()
print(first_line)
print(content)
```

<TumLogo />
<TumBarBottom />


---

# Working with Files

Python has built-in functions for file operations.

- **`write()`** method: write a string to the file.
```python
file = open("hello.txt", "w")
file.write("Hello, world!")
file.close()
```

- Remember to **close the file** after reading or writing!
- **`with`** statement (**recommended**): automatically close the file after reading or writing.

```python
with open("hello.txt", "r") as file:
    for line in file:
        print(line)
```

<TumLogo />
<TumBarBottom />



---

# Oops, Errors!

Python has built-in exceptions for error handling.

- **Exceptions** are events that can modify the flow of control through a program.
- **Error handling** is the process of responding to exceptions.
  - **`try`** block: the code that may raise an exception.
  - **`except`** block: the code that handles the exception.
```python
try:
    print(1 / 0)
except ZeroDivisionError as e:
    print(e)
```

<TumLogo />
<TumBarBottom />



---

# Oops, Errors!

Python has built-in exceptions for error handling.

- Different types of exceptions can be handled separately.
- **`else`** block: the code that is executed if no exception is raised.
- **`finally`** block: the code that is always executed.
```python
f = lambda x: 1 / x
try:
    # print(f(name='Alice'))
    print(f(0))
except ZeroDivisionError as e:
    print('Denominator cannot be zero')
except Exception as e: # catch all other exceptions
    print(e)
else:
    print("No exception")
finally:
    print("Always executed")
```

<TumLogo />
<TumBarBottom />


---

# Oops, Errors!

Python has built-in exceptions for error handling.

- **`raise`** statement: raise an exception manually.

```python
def divide(x, y):
    if y == 0:
        raise ZeroDivisionError("Denominator cannot be zero")
    return x / y

divide(1, 0)
```

- **`assert`** statement: raise an exception if a condition is false.

```python
old_password = "123"
new_password = "1234"
assert new_password != old_password, "New password cannot be the same as the old one"
```

<TumLogo />
<TumBarBottom />
