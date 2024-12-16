# Python Functions: Detailed Notes

## 1. Introduction to Functions
- **What is a Function?**
  A function is a reusable block of code designed to perform a specific task. It allows you to avoid repeating code, making it easier to solve problems.
  
- **Functions You’ve Already Used**
  You’ve already encountered functions like `type()`, which returns the type of a value, and `max()`, which finds the maximum value in a list. These built-in functions are a great starting point for learning how to use functions in Python.

## 2. Using Built-in Functions

### Example with `max()`
- **Purpose of `max()`**: Finds the maximum value in a list.
- **How It Works**: You can use the `max()` function to find the maximum value from a list without writing the logic yourself.
  
  Example:
  ```python
  fam = [1.70, 1.89, 1.73, 1.80, 1.60]
  print(max(fam))  # Output: 1.89
  ```
  
- **Explanation**: You provide `fam` (the list) as an argument, and the function finds the largest value for you.

### Assigning Function Results to Variables
- You can assign the output of a function to a variable for further use.
  
  Example:
  ```python
  tallest = max(fam)
  print(tallest)  # Output: 1.89
  ```

## 3. The `round()` Function

- **Purpose**: Rounds a number to a specified number of decimal places.
- **Syntax**: `round(number, ndigits)`, where:
  - `number`: The number you want to round.
  - `ndigits`: The number of decimal places to round to (optional).
  
  Example 1: Rounding to 1 decimal place:
  ```python
  print(round(1.68, 1))  # Output: 1.7
  ```

  Example 2: Rounding to the nearest integer:
  ```python
  print(round(1.68))  # Output: 2
  ```

- **Explanation**: The `round()` function can be called with either one or two arguments. If only one argument is passed, Python rounds to the nearest integer by default.

### Function Internals
- The function `round()` takes two inputs, `number` and `ndigits`. The second input (`ndigits`) is optional, and Python automatically handles it if not provided. Internally, Python processes these arguments and returns the rounded number.

## 4. How to Find Functions in Python

- **Using Functions**: As you work with Python, you will encounter many standard tasks, and there is likely a built-in function to help you complete those tasks.
  
- **Finding Functions**: 
  - Search the internet or refer to Python documentation to discover functions that can help.
  - Utilize Python’s built-in `help()` function for additional information about functions. For example, `help(round)` will give you more details about the `round()` function.
  
  Example of using `help()`:
  ```python
  help(round)
  ```
