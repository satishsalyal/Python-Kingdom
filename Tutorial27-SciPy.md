## Introduction to SciPy

- SciPy is an open-source Python library that is used for scientific and technical computing. 
- It is built on top of the NumPy library, and 
- it provides a large number of functions for optimization, integration, interpolation, signal processing, linear algebra, and more.
-  It is one of the most popular libraries for scientific computing in Python.

## Why use SciPy
- SciPy contains varieties of sub packages which help to solve the most common issue related to Scientific Computation.
- SciPy package in Python is the most used Scientific library only second to GNU Scientific Library for C/C++ or Matlab’s.
 -  Easy to use and understand as well as fast computational power.
-  It can operate on an array of NumPy library.

  ## Install SciPy using pip
To install, run the following command in the terminal:
```python
pip install scipy  
```

## Creating a function in SciPy

Creating a function in SciPy is similar to creating a function in Python. 
You can use the def keyword to define a function, and you can use the functions provided by SciPy to perform scientific calculations.

For example, let's create a function that computes the square root of a number using the scipy module:

```python

import scipy

def sqrt(x):
    return scipy.sqrt(x)
```
### Subpackages in SciPy:
SciPy has a number of subpackages for various scientific computations which are shown in the following table:

##   Name	                   Description
     cluster	               Clustering algorithms
     constants	               Physical and mathematical constants
      fftpack	               Fast Fourier Transform routines
      integrate	               Integration and ordinary differential equation solvers
      interpolate	           Interpolation and smoothing splines
      io	                   Input and Output
      linalg	                Linear algebra
      ndimage                  	N-dimensional image processing
      odr                    	Orthogonal distance regression
      optimize	                Optimization and root-finding routines
      signal	                Signal processing
      sparse	                Sparse matrices and associated routines
      spatial	                Spatial data structures and algorithms
      special	                Special functions
      stats	                   Statistical distributions and functions

## Modules of SciPy
SciPy provides a large number of modules for different scientific calculations. Here are some of the most commonly used modules:

### 1. scipy.optimize
The scipy.optimize module provides functions for optimization, which is the process of finding the best solution to a problem. 
It includes functions for minimizing or maximizing functions, finding roots of equations, and more.

### 2. scipy.integrate
The scipy.integrate module provides functions for numerical integration, which is the process of finding the area under a curve. 
It includes functions for computing definite integrals, solving ordinary differential equations, and more.

### 3. scipy.interpolate
The scipy.interpolate module provides functions for interpolation, which is the process of estimating the value of a function for an intermediate point. 
It includes functions for cubic splines, B-splines, and more.

### 4. scipy.signal
The scipy.signal module provides functions for signal processing, which is the process of analyzing and manipulating signals. 
It includes functions for filtering, Fourier transforms, wavelet transforms, and more.

### 5. scipy.linalg
The scipy.linalg module provides functions for linear algebra, which is the study of linear equations and their solutions.
It includes functions for solving linear systems, computing eigenvalues and eigenvectors, and more.

### 6. scipy.stats
The scipy.stats module provides functions for statistical analysis, which is the process of analyzing data to draw conclusions. 
It includes functions for computing probability distributions, performing hypothesis tests, and more.

These are just a few of the modules provided by SciPy. There are many more modules available for scientific computing in Python, and 
SciPy is a great library to use if you need to perform complex scientific calculations.

## SciPy provides a large number of functions for scientific and technical computing.
Here is a non-exhaustive list of some of the most commonly used functions:

- Integration functions: **_quad, dblquad, tplquad, fixed_quad, quadrature, romberg-**

- Optimization functions: **_minimize, root, linprog, curve_fit, fmin, fmin_bfgs, fmin_powell, fmin_cg, fmin_ncg_**

- Interpolation functions: **_interp1d, interp2d, interpn, griddata, spline, BSpline_**

- Linear algebra functions: **_solve, inv, det, eig, eigvals, svd, cholesky, qr, lu, norm_**

- Fourier transform functions: **_fft, ifft, fft2, ifft2, fftn, ifftn, rfft, irfft, dct, idct_**

- Signal processing functions: **_convolve, correlate, hilbert, hanning, hamming, kaiser, lfilter, resample, sosfilt_**

