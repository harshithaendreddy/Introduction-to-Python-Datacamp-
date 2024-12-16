# Python Methods and NumPy Basics

## 1. Python Methods

### 1.1. Built-in Functions
- **Python Functions**: Functions like `max`, `len`, etc., are built-in in Python.
  - `max()`: Finds the maximum of a list.
  - `len()`: Returns the length of a list or string.
- **Limitations**: Basic built-in functions don’t cover tasks like:
  - Getting the index of a specific element in a list.
  - Reversing a list.

### 1.2. Back to Basics: Python Objects
- **Python Objects**: All values and data structures in Python (like strings, floats, and lists) are objects.
  - Example: `"liz"` is a string object, `1.73` is a float object, and `[1.73, "liz"]` is a list object.
- **Methods**: These are functions that belong to specific Python objects. 
  - Example: `capitalize()` for strings and `replace()` for strings.

### 1.3. List Methods
- **Index Method**: Use `index()` to get the index of a specific element in a list.
  - Example: `fam.index("mom")` will return the index of `"mom"` in the `fam` list.
- **Count Method**: Use `count()` to find how many times an element occurs in a list.
  - Example: `fam.count(1.73)` will return the count of `1.73` in the list.

### 1.4. String Methods
- **String Methods**:
  - `capitalize()`: Capitalizes the first letter of a string.
  - `replace()`: Replaces part of the string with another string.
  - Example: `"liz".capitalize()` will return `"Liz"`, and `"liz".replace("z", "sa")` will return `"lisa"`.
  
### 1.5. Understanding Method Behavior
- **Method Behavior**: Methods can vary depending on the object type.
  - `index()` works differently on strings and lists. On strings, it returns the index of characters, whereas on lists, it returns the index of elements.
- **Mutating vs Non-Mutating Methods**:
  - Some methods, like `append()` on lists, mutate the object.
  - Others, like `replace()` on strings, return a new value without changing the original.

### 1.6. Summary of Python Methods
- Functions: e.g., `type()`, `max()`, `round()`.
- Methods: Functions specific to Python objects that can be called using dot notation (`object.method()`).
- Behavior of methods depends on the object type (e.g., list, string, etc.).

---

## 2. Introduction to NumPy

### 2.1. Python Lists and Operations
- **Limitations of Lists**: Lists in Python do not support efficient element-wise operations.
  - Example: Calculating the Body Mass Index (BMI) for multiple people using lists requires iterating over each element manually.

### 2.2. Solution: NumPy
- **NumPy**: A powerful package that provides an alternative to lists: NumPy arrays.
  - **NumPy Array**: Similar to lists but supports element-wise operations, making data manipulation and calculations faster.
  - Install NumPy: `pip3 install numpy`.

### 2.3. Using NumPy Arrays
- **Importing NumPy**: `import numpy as np`
- **Creating NumPy Arrays**: Use `np.array()` to create an array from a Python list.
  - Example: `np_height = np.array(height_list)` and `np_weight = np.array(weight_list)`.
- **Element-wise Operations**: Operations like BMI calculation are performed element-wise on arrays.
  - Example: `BMI = np_weight / np_height**2`.

### 2.4. Comparison of Python Lists vs NumPy Arrays
- **Python Lists**: Operations on lists do not work element-wise (e.g., BMI calculation will throw an error).
- **NumPy Arrays**: Operations work on the entire array element-wise.

### 2.5. NumPy Remarks
- **Single Data Type**: NumPy arrays require all elements to be of the same type.
  - Example: If you mix types (boolean and float), the array will store everything as a string.
- **Array Operations**: Array operations can behave differently compared to list operations.
  - Example: `python_list + python_list` results in a list concatenation, but `numpy_array + numpy_array` performs element-wise addition.

### 2.6. Subsetting NumPy Arrays
- **Basic Subsetting**: Use square brackets to access specific elements of the array.
  - Example: `bmi[1]` will return the BMI of the second person in the array.
- **Boolean Indexing**: You can use a condition to create a boolean array for subsetting.
  - Example: `bmi > 23` creates a boolean array where `True` corresponds to BMI values greater than 23.
  - Use this boolean array to filter values: `bmi[bmi > 23]` will return all BMI values above 23.

### 2.7. Practice and Further Learning
- Continue practicing and exploring NumPy in the exercises to deepen your understanding.

---

## 3. Key Takeaways

### 3.1. Python Methods
- **Methods** are functions tied to specific Python objects and are accessed using dot notation (`object.method()`).
- Methods can either modify the object they are called on (mutating) or return a new value (non-mutating).

### 3.2. NumPy Arrays
- **NumPy** offers a more efficient way to perform operations on large collections of data compared to regular Python lists.
- NumPy arrays support element-wise operations, making them essential for data manipulation in data science.
