## Python Crash Course Notes and Examples

### I. Introduction and Setup

**Python as a Language**
Python is one of the **most popular programming languages** and is highly sought after for jobs. It is known for being **powerful and easy to use**. Unlike many other programming languages that have complex syntax and a steep learning curve, Python has a low learning curve, and a first program can often be written in seconds. It is often used for writing awesome scripts and **automating tasks**.

**Installation and Environment**
1.  **Version:** There are two major versions, Python 2 (a legacy version that is not actively maintained or officially supported) and **Python 3** (the future and newest version). Python 3 is recommended for beginners. This material uses Python 3.10.
2.  **IDE (Integrated Development Environment):** An IDE is a special program or environment designed for writing, running, and executing Python code. It provides feedback on errors. The recommended IDE is **PyCharm** (specifically the free and open-source Community version).
3.  **Project Setup:** When creating a new project, ensure that **Python version three is selected as the interpreter**.

### II. Basic Programming Structure

**Execution Flow**
Programming in Python involves providing the computer a **set of instructions**. Python executes the lines of code in the file sequentially, meaning the **order of instructions matters a lot**.

**Output: Print Statements**
The `print()` function is a basic instruction used to output information onto the screen or console (called the **console**).

| Concept | Description | Example |
| :--- | :--- | :--- |
| **Print Output** | Outputs text (strings) enclosed in quotation marks or variables. | `print("hello world")` |
| **Sequential Flow** | Instructions are executed in order. | `print("line 1")` followed by `print("line 2")` |

### III. Variables and Scalar Data Types

**Variables**
A **variable** is essentially a container used to **store certain data values**. Storing values in variables makes dealing with different data types easier and helps manage data inside programs.

*   **Naming Convention:** When naming variables composed of multiple words, generally **separate the words using an underscore** (e.g., `character_name`).

| Data Type (Scalar) | Description | Example |
| :--- | :--- | :--- |
| **String (`str`)** | Used to store **plain text**, enclosed in quotation marks (`"` or `'`). Strings are immutable; they cannot be modified in place. | `character_name = "Tom"`, `"draft Academy"` |
| **Number** | Stores numerical values. Can be **integers** (whole numbers) or **floats** (decimal numbers). When storing a number, quotation marks are not needed. | `character_age = 50`, `3 + 4.5`, `50.5678213` |
| **Boolean (`bool`)** | Stores a **true or false** value (`True` or `False`). These values are super important in programming. | `is_mail = True` |
| **None** | The Python "null" value. There is only one instance of the `None` object. | `a = None` |

**Key Operations on Data Types**

