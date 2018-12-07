---
description: "ndarray is the earth of NumPy, it's the main data storage object of the framework. It is a homogeneus array, all the components share the same data-type. 
."
author: "Daniel Sobrado"
date: 2016-02-29
linktitle: Numpy ndarrays
next: /numpy-introduction
prev: /numpy-introduction
title: "Numpy: ndarrays"
image: https://i.imgur.com/oQNt9Gt.jpg
tags : [
    "Python",
	"Numpy"
]
categories : [
    "Data Science",
	"Programming"
]
---

# Creating ndarrays

We can get Numpy vector and a matrix rapidly from a Python list:

<pre class="prettyprint lang-py linenums">
vector = np.array([1,2,3,4])
vector
<span class="nocode" style="color:white">
Output:
$ array([1, 2, 3, 4])

</span>
matrix = vector.reshape((2,2))
matrix
<span class="nocode" style="color:white">
Output:
$ array([[1, 2],
         [3, 4]])
</span>
</pre>

We can quickly create matrices of ones and zeros: 

<pre class="prettyprint lang-py linenums">
all_zeros = np.zeros((3,3))
all_zeros
<span class="nocode" style="color:white">
Output:
$ array([[0., 0., 0.],
         [0., 0., 0.],
         [0., 0., 0.]])
</span>
all_ones = np.ones((3,3))
all_ones
<span class="nocode" style="color:white">
Output:
$ array([[1., 1., 1.],
         [1., 1., 1.],
         [1., 1., 1.]])
</span>
</pre>

We can create ndarrays initialized 

# Or 10 to 100?
arr = np.arange(10,100)
# If you want 100 steps from 0 to 1...
arr = np.linspace(0, 1, 100)
# Or if you want to generate an array from 1 to 10
# in log10 space in 100 steps...
arr = np.logspace(0, 1, 100, base=10.0)

We can observe some attributes from an ndarray, with the following operations, for an array defined as `np.array([(2,4,6)])`:

* itemsize: Will return `4`, that is the number of bytes used by the array. 
* dtype: `int32` is the result, that is the type of the elements in the array. (we can have np.int32, np.float16, np.float32, or np.float64)
* ndim: 


| Data type	Description                    |
|------------------------------------------|
| bool_	Boolean stored as a byte           |
| int_	Default integer type (either int64 or int32) |
| intc	C int (either int32 or int64) |
| intp	C ssize_t (either int32 or int64) |
| int8	Byte (-128 to 127)                  |
| int16	Integer (-32768 to 32767)          |
| int32	Integer (-2147483648 to 2147483647) |
| int64	Integer (-9223372036854775808 to 9223372036854775807) |
| uint8	Unsigned integer (0 to 255)        |
| uint16	Unsigned integer (0 to 65535)     |
| uint32	Unsigned integer (0 to 4294967295) |
| uint64	Unsigned integer (0 to 18446744073709551615) |
| float_	Shorthand for float64.            |
| float16	Half precision float: sign bit, 5 bits exponent, 10 bits mantissa |
| float32	Single precision float: sign bit, 8 bits exponent, 23 bits mantissa |
| float64	Double precision float: sign bit, 11 bits exponent, 52 bits mantissa |
| complex_	Shorthand for complex128.       |
| complex64	Complex number, represented by two 32-bit floats |
| complex128	Complex number, represented by two 64-bit floats |


# Structured arrays

# Slice and dice

# Broadcasting

When there is no ambiguity the smaller array will be expanded to match the shape of the bigger array.

<pre class="prettyprint lang-py linenums">
array = np.arange(1e8)
list = array.tolist()
<span class="nocode" style="color:white">
Output: 17.2 s ± 785 ms per loop (mean ± std. dev. of 7 runs, 1 loop each)
</span>
</pre>