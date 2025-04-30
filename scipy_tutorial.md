# 🔬 SciPy: Scientific Computing in Python

## 🧠 What is SciPy?

**SciPy** is an open-source Python library that extends the capabilities of **NumPy**. It provides a comprehensive collection of mathematical algorithms and functions built on top of NumPy arrays. SciPy is widely used in scientific and engineering disciplines for:

- Numerical integration
- Optimization
- Signal and image processing
- Linear algebra
- Interpolation
- Statistics
- And more...

### 🚀 Why Use SciPy?

- **High-performance**: Built on optimized libraries like BLAS, LAPACK, and C libraries.
- **Rich functionality**: Covers a wide range of numerical and scientific tasks.
- **Extensible**: Works seamlessly with other scientific packages like `pandas`, `matplotlib`, `SymPy`, and `scikit-learn`.

---

## 🔍 NumPy vs SciPy

| Feature       | NumPy                         | SciPy                                       |
|---------------|-------------------------------|---------------------------------------------|
| Purpose       | Efficient array computation   | Advanced scientific computation             |
| Scope         | Array objects and basic math  | Specialized algorithms (e.g., optimization) |
| Dependencies  | Core dependency                | Built on top of NumPy                       |

### 🧮 Example

```python
import numpy as np
from scipy import linalg

A = np.array([[1, 2], [3, 4]])
print("Determinant using SciPy:", linalg.det(A))
```

---

## 🧩 Key Subpackages in SciPy

SciPy is organized into specialized submodules:

| Subpackage         | Purpose                             |
|--------------------|-------------------------------------|
| `scipy.integrate`  | Numerical integration               |
| `scipy.optimize`   | Optimization algorithms             |
| `scipy.fft`        | Fast Fourier Transforms             |
| `scipy.signal`     | Signal processing                   |
| `scipy.linalg`     | Linear algebra                      |
| `scipy.ndimage`    | Multidimensional image processing   |
| `scipy.io`         | Input/output operations             |
| `scipy.spatial`    | Spatial data structures and queries |
| `scipy.stats`      | Statistical functions               |

---

## 🛠️ Installation

You can install SciPy using pip:

```bash
pip install scipy
```

Or with conda:

```bash
conda install scipy
```

---

---

## 🔢 Constants in SciPy

SciPy includes a comprehensive set of scientific constants in the `scipy.constants` module. These are especially useful for physics, chemistry, and data science applications.

### 🧪 Example: Print the Value of π (Pi)

```python
from scipy import constants

print(constants.pi)
```

### 📋 Listing All Constants

To see all available constants:

```python
from scipy import constants

print(dir(constants))
```

🧠 These constants include units for energy, mass, temperature, angles, and more.

---

## ⚙️ Optimizers in SciPy

SciPy provides a collection of optimization tools in the `scipy.optimize` module. These tools are useful for:

- Minimizing functions (used in machine learning models)  
- Finding the root of equations

### 🧮 Finding Roots of Non-linear Equations

Unlike NumPy, SciPy can find roots of non-linear equations.

#### 📌 Example: Solve `x + cos(x) = 0`

```python
from scipy.optimize import root
from math import cos

def eqn(x):
    return x + cos(x)

solution = root(eqn, 0)
print("Root:", solution.x)
```

🧠 **Explanation:**
- `eqn` is the function to solve  
- `0` is the initial guess  
- The root is accessed with `.x`

---

## 🧊 Sparse Data and Matrices

Sparse data refers to datasets where most elements are zeros or empty.

🔸 **Example:**

```python
[1, 0, 2, 0, 0, 3, 0, 0, 0]
```

This kind of data is common in scientific computing, especially in linear algebra, PDEs, and machine learning.

### 🧰 Working with Sparse Matrices

SciPy’s `scipy.sparse` module provides efficient structures for sparse data. Two common formats are:

- **CSR (Compressed Sparse Row):** Best for row slicing, matrix-vector products.  
- **CSC (Compressed Sparse Column):** Best for arithmetic and column slicing.

### 🧱 Example: Creating a CSR Matrix

```python
import numpy as np
from scipy.sparse import csr_matrix

arr = np.array([0, 0, 0, 0, 0, 1, 1, 0, 2])
sparse_matrix = csr_matrix(arr)

print(sparse_matrix)
```

#### 🔍 Output:
```
  (0, 5)	1
  (0, 6)	1
  (0, 8)	2
```

This shows only non-zero entries with their (row, column) positions and values.

### 🔍 View Stored (Non-Zero) Values Only

```python
arr2d = np.array([[0, 0, 0], [0, 0, 1], [1, 0, 2]])
sparse = csr_matrix(arr2d)

print(sparse.data)
```

---

## 📥 Importing SciPy Modules

To use any module from SciPy, import it directly:

```python
from scipy import constants
print(constants.liter)  # How many cubic meters in a liter
```