- Statistics functions: **_norm, binom, poisson, uniform, expon, beta, gamma, t, f, chi2, ks_2samp, ttest_ind_**

- Sparse matrix functions: **_csr_matrix, coo_matrix, lil_matrix, dok_matrix, issparse, spdiags, bsr_matrix_**

- Image processing functions: **_imread, imsave, imresize, imshow, rgb2gray, gray2rgb, label, find_contours, gaussian_filter_**

- Cluster functions: **_hierarchy.linkage, hierarchy.dendrogram, kmeans, fcluster_**

- Distance functions: **_euclidean, cityblock, hamming, jaccard, pdist, cdist_**

## Basic Functions:
## Interaction with NumPy:
SciPy builds on NumPy and therefore you can make use of NumPy functions itself to handle arrays. To know in-depth about these functions, you can simply make use of help(), info() or source() functions.

## help():
To get information about any function, you can make use of the help() function. There are two ways in which this function can be used:

without any parameters
using parameters
Here is an example that shows both of the above methods:

```python
from scipy import cluster
help(cluster)               #with parameter
help()                       #without parameter
```
When you execute the above code, the first help() returns the information about the cluster submodule. The second help() asks the user to enter the name of any module, keyword, etc for which the user desires to seek information. To stop the execution of this function, simply type ‘quit’ and hit enter.

## info():
This function returns information about the desired functions, modules, etc.

```python
scipy.info(cluster)
```
## SciPy constants
There are a variety of constants that are included in the scipy.constant sub-package.These constants are used in the general scientific area. 
Let us see how these constant variables are imported and used.
```python

from scipy import constants

print(constants.pi)
Output: 
3.1415926535897931
 
```

```python
from scipy import constants

print(dir(constants))
```
As you can see, we imported and printed the pio constant using SciPy.
The scipy.constant also provides the find() function, which returns a list of physical_constant keys containing a given string.

Consider the following example:

```python
from scipy.constants import find  
find('boltzmann')
 Output:
['Boltzmann constant',
 'Boltzmann constant in Hz/K',
 'Boltzmann constant in eV/K',
 'Boltzmann constant in inverse meter per kelvin',
 'Stefan-Boltzmann constant']
 ```
Here is how you can get the value of the required constant:

 The scipy.constant provides the following list of mathematical constants.

### Sr. No.	Constants	Description
        1.	pi	        pi
        2.	golden	    Golden ratio
        The scipy.constant.physical_sconstants provides the following list of physical constants.

        Sr.No.	Physical_Constants	Description
        1.	c	                    Speed of light in vacuum
        2.	speed_of_light	        Speed of light in vacuum
        3.	G	                    Standard acceleration of gravity
        4.	G	                    Newton Constant of gravitation
        5.	E	                    Elementary charge
        6.	R	                    Molar gas constant
        7.	Alpha	                Fine-structure constant
        8.	N_A	                    Avogadro constant
        9.	K	                    Boltzmann constant
        10	Sigma	                Stefan-Boltzmann constant σ
        11.	m_e	                    Electron mass
        12.	m_p	                    Proton mass
        13.	m_n	                    Neutron Mass
        14.	H	                    Plank Constant

## Example
```python
from scipy import constants
print(constants.tera)     #1000000000000.0
print(constants.giga)     #1000000000.0
print(constants.mega)     #1000000.0
print(constants.kilo)     #1000.0
print(constants.hecto)    #100.0
print(constants.deka)     #10.0
print(constants.deci)     #0.1
print(constants.centi)    #0.01
print(constants.milli)    #0.001
print(constants.micro)    #1e-06
````

## Special Functions:

SciPy provides a number of special functions that are used in mathematical physics such as elliptic, convenience functions, gamma, beta, etc. To look for all the functions, you can make use of help() function as described earlier.

### Exponential and Trigonometric Functions:
SciPy’s Special Function package provides a number of functions through which you can find exponents and solve trigonometric problems.

## Consider the following example:

EXAMPLE:

```python
from scipy import special
a = special.exp10(3)
print(a)
 
b = special.exp2(3)
print(b)
 
c = special.sindg(90)
print(c)
 
d = special.cosdg(45)
print(d)
```
OUTPUT:

1000.0
8.0
1.0
0.7071067811865475
      
