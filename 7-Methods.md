# **Python Functions and Methods: Notes for Easy Revision**

## **1. Introduction to Functions**

### **What is a Function?**
- A **function** is a reusable piece of code aimed at solving a particular task.
- Functions allow you to perform specific actions without rewriting the code every time.
- Functions can be **built-in** (like `type()`, `max()`) or **user-defined**.

### **How Functions Work**
- Functions in Python are called using their **name** followed by parentheses `()`.
- You can pass **arguments** inside the parentheses to provide input to the function.

### **Example of Using Functions**
```python
fam = [1.60, 1.70, 1.89]
tallest = max(fam)  # max is a function that finds the maximum value in the list
print(tallest)  # Output: 1.89
```
- The **max()** function works as a black box: you don’t need to know its implementation; it just gives the result.
  
### **Function Return Values**
- The result of a function can be stored in a **variable** to be used for further calculations.

```python
tallest = max(fam)  # Store result in variable
```

## **2. Built-in Functions**

### **Common Built-in Functions**
- **max()**: Returns the maximum value from an iterable (like a list).
- **len()**: Returns the length of an object (e.g., list, string).
- **round()**: Rounds a number to a specified number of decimal places.

### **round() Function**
- The `round()` function rounds a number to the nearest integer or to a specified number of decimal places.
- **Syntax**:
```python
round(number, ndigits)
```
  - `number`: The number to round.
  - `ndigits`: The number of digits after the decimal (optional).

#### **Examples**:
```python
round(1.68, 1)  # Output: 1.7
round(1.68)     # Output: 2
```

### **Optional Arguments**
- `ndigits` is **optional**: if omitted, the function rounds to the nearest integer.

### **Help Function**
- You can get information about built-in functions using `help()`.
```python
help(round)
```

## **3. Methods in Python**

### **What are Methods?**
- A **method** is a function that "belongs" to an object in Python.
- Methods are specific to the type of object they are called on, such as strings, lists, or floats.
- **Example**: The string object has methods like `capitalize()` and `replace()`.

### **Calling Methods**
- Methods are called using the **dot notation**:
```python
string.capitalize()  # Calls the capitalize method on the string
```

#### **Examples of String Methods:**
- **capitalize()**: Capitalizes the first letter of the string.
```python
sister = "liz"
print(sister.capitalize())  # Output: "Liz"
```
- **replace()**: Replaces part of the string with another.
```python
print(sister.replace("z", "sa"))  # Output: "lisa"
```

### **Methods for Lists**
- Lists also have methods such as **index()** and **count()**.
- **index()**: Returns the index of a specified element in the list.
```python
fam = ["liz", 1.73, "mom"]
print(fam.index("mom"))  # Output: 4
```
- **count()**: Counts occurrences of a specified element in the list.
```python
print(fam.count(1.73))  # Output: 1
```

### **Types of Methods**
- Methods behave differently depending on the type of object (string, list, float, etc.).
- **Example**: The `index()` method works on both strings and lists but behaves differently:
  - On a **list**, it returns the index of an element.
  - On a **string**, it returns the index of a character.

### **Methods that Modify Objects**
- Some methods modify the object they are called on (i.e., **in-place changes**).
- **Example**: `append()` adds an element to a list.
```python
fam.append("me")  # Adds 'me' to the list
print(fam)  # Output: ['liz', 1.73, 'mom', 'me']
```

### **Important Note on Methods**
- Be cautious: Some methods modify objects, while others return new objects.
- Example: `append()` modifies the list, but methods like `replace()` return a new string.

## **4. Summary of Functions and Methods**

### **Functions**
- Functions are reusable pieces of code that can be called with arguments.
- Built-in functions like `max()`, `len()`, and `round()` are commonly used for standard tasks.
- Functions can return results to be stored in variables.

### **Methods**
- Methods are functions that belong to specific Python objects.
- They are called using dot notation on objects.
- Methods can modify objects in-place or return new objects, depending on the method.

