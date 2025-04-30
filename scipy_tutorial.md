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

# SciPy Tutorial: Interpolation, Linear Algebra, IO, and Image Processing

## Interpolation with SciPy

Interpolation is the process of estimating unknown values that lie between known data points. SciPy provides a convenient sub-package, `scipy.interpolate`, which simplifies this task. It supports both 1-D (univariate) and multivariate (e.g., spatial) interpolation.

### 1-D Interpolation Example

Let’s begin with a simple 1-D interpolation using the `interp1d` function.

```python
import numpy as np  
import matplotlib.pyplot as plt  
from scipy.interpolate import interp1d  

# Define known data points
x = np.linspace(0, 5, 10)  
y = np.cos(x**2 / 3 + 4)  

# Plot the data points
plt.scatter(x, y, c='r')  
plt.title("Original Data Points")
plt.show()
```

#### Using Different Interpolation Methods

We will now use `interp1d` to perform linear and cubic interpolation.

```python
fun1 = interp1d(x, y, kind='linear')  
fun2 = interp1d(x, y, kind='cubic')  

xnew = np.linspace(0, 4, 30)  

plt.plot(x, y, 'o', xnew, fun1(xnew), '-', xnew, fun2(xnew), '--')  
plt.legend(['Data', 'Linear', 'Cubic'], loc='best')  
plt.title("Linear vs Cubic Interpolation")
plt.show()
```

You can change the input range to observe how interpolation methods behave at different sections:

```python
xnew = np.linspace(3, 5, 30)  
plt.plot(x, y, 'o', xnew, fun1(xnew), '-', xnew, fun2(xnew), '--')  
plt.legend(['Data', 'Linear', 'Cubic'], loc='best')  
plt.title("Interpolation in Range 3 to 5")
plt.show()
```

### Supported Interpolation Methods

- `linear`
- `nearest`
- `zero`
- `slinear`
- `quadratic`
- `cubic`

---

## Linear Algebra with SciPy

SciPy offers high-performance linear algebra operations via the `scipy.linalg` module. It uses optimized libraries like BLAS and LAPACK.

### Why `scipy.linalg` over `numpy.linalg`?

While `numpy.linalg` provides basic functionality, `scipy.linalg`:
- Contains all `numpy.linalg` features
- Includes additional advanced features
- Is always compiled with optimized BLAS/LAPACK support

### Solving Linear Systems

We solve a system of linear equations:

\[
\begin{align*}
x + 2y - 3z &= -3 \\
2x - 5y + 4z &= 13 \\
5x + 4y - z &= 5
\end{align*}
\]

```python
from scipy import linalg  
import numpy as np  

A = np.array([[1, 2, -3], [2, -5, 4], [5, 4, -1]])  
b = np.array([[-3], [13], [5]])  

x = linalg.solve(A, b)  
print("Solution:\n", x)

# Verify the solution
print("Check (Ax - b):\n", A.dot(x) - b)
```

### Determinant of a Matrix

```python
A = np.array([[1, 2, 9], [3, 4, 8], [7, 8, 4]])  
det = linalg.det(A)  
print("Determinant of A is:", det)
```

### Eigenvalues and Eigenvectors

```python
A = np.array([[2, 1, -2], [1, 0, 0], [0, 1, 0]])  
values, vectors = linalg.eig(A)  

print("Eigenvalues:\n", values)  
print("Eigenvectors:\n", vectors)
```

---

## SciPy I/O Operations

The `scipy.io` module helps handle a variety of data formats such as `.mat` files (MATLAB), `.wav`, `.arff`, and others.

### Working with MATLAB Files

Save a structure in MATLAB:

```matlab
my_struct = struct('lon', 78, 'lat', 56)
save('test.mat', 'my_struct')
```

Load the file in Python:

```python
from scipy.io import loadmat  

data = loadmat('test.mat')  
lon = data['lon']  
lat = data['lat']
```

---

## SciPy ndimage: Image Processing

`scipy.ndimage` provides functions for multi-dimensional image processing.

### Load and Display Image

```python
import scipy.misc
import matplotlib.pyplot as plt

face = scipy.misc.face()  # Raccoon face image
plt.imshow(face)
plt.title("Original Image")
plt.axis('off')
plt.show()
```

### Crop Image

```python
lx, ly, _ = face.shape  
crop_face = face[int(lx/4):-int(lx/4), int(ly/4):-int(ly/4)]  
plt.imshow(crop_face)
plt.title("Cropped Image")
plt.axis('off')
plt.show()
```

### Rotate Image

```python
from scipy import ndimage  

rotated = ndimage.rotate(face, 180)  
plt.imshow(rotated)
plt.title("Rotated Image")
plt.axis('off')
plt.show()
```

### Gaussian Blurring

```python
from scipy import ndimage  

gray_face = scipy.misc.face(gray=True)  
blurred = ndimage.gaussian_filter(gray_face, sigma=3)  
very_blurred = ndimage.gaussian_filter(gray_face, sigma=5)

plt.figure(figsize=(9, 3))
plt.subplot(131)
plt.imshow(gray_face, cmap='gray')
plt.title("Original")
plt.axis('off')

plt.subplot(132)
plt.imshow(very_blurred, cmap='gray')
plt.title("Very Blurred")
plt.axis('off')

plt.subplot(133)
plt.imshow(blurred, cmap='gray')
plt.title("Blurred")
plt.axis('off')

plt.tight_layout()
plt.show()
```

### Sharpening Image

```python
f = scipy.misc.face(gray=True).astype(float)  
blurred = ndimage.gaussian_filter(f, sigma=3)  
sharpened = blurred + 30 * (blurred - ndimage.gaussian_filter(blurred, 1))

plt.figure(figsize=(12, 4))
plt.subplot(131)
plt.imshow(f, cmap='gray')
plt.title("Original")
plt.axis('off')

plt.subplot(132)
plt.imshow(blurred, cmap='gray')
plt.title("Blurred")
plt.axis('off')

plt.subplot(133)
plt.imshow(sharpened, cmap='gray')
plt.title("Sharpened")
plt.axis('off')

plt.tight_layout()
plt.show()
```

### Edge Detection with Sobel Filter

```python
import numpy as np  

im = np.zeros((256, 256))  
im[64:-64, 64:-64] = 1  
im = ndimage.rotate(im, 15, mode='constant')  
im = ndimage.gaussian_filter(im, sigma=8)

sx = ndimage.sobel(im, axis=0, mode='constant')  
sy = ndimage.sobel(im, axis=1, mode='constant')  
edges = np.hypot(sx, sy)

plt.figure(figsize=(9, 4))
plt.subplot(121)
plt.imshow(im, cmap='gray')
plt.title("Original Square")
plt.axis('off')

plt.subplot(122)
plt.imshow(edges, cmap='gray')
plt.title("Sobel Edge Detection")
plt.axis('off')

plt.tight_layout()
plt.show()
```
