# matrix

A python package for matrix operations and manipulations.

## Contents

* [Back-Story](#back-story)
* [Features](#features)
* [Installation](#installation)
* [Usage](#usage)
* [Uninstallation](#uninstallation)
* [Contributing](#contributing)
* [TODO](#todo)

## Back-Story

I had just completed my "Journey through the Docs", finished studying the Core Python aspect of the Python Docs (majorly the Library & Language Reference, wherever else those referred me to and whatever else i needed to fully understand) with interactive sessions, testing things out and making notes.

Then i needed something to put to (real) practice all the things i had learned.
I wanted something purely **Standard** Python, no 3rd-party libraries and seemed this project would be a good place to start.

The project was actually concieved in the course of my "Journey through the Docs" but only stayed on my TODO list till after.

It's been interesting so far and the project actually turned out to incoparate a lot of what i learned... though, definitely not all. :smile:

**NOTE:** This project is not intended to be a "re-invention of any wheel", it's basically just me practicing.
I actually made sure i didn't test out or go through any similar project, till i had implemented all I originally planned to.

## Features

This is just an outline of the major features of the library. For the complete feature list, detailed descriptions and project documentation, see the [documentation](docs/index.md).

### Matrix initialization. Via:
* The class constructor
* Utility functions to generate:
  * Unit matrices.
  * Matrices filled with random integer elements.
  * Matrices filled with random floating-point elements.

### Matrix object interactions
* Intelligent string representation
* Subscription
  * Single-element indexing, assignment and deletion
  * Block-slice (sub-matrix) subscription and assignment.
* Truthiness
* Membership test for elements
* Iteration over elements
* Per-element rounding

### Matrix object properties
* Size
* Number of rows
* Number of columns
* Determinant
* Principal diagonal
* Trace

### Matrix Operations
* Negation
* Equality comparison
* Addition and subtraction
* Scalar multiplication
* Matrix multiplication
* Division (by scalar)
* Inverse
* Transpose
* Augmentation
* Row reduction

### Tests for matrix properties and special matrices
* Diagonality
* Nullity
* Orthogonality
* Squareness
* Symmetry
* Triangularity
* Identity matrix
* Conformability

### Matrix views
These are views of the matrix object, like `.keys()` and `.values()` are to `dict`.

* Rows and Columns (and their slices). Support:
  * Single row/column Indexing
  * Slicing of multiple rows/columns (Yes, a slice of rows/columns can still be sliced further! :sunglasses:)
  * Row/column assignment and deletion (Rows/Columns slices **DO NOT** support these).
  * Length (number of rows/columns "in" the view)
  * Iteration over rows/columns
* Row and column. Support:
  * String representation
  * Single element indexing
  * Multiple element slicing
  * Equality comparison
  * Mathematical operations (Also supports augmented assignment of these operations):
    * Addition and subtraction of rows and/or columns (Element-wise)
    * Multiplication and Division by scalar
    * Multiplication and Division by row/column (i.e inter-operation of two rows/columns element-by-element)
    * **NOTE:** Augmented assignments of these operations are performed **in-place** i.e affect the matrix itself.
  * Row/column length
  * Membership tests
  * Iteration over elements

### Other operations on matrices
* Horizontal and vertical flip
* Clockwise and anti-clockwise rotation
* Matrix copy
* Matrix resize
* Rounded comparison


## Installation

Download and unzip this [repository](https://github.com/AnonymouX47/matrix/archive/refs/heads/main.zip) or run
```sh
git clone https://github.com/AnonymouX47/matrix
```

Change your Working Directory to that of the repository; run
```sh
cd matrix
```

Then, run
```sh
python setup.py install
```
OR run
```
python -i test.py
```
to just test it out without installing the package.

**NOTE:** For windows users, Python must've been added to PATH (For help, check [here](https://datatofish.com/add-python-to-windows-path/)).


## Usage

Quick example:
```python
>>> from matrix import Matrix
>>> print(Matrix(4, 4))
―――――――――――――――――
| 0 | 0 | 0 | 0 |
―――――――――――――――――
| 0 | 0 | 0 | 0 |
―――――――――――――――――
| 0 | 0 | 0 | 0 |
―――――――――――――――――
| 0 | 0 | 0 | 0 |
―――――――――――――――――
```

For more usage examples, check the [samples](samples/).

For the complete feature list and descriptions, see [Features](docs/features.md).


## Uninstallation

To uninstall the package, run
```sh
pip uninstall matrix
```


## Contributing

If you find any bug or have any suggestion for an improvement, please open an **Issue** in the [Issues section](https://github.com/AnonymouX47/matrix/issues), they're greatly welcomed.

Please make sure you check other issues first to make sure you don't create a duplicate.


## TODO

1. Solution to systems of linear equations.
   * Though still currently possible i.e `x = ~A @ b`.
2. Implementation of methods to find eigenvalues and eigenvectors.
   * This requires a polynomial "solver" (at least for the general approach) and I'm currently working on that.

Please note that I personally **do NOT** plan to implement any "more efficient" algorithms for the matrix operations in this project. It's not the point of this project (at least, as of now) but contributions are welcome.

