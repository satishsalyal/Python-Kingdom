# SciPy: A Comprehensive Tutorial


SciPy is an open-source Python library used for scientific and technical computing. 
It builds on NumPy and provides a large number of functions that operate on NumPy arrays. 
SciPy includes modules for optimization, integration, interpolation, eigenvalue problems, algebraic equations, signal and image processing, and many more.


## NumPy vs SciPy

```

import numpy as np
from scipy import linalg

A = np.array([[1, 2], [3, 4]])
print("NumPy array:")
print(A)

print("Determinant using SciPy:", linalg.det(A))

```

## Subpackages in SciPy


SciPy is organized into subpackages:
- `scipy.integrate`: Integration routines
- `scipy.optimize`: Optimization algorithms
- `scipy.fft`: Fast Fourier Transforms
- `scipy.signal`: Signal processing
- `scipy.linalg`: Linear algebra
- `scipy.sparse`: Sparse matrices
- `scipy.spatial`: Spatial algorithms
- `scipy.ndimage`: Multidimensional image processing
- `scipy.io`: Input/output including MATLAB file formats


## Basic Functions

```

from scipy import poly1d

p = poly1d([1, 0, -4])  # x^2 - 4
print("Roots of the polynomial x^2 - 4 are:", p.r)

```

## Special Functions

```

from scipy import special
import matplotlib.pyplot as plt

x = np.linspace(-5, 5, 100)
y = special.expit(x)  # Sigmoid function

plt.plot(x, y)
plt.title("Sigmoid Function (expit)")
plt.grid(True)
plt.show()

```

## Integration Functions

```

from scipy import integrate

result, error = integrate.quad(lambda x: x**2, 0, 3)
print("Integral of x^2 from 0 to 3:", result)

```

## Optimization Functions

```

from scipy.optimize import minimize

f = lambda x: (x - 3)**2 + 10
result = minimize(f, x0=0)
print("Minimum of f(x) = (x-3)^2 + 10 is at x =", result.x)

```

## Fourier Transform Functions

```

from scipy import fft

signal = np.random.random(100)
fft_signal = fft.fft(signal)
print("First 5 FFT coefficients:", fft_signal[:5])

```

## Signal Processing Functions

```

from scipy import signal

sig = np.array([1, 2, 3, 4, 5])
kernel = np.array([1, -1])
convolved = signal.convolve(sig, kernel, mode='valid')
print("Convolved Signal:", convolved)

```

## Linear Algebra

```

from scipy import linalg

A = np.array([[3, 1], [1, 2]])
b = np.array([9, 8])
x = linalg.solve(A, b)
print("Solution of linear system Ax = b is:", x)

```

## Sparse Eigenvalues

```

from scipy.sparse import csr_matrix
from scipy.sparse.linalg import eigs

sparse_matrix = csr_matrix([[1, 0], [0, 2]])
vals, vecs = eigs(sparse_matrix, k=1)
print("Largest eigenvalue of sparse matrix:", vals)

```

## Spatial Data Structures and Algorithms

```

from scipy.spatial import KDTree

points = np.random.rand(5, 2)
tree = KDTree(points)
distance, index = tree.query([0.5, 0.5])
print("Nearest neighbor to [0.5, 0.5] is:", points[index])

```

## Multidimensional Image Processing Functions

```

from scipy import ndimage

image = np.random.rand(5, 5)
filtered = ndimage.gaussian_filter(image, sigma=1)
print("Filtered Image:")
print(filtered)

```

## File IO

```

from scipy import io

data = {'array': np.arange(10)}
io.savemat("example.mat", data)
loaded = io.loadmat("example.mat")
print("Loaded data from MAT file:", loaded['array'])

```
