# 📘 NumPy Basics

> 🧠 **TL;DR**: In this notebook, I explored NumPy basics including array creation, attributes, operations, and matrix math.  
> I also compared NumPy arrays with Python lists in terms of memory and speed, proving why NumPy is essential for ML workflows.

> NumPy is the foundation for libraries like `pandas`, `scikit-learn`, `TensorFlow`, and `PyTorch`.  
> Mastering it means writing faster and more efficient code for data analysis and machine learning.

---

## 📌 What I Learned

### 1️⃣ Creating Arrays
You can create NumPy arrays from:
- Python lists & tuples ➡️ `np.array([1, 2, 3])`
- Built-in NumPy methods:
  - `np.zeros((2, 3))` → array of 0s  
  - `np.ones(5)` → array of 1s  
  - `np.arange(0, 10, 2)` → sequence  
  - `np.linspace(0, 1, 5)` → evenly spaced values

```python
import numpy as np
np.array([1, 2, 3])
np.zeros((2, 3))
np.linspace(0, 1, 5)
```

---

### 2️⃣ Array Attributes

Attributes give useful metadata about arrays:

```python
arr = np.array([[1, 2], [3, 4]])
print(arr.shape)   # (2, 2)
print(arr.ndim)    # 2
print(arr.dtype)   # int64
print(arr.size)    # 4
```

---

### 3️⃣ Array Functions & Operations

* `reshape()`, `flatten()`, `.T` (transpose)
* Element-wise math operations: `+`, `-`, `*`, `/`
* Broadcasting — automatically expands smaller arrays in operations

```python
arr = np.array([[1, 2], [3, 4]])
print(arr * 2)
print(arr + np.array([[10, 20], [30, 40]]))  # Broadcasting
```

---

### 4️⃣ Matrix Operations

* Matrix multiplication using `np.dot()` or `@`
* Other linear algebra tools like `inv()`, `transpose()`, and `identity()`

```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

print(np.dot(A, B))
print(A @ B)

# Boolean masking
x = np.array([[1, 2, 3], [4, 5, 6], [7, 0, 1]])
np.where(x > 5)
```

---

### 5️⃣ 🔥 Why NumPy is Better Than Python Lists

#### ✅ Memory Comparison
NumPy uses significantly less memory than Python lists:

<img width="589" alt="Screenshot 2025-07-05 at 12 15 09 AM" src="https://github.com/user-attachments/assets/fa38a9cc-cfd4-4606-bacb-dd3d18c1f5fb" />

#### ✅ Runtime Comparison
NumPy is faster due to vectorization and C-level optimization:

<img width="579" alt="Screenshot 2025-07-05 at 12 16 47 AM" src="https://github.com/user-attachments/assets/ea91c0c8-4177-47ae-9bcd-76dafc66a4b3" />


## ⚙️ Tools Used
- Python 3.x
- NumPy v1.24+
- Jupyter Notebook / Colab

