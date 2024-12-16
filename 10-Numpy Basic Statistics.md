# Notes on NumPy: Basic Statistics and 2D Arrays

## 1. **Introduction to NumPy Arrays**  
NumPy is a powerful library in Python used for handling large, multi-dimensional arrays and matrices. It is particularly useful for numerical computations, such as basic statistics, linear algebra, and random number generation.

### 2. **Understanding NumPy Arrays**
   - **Type of NumPy Arrays**:  
     - NumPy arrays are of type `numpy.ndarray`.  
     - `ndarray` stands for "n-dimensional array," which indicates that NumPy can handle arrays of any number of dimensions (e.g., 1D, 2D, 3D, etc.).  
     - Example of a 1D array: `np_height` and `np_weight`.  
     - NumPy arrays can be created using lists, tuples, or other array-like structures in Python.

   - **Creating 2D NumPy Arrays**:  
     - A 2D NumPy array is a matrix-like data structure, created from a list of lists in Python.  
     - Example: 
       ```python
       np_2d = np.array([[1.75, 70], [1.80, 85], [1.60, 50], [1.55, 45], [1.90, 100]])
       print(np_2d.shape)  # Output: (5, 2), indicating 5 rows and 2 columns.
       ```
     - This 2D array can represent multiple attributes of data, such as height and weight for a group of people.

## 3. **Subsetting and Indexing 2D Arrays**
   - **Selecting Specific Elements**:  
     - In a 2D array, elements are accessed via row and column indices.  
     - Example of accessing the third element of the first row:
       ```python
       np_2d[0][2]  # or np_2d[0, 2]
       ```
     - **Advanced Subsetting**:  
       - Using a colon `:` to select multiple rows or columns:
         ```python
         np_2d[0:2, 1:3]  # Selects rows 0 and 1, and columns 1 to 2
         np_2d[1, :]      # Selects the entire second row
         np_2d[:, 1]      # Selects all rows in the second column
         ```
   - **Accessing Specific Rows and Columns**:  
     - If you want to select all rows for a specific column, use the syntax `np_2d[:, col_index]`.

## 4. **Basic Statistics with NumPy**
   NumPy provides various functions to calculate statistics, summarize, and analyze data efficiently.

   - **Mean**:  
     To find the average of a set of numbers, NumPy's `mean()` function can be used.  
     Example:  
     ```python
     np.mean(np_2d[:, 0])  # Mean of the height (first column) of all rows
     ```

   - **Median**:  
     The median is the middle value of a sorted set. You can calculate it using the `median()` function.  
     Example:  
     ```python
     np.median(np_2d[:, 0])  # Median height
     ```

   - **Standard Deviation (std)**:  
     Standard deviation measures the amount of variation or dispersion in a set of values.  
     Example:  
     ```python
     np.std(np_2d[:, 0])  # Standard deviation of the height
     ```

   - **Correlation Coefficient (corrcoef)**:  
     This function calculates the correlation between two variables.  
     Example:  
     ```python
     np.corrcoef(np_2d[:, 0], np_2d[:, 1])  # Correlation between height and weight
     ```

   - **Sum and Sort**:  
     You can calculate the sum of all elements in an array using `sum()` and sort the array using `sort()`.  
     Example:
     ```python
     np.sum(np_2d[:, 1])  # Sum of all weights
     np.sort(np_2d[:, 0])  # Sort heights
     ```

   - **Data Generation**:  
     NumPy allows you to generate random data using its random number generation functions. Example:
     ```python
     height = np.random.normal(1.75, 0.1, 5000)  # 5000 samples of height
     weight = np.random.normal(70, 15, 5000)    # 5000 samples of weight
     np_city = np.column_stack((height, weight))  # Combine into a 2D array
     ```

## 5. **Why Use NumPy for Basic Statistics?**
   - **Speed and Efficiency**:  
     NumPy performs statistical calculations faster than Python's built-in list operations due to its optimized C-based backend.  
   - **Memory Optimization**:  
     Arrays in NumPy require less memory compared to standard Python lists because of the type enforcement on arrays.

## 6. **Practical Application and Data Exploration**
   - **Exploring NumPy Arrays**:  
     In practice, analyzing and exploring your data typically involves:
     - Generating summary statistics like mean, median, and standard deviation.  
     - Visualizing the data (though visualization is beyond the scope of this video).  
     - Identifying any anomalies or data issues (e.g., an average weight of 2000 kg, which would be unrealistic).

---

## 7. **Key Points to Remember**
   - NumPy arrays can be created from lists or other array-like structures and can represent multi-dimensional data.
   - You can access elements in a 2D array using row and column indices.
   - NumPy offers several functions for statistical analysis such as `mean()`, `median()`, `std()`, `corrcoef()`, `sum()`, and `sort()`.
   - NumPy's efficiency in handling large datasets and performing computations makes it an essential tool for data analysis in Python.
