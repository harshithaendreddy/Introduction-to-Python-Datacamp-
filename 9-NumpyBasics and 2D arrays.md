# **NumPy Basics and 2D Arrays**

## **1. Introduction to NumPy**
### **Objective:**
NumPy, short for **Numeric Python**, is a powerful Python package used for numerical computing. It provides an efficient way of handling and performing operations on large datasets, which is a key skill for aspiring data scientists.

### **Why NumPy?**
- Lists are useful in Python, but they are inefficient for performing operations on entire datasets, especially when it comes to numerical data.
- **NumPy arrays** allow fast, element-wise computations, making data manipulation more efficient.

---

## **2. Lists Recap**
### **Python Lists:**
- Python lists can store different types of data (integers, strings, floats, etc.) and allow operations like appending, removing, or updating elements.

### **Limitations:**
- **Operations across entire collections** (such as adding or multiplying every element) are not efficient or straightforward in Python lists. For example, trying to calculate the **Body Mass Index (BMI)** for multiple family members stored in lists would require looping through each element, which is cumbersome.

---

## **3. Solution: NumPy Arrays**
### **What is a NumPy Array?**
- A **NumPy array** is a more advanced data structure than the Python list, offering better performance and mathematical functionality.
- NumPy arrays support **element-wise operations**, which means calculations can be performed on every item in the array simultaneously, making it faster and easier.

### **Creating NumPy Arrays:**
```python
import numpy as np

# Creating NumPy arrays from Python lists
np_height = np.array([1.73, 1.80, 1.75])
np_weight = np.array([65.4, 85.2, 70.0])
```

### **Example: BMI Calculation**
```python
bmi = np_weight / np_height**2  # Element-wise operation
```

---

## **4. Key Features of NumPy Arrays**
### **Array Homogeneity:**
- Unlike Python lists, NumPy arrays must contain elements of the same type (e.g., all floats, all integers). If you try to mix types (e.g., strings with numbers), NumPy will coerce them into a single type (usually a string).

### **Array Operations:**
- **Element-wise operations** are straightforward with NumPy arrays. You can perform calculations like addition, subtraction, multiplication, etc., on entire arrays at once.

### **Example:**
```python
# NumPy arrays allow element-wise operations
np_height_squared = np_height ** 2
```

---

## **5. Comparison: Lists vs NumPy Arrays**
### **Python List (Inefficient for Calculations):**
```python
bmi = []
for i in range(len(height)):
    bmi.append(weight[i] / height[i]**2)
```

### **NumPy Array (Efficient and Simple):**
```python
bmi = np_weight / np_height**2  # Element-wise operation
```
- With NumPy, operations are **faster and more readable**, especially with large datasets.

---

## **6. Subsetting NumPy Arrays**
### **Accessing Array Elements:**
- **Single element:** Use the index (0-based) to access an element.
```python
bmi[1]  # Access BMI of second person
```

### **2D Arrays (Accessing Rows and Columns):**
- **2D arrays** are similar to lists of lists in Python.
```python
np_2d = np.array([[1.73, 65.4], [1.80, 85.2], [1.75, 70.0]])
```

### **Accessing Specific Rows and Columns:**
- You can access specific rows or columns in a 2D array using **slicing**.
```python
# Accessing first row
row_1 = np_2d[0]

# Accessing third column of second row
third_column = np_2d[1, 2]

# Slicing multiple rows and columns
subset = np_2d[1:3, 1:2]  # Rows 1 and 2, column 1
```

---

## **7. 2D NumPy Arrays: Practical Example**
### **Creating a 2D Array:**
- You can convert a **list of lists** into a 2D NumPy array.
```python
# Create 2D array for height and weight of family
np_2d = np.array([[1.73, 65.4], [1.80, 85.2], [1.75, 70.0]])
```

### **Array Shape:**
- Use `.shape` to get the dimensions of a 2D array (rows, columns).
```python
np_2d.shape  # Output: (3, 2), meaning 3 rows and 2 columns
```

### **Subsetting with Comma Notation:**
- You can use a **comma** to separate row and column indices.
```python
# Accessing specific row and column
np_2d[0, 1]  # First row, second column (height)
```

### **Selecting Multiple Rows/Columns:**
- You can use **slicing** to select multiple rows or columns.
```python
# Select first and second rows, second and third columns
subset = np_2d[0:2, 1:3]  # Note the exclusion of the upper bound in the slice
```

---

## **8. Advanced NumPy Array Subsetting**
### **Boolean Indexing:**
- Create a Boolean array based on a condition and use it to **filter data**.
```python
# Example: Get all BMI values above 23
bmi = np_weight / np_height**2
high_bmi = bmi > 23
bmi_above_23 = bmi[high_bmi]  # Select all BMI values where the condition is True
```

---

## **9. Remarks and Best Practices**
### **Element-wise Operations:**
- Remember, NumPy allows you to perform **element-wise calculations** efficiently, even for 2D arrays.

### **Homogeneity:**
- Always ensure that the array contains **only one data type** (e.g., float, integer). NumPy automatically converts mixed types to a common type.

### **Slicing and Indexing:**
- NumPy arrays offer **advanced subsetting** through slicing, which can be more intuitive compared to Python lists.

---

### **Summary of Key Takeaways:**
- **NumPy arrays** provide an efficient way of handling large datasets with **element-wise operations**.
- **2D arrays** can be created from lists of lists and offer enhanced indexing and subsetting functionality.
- **Boolean indexing** allows for filtering arrays based on conditions.
- **Subsetting** using both **indices** and **slices** is crucial for working with multidimensional data.
