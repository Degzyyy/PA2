# 📘 PA 2 – Programming Assignment

👨‍💻 Author: Joshua de Guzman <br>
📅 Date: September 09, 2024 <br>
📚 Course: ECE2112 – Programming Assignment

# 📌 Version History

V1.0 (09-09-24) – Initial Release and Submission of GitHub Link

V1.1 (09-10-24) – Added README Documentation for Problems

V1.2 (09-11-24) – Added Code Snippets and Outputs in README

# 📌 Problem 1: Normalization Problem

This problem performs normalization on a 5×5 array. Normalization ensures that the dataset has a mean of 0 and a standard deviation of 1, which is useful in machine learning and data preprocessing.

Steps:
1. Create a 5×5 random array using np.random.rand(). 
2. Compute the mean using .mean() and standard deviation using .std().
3.Apply normalization using the formula:

X_norm = (X - mean) / std

4. Save the normalized array in a file named X_normalized.npy.

5. Load and print the results to confirm correctness.

# ✅ Input:
```
# PA 2 – Problem 1: NORMALIZATION PROBLEM

import numpy as np

# Create a random 5x5 array
X = np.random.rand(5, 5)

# Compute the mean and standard deviation
X_mean = X.mean()
X_std = X.std()

# Normalize the array
X_norm = (X - X_mean) / X_std

# Save to file
np.save('X_normalized.npy', X_norm)

# Print results
print("Original Array (X):\n", X)
print("\nNormalized Array (X_normalized):\n", X_norm)
```


# ✅ Output:
```
Original Array (X):
[[0.3303 0.3979 0.5035 ... 0.3271]
 [0.4594 0.0786 0.6237 ... 0.4925]
 ...
 [0.1711 0.5233 0.9936]]

Normalized Array (X_normalized):
[[-0.4571 -0.2005  0.2003 ... -0.4690]
 [ 0.4549 -1.4219  0.5754 ...  0.1585]
 ...
 [-1.0070  0.4360  1.9976  0.2089]]
```

# 📌 Problem 2: Divisible by 3 Problem

This problem generates the squares of the first 100 positive integers, reshapes them into a 10×10 array, and filters values that are divisible by 3.

Steps:

Create an array of numbers from 1 to 100 using np.arange().

Square the array values.

Reshape the squared numbers into a 10×10 array.

Use modulo % to find numbers divisible by 3.

Save the result as div_by_3.npy.

# ✅ Input:
```
# PA 2 – Problem 2: DIVISIBLE BY 3 PROBLEM

import numpy as np

num = np.arange(1, 101)
squares = num ** 2
A = squares.reshape((10,10))

div_by_3 = A[A % 3 == 0]

np.save('div_by_3.npy', div_by_3)

print("Original 10x10 Array:\n")
print(A)

print("\nArray of Squares Divisible by 3:\n")
print(div_by_3)
```

# ✅ Output:
```
Original 10x10 Array:
[[    1     4     9 ...   100]
 [  121   144   169 ...   400]
 ...
 [ 9604  9801 10000]]

Array of Squares Divisible by 3:
[   9   36   81  144 ... 9801]

```
# 🛠 Software(s) Used
<p align="left"> <img src="https://www.python.org/static/community_logos/python-logo.png" alt="Python Logo" width="120"/> <img src="https://jupyter.org/assets/homepage/main-logo.svg" alt="Jupyter Logo" width="90"/> </p>
📂 Repository Information

# Languages Used:

Python (100%)
