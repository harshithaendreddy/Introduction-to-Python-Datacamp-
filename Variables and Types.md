# **Python for Data Science: Variables and Types**

## **1. Introduction: Variables and Types**  
Python isn't just a powerful calculator; it allows you to save values for reuse, enabling more complex calculations. This is done using **variables**.

---

## **2. Variables**  
### **Definition**  
A variable is a name of the memory location used to store a value. Variables in Python are:  
- **Case-sensitive:** For example, `Height` and `height` are different.  
- **Assigned using the equals sign (`=`):** This associates a name with a value.  

### **Example**  
```python
# Assigning values to variables
height = 1.79  # Height in meters
weight = 68.7  # Weight in kilograms

# Accessing variable values
print(height)  # Outputs: 1.79
```

---

## **3. Calculating BMI (Body Mass Index)**  
### **Formula**  
The formula for BMI is:  
**BMI** = `weight (kg)` / `(height (m) ^ 2)`


### **Using Variables to Calculate BMI**  
```python
# Calculate BMI
bmi = weight / (height ** 2)
print(bmi)  # Outputs: 21.44
```  

### **Advantages of Using Variables**  
- **Reusability:** Makes it easier to reuse values in calculations.  
- **Reproducibility:** Simplifies updating calculations when values change.  

---

## **4. Reproducibility**  
Variables improve reproducibility in coding.  

### **Example**  
If you change the `weight` variable, the BMI calculation updates automatically:  
```python
# Update weight
weight = 75  # New weight in kilograms

# Recalculate BMI
bmi = weight / (height ** 2)
print(bmi)  # Outputs: Updated BMI
```

---

## **5. Python Types: Numerical Data**  
Python assigns a specific **type** to every value.  

### **Checking the Type**  
You can use the `type()` function to determine the type of a variable:  
```python
print(type(bmi))  # Outputs: <class 'float'>
```

### **Common Numerical Types**  
- **Float:** Represents real numbers, e.g., 1.79 or 21.44.  
- **Int:** Represents whole numbers, e.g., 42.  

---

## **6. Python Types: Strings and Booleans**  
Python provides other essential types:  

### **Strings**  
- Represent textual data.  
- Enclosed in single (`'`) or double (`"`) quotes.  

```python
name = "Python"
print(type(name))  # Outputs: <class 'str'>
```  

### **Booleans**  
- Represent logical values: `True` or `False`.  
- Useful for filtering data and logical operations.  

```python
is_adult = True
print(type(is_adult))  # Outputs: <class 'bool'>
```

---

## **7. Behavior of Operators with Different Types**  
The behavior of operators changes based on the types of their operands.  

### **Examples**  
#### Adding Integers  
```python
print(3 + 4)  # Outputs: 7
```  
#### Concatenating Strings  
```python
print("Data" + "Science")  # Outputs: DataScience
```  

### **Takeaway**  
Operators like `+` behave differently for numerical types and strings.

---

## **8. Practice and Application**  
### **What to Do**  
- Create variables to store values.  
- Experiment with different types (numerical, strings, booleans).  
- Understand how operators interact with various types.  

---

## **Key Takeaways**  
1. **Variables:** Allow you to store and reuse values efficiently.  
2. **Data Types:** Python supports multiple types, including numerical (int, float), strings, and booleans.  
3. **Operators:** Behave differently depending on the type of their operands.  
4. **Reproducibility:** Variables enable seamless recalculations by updating the values.