*   **String Manipulation:**
    *   **Concatenation:** Using the `+` operator to append one string onto another. Example: `phrase + " is cool"`.
    *   **Indexing:** Accessing an individual character using square brackets `[]`. Indexing starts at **position 0**. Example: `phrase` gets the first character.
    *   **Escape Character (`\`):** Used to insert special characters literally, such as a quotation mark (`\"`) or a new line (`\n`).
    *   **String Functions/Methods:** Functions can be used to modify strings or get information about them.
        *   `.index("substring")`: Returns the starting index of the character or substring.
        *   `.replace("old", "new")`: Replaces specified words or letters.
        *   `.count("value")`: Counts the number of nonoverlapping occurrences of a substring.
*   **Number Functions:** Python supports basic arithmetic operations like addition, subtraction, and multiplication.
    *   **Conversion:** To print a number next to a string, the number must first be converted using the `str()` function. Example: `print("My favorite number " + str(my_num))`.
    *   **Math Functions:** Advanced math functions (like `round()`, `floor()`, `sqrt()`, `abs()`) are available. To access many specific math functions, the **`math` module** must be imported using `import math` or `from math import *`.

### IV. User Input and Control Flow

**Getting User Input**
The **`input()`** function prompts the user to enter information, and that information can be stored in a variable. Data received from the user generally comes in as a string.

*   **Handling Number Input:** If user input needs to be used as a number for calculations, the string input must be **converted** using the `int()` or `float()` functions.
    *   *Example:* `num_one = int(input("Enter first number: "))`

**Decision Making: If/Elif/Else Statements**
`if` statements allow programs to make **decisions by checking conditions**.

*   **Structure:** They use `if`, optionally `elif` (else if), and optionally `else` (otherwise). Code blocks within conditional statements must be **indented**.
*   **Logical Operators:** Used to combine conditions: `and`, `or`, and `not`.
*   **Comparison Operators:** Used to compare values.
    *   Equality: `==`
    *   Inequality: `!=`
    *   Greater/Less Than: `>`, `<`, `>=`, `<=`

**Loops**
Loops allow a block of code to be repeatedly executed.

1.  **While Loop:** Executes a block of code **as long as a specified condition is true**.
    *   *Example:*
        ```python
        i = 1
        while i <= 10: 
            print(i)
            i += 1  # shorthand for i = i + 1
        print("Done with loop") 
        ```
2.  **For Loop:** Used to **loop over collections of items** (e.g., iterating through a string, a list, or a range of numbers).
    *   **Iterating over a collection:** `for friend in friends:`.
    *   **Iterating over a range:** The `range(N)` function generates a sequence of integers starting at 0 and going up to, but **not including**, N.
    *   *Example:* `for index in range(5):`.

### V. Data Structures

**Lists**
Lists are used to store **lists of related values** (a sequence of mutable Python objects).

*   **Definition:** Defined using **square brackets `[]`**.
*   **Mutability:** Lists are **variable length** and their contents can be modified in place.
*   **Access:** Items are accessed by their **index position**, starting at 0.
*   **List Functions/Methods:**
    *   `.extend(list)`: Appends another list onto the end of the current list.
    *   `.append(item)`: Adds one item to the end of the list.
    *   `.insert(index, item)`: Inserts an item at a specific index.
    *   `.remove(item)`: Removes the first matching item.
    *   `.copy()`: Creates a duplicate list.

**Tuples**
A tuple is a type of data structure similar to a list, but it is a **fixed-length, immutable sequence** of Python objects.

*   **Definition:** Defined using **parentheses `()`**.
*   **Immutability:** Once created, its values **cannot be changed or mutated**. This is useful for storing data that should not be changed.
*   **Access:** Elements are accessed using square brackets and indexing, similar to lists.

**Dictionaries (Dicts)**
Dictionaries store information in **key-value pairs**.

*   **Definition:** Defined using **curly brackets `{}`**.
    *   *Example:* `month_conversions = {"JAN": "January", "FEB": "February"}`.
*   **Keys:** Keys must be **unique**. Keys are used to access the associated value.
*   **Accessing Values:**
    1.  Using square brackets and the key: `month_conversions["JAN"]`.
    2.  Using the **`.get()`** method. This method allows you to specify a default value to return if the key is invalid, preventing an error.

### VI. Functions and Object-Oriented Programming (OOP)

**Functions**
A **function** is a collection of code that performs a specific task, primarily used for **code organization and reuse**.

*   **Definition:** Defined using the keyword **`def`**, followed by the function name, parentheses (which may contain parameters), and a colon (`:`).
*   **Indentation:** The code block inside the function must be **indented**.
*   **Parameters (Arguments):** Information passed into the function. Parameters receive values when the function is called, allowing the function to be more flexible.
*   **Return Statement:** The **`return`** keyword is used to return a specific value or piece of information back to where the function was called. Any code written after the `return` statement in a function will not be executed.

**Classes and Objects**
Classes allow developers to create **custom data types** (creating an "object model") to model real-world entities.

*   **Class:** A **class** is the template or definition for the custom data type, defined using the `class` keyword. It specifies the attributes (properties) that the object should have.
    *   *Example:* A `Student` class defines that a student has a name, major, GPA, and probation status.
*   **Object:** An **object** is an **instance** created from the class definition. An object has actual information assigned to its attributes.
    *   *Example:* Creating a student object: `student_one = Student("Jim", "Business", 3.1, False)`.
*   **Class Functions (Methods):** Functions defined inside a class (often called methods) can modify the objects of that class or figure out information about them.
*   **Inheritance:** A mechanism where a new class (e.g., `ChineseChef`) can **inherit the functions and capabilities** of an existing class (e.g., `Chef`), avoiding the need to rewrite common functionality.

### VII. Environment, Modules, and Error Handling

**Modules and PIP**
1.  **Module:** A module is a Python file (`.py`) containing reusable code (functions, variables) that can be imported and accessed in another file using the **`import`** statement. This is critical for importing functionality from external Python files.
2.  **PIP (Package Manager):** A program (often pre-installed with newer Python 3 versions) used to **install, manage, update, and uninstall external or third-party Python modules**. The command `pip install module_name` is typically used to install modules.

**The Python Interpreter**
The **Python interpreter** is a standalone environment (accessed via typing `python3` in the terminal/command prompt) used to execute Python commands in a **sandbox environment**. It is useful for testing small amounts of code instantly without setting up a full file or project ("quick and dirty tests").

**Error Handling**
The **`try/except` block** is used to watch out for specific errors (exceptions) and handle them gracefully, preventing the program from completely crashing.

*   The code that might cause an error is placed in the **`try`** block.
*   The code that handles the error is placed in the **`except`** block.
*   It is a best practice to catch **specific errors** (e.g., `ValueError`) rather than accepting any exception.

**Comments**
A comment is a line of text that is **ignored by the Python interpreter**.

*   **Usage:** Used to leave notes, reminders, or explain lines of code to human readers (other developers or oneself).
*   **Syntax:** Comments begin with the hash mark (`#`).
*   **Commenting Out Code:** Comments can be used to temporarily disable (comment out) a line or block of code without deleting it.

**File Operations**
The `open()` function is used to interact with external files for reading or writing.

*   **Modes:** Different modes control interaction: `"r"` (read-only), `"w"` (write-only, which overwrites the file), `"a"` (append), or `"r+"` (read and write).
*   **Closing:** It is necessary to close the file when finished to release its resources. The `with` statement can automatically close files upon exiting the block.

### VIII. Python for Data Analysis Context

Python has developed a **large and active scientific computing and data analysis community**. It is an excellent choice for building data applications due to its strength in **general-purpose software engineering**.

**Core Data Libraries**
1.  **NumPy (Numerical Python):** A cornerstone for numerical computing. It provides the efficient **multidimensional array object `ndarray`**, functions for element-wise computations, linear algebra, and random number generation. NumPy arrays are the standard *lingua franca* for data exchange between scientific libraries.
2.  **pandas:** Provides high-level data structures like the **`DataFrame`** (a tabular, column-oriented structure with row and column labels) and **`Series`** (a one-dimensional labeled array). pandas is especially designed for working with **structured or tabular data** and is critical for data manipulation, preparation, and cleaning.
3.  **matplotlib:** The most popular Python library for producing **plots and other two-dimensional data visualizations**.
4.  **IPython/Jupyter:** The IPython shell is an enhanced interactive Python interpreter. The **Jupyter notebook** is an interactive document format that allows users to author content mixing code, text (Markdown/HTML), and data visualizations.