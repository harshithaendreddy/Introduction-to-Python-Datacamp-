# Python Lists


## 1. Python Data Types (00:09 - 00:33)
Before exploring lists, let's quickly recap Python's basic data types:

1. **int**: Represents integers (e.g., `1`, `42`, `-7`).
2. **float**: Represents real numbers with decimal points (e.g., `3.14`, `-2.0`).
3. **str**: Represents text (e.g., `'Hello'`, `'Python'`).
4. **bool**: Represents `True` or `False` values.

You can assign any of these types to variables. For example:

```python
x = 42        # int
y = 3.14      # float
name = "Alice"  # str
is_happy = True  # bool
```

## 2. The Problem (00:33 - 00:50)
In data analysis, you'll often deal with many data points. For instance, if you want to record the height of everyone in your family, creating a new variable for each person would be inefficient:

```python
height_mom = 1.62
height_dad = 1.75
height_sister = 1.55
# And so on...
```

### **Solution**: Use a Python List!
Lists allow you to store multiple data points in a single structure.

---

## 3. What Are Python Lists? (00:50 - 01:38)
### **Definition**
A list is a collection of values grouped under a single name. These values are enclosed in square brackets (`[]`) and separated by commas.

### **Key Features**
1. Lists can contain elements of any type: `int`, `float`, `str`, `bool`, or even other lists.
2. Lists can mix data types (e.g., a list can have integers and strings).

### **Example**
Suppose you measured your family's heights:

```python
# Create a list of heights
heights = [1.62, 1.75, 1.55, 1.80]

# Assign the list to a variable
family_heights = heights
```
Here, `family_heights` is a single variable holding all the height values.

---

## 4. Lists With Mixed Data Types (01:38 - 02:34)
### **Adding Names to the List**
You can include strings alongside numbers to specify which height belongs to whom:

```python
family = ["Mom", 1.62, "Dad", 1.75, "Sister", 1.55]
```

### **Using Sublists**
For better organization, use sublists to group related data:

```python
fam2 = [["Mom", 1.62], ["Dad", 1.75], ["Sister", 1.55], ["Brother", 1.80]]

# Print the list of lists
print(fam2)
```
**Output:**
```plaintext
[["Mom", 1.62], ["Dad", 1.75], ["Sister", 1.55], ["Brother", 1.80]]
```
Here, `fam2` is a list containing four sublists. Each sublist represents one family member's data.

---

## 5. List Type and Functionality (02:34 - 02:58)
Lists are a fundamental Python data type. Like other types (e.g., `int`, `str`), lists come with specific tools and behaviors.

### **Identifying List Types**
Use the `type()` function to confirm if a variable is a list:

```python
print(type(family))  # Output: <class 'list'>
print(type(fam2))    # Output: <class 'list'>
```




