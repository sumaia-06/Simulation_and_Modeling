# Simulation and Modeling Lab

A collection of Python scripts demonstrating fundamental numerical computing operations using **NumPy**, along with visualization using **Seaborn** and **Matplotlib**. This repository covers mathematical functions, multidimensional matrix transformations, array sorting techniques, statistical summary metrics, and heatmaps.

---

## 📋 Table of Contents

* [Overview](https://www.google.com/search?q=%23overview)
* [Requirements & Installation](https://www.google.com/search?q=%23requirements--installation)
* [Project Tasks](https://www.google.com/search?q=%23project-tasks)
* [Task 1: Scalar & Array Operations](https://www.google.com/search?q=%23task-1-scalar--array-operations)
* [Task 2: 3×2 Matrix Operations](https://www.google.com/search?q=%23task-2-32-matrix-operations)
* [Task 3: 2×3 Matrix Operations & Advanced Sorting](https://www.google.com/search?q=%23task-3-23-matrix-operations--advanced-sorting)
* [Bonus: Dynamic Input & Heatmap Visualization](https://www.google.com/search?q=%23bonus-dynamic-input--heatmap-visualization)


* [Usage](https://www.google.com/search?q=%23usage)

---

## 🔍 Overview

This project provides step-by-step implementations of core NumPy workflows:

1. **Element-wise Mathematical Operations:** Applying trigonometric, logarithmic, exponential, rounding, and remainder functions across 1D arrays and 2D matrices.
2. **Safe Clipping:** Preventing math domain errors (e.g., `NaN` outputs during inverse trigonometric evaluations like `arcsin` or `arccos`) using domain clamping (`np.clip`).
3. **Sorting Mechanics:** Demonstrating row-wise ascending/descending sorts vs. global array flattening.
4. **Summary Statistics:** Computing min, max, indices (flat and 2D), median, mean, product, and standard deviation.
5. **Data Visualization:** Rendering matrix data visually with custom heatmaps.

---

## 🛠 Requirements & Installation

Make sure you have **Python 3.8+** installed. You can install the required dependencies via `pip`:

```bash
pip install numpy sympy matplotlib seaborn

```

---

## 🧪 Project Tasks

### Task 1: Scalar & Array Operations

Computes mathematical outputs for a 1D NumPy array using a custom scalar input:

* **Trigonometry:** `sin`, `cos`, `tan`, `arcsin`, `arccos`, `arctan`
* **Exponents & Logarithms:** Natural log (`np.log`) and base-$e$ exponential (`np.exp`)
* **Arithmetic & Rounding:** Absolute values, square roots, modulo/remainder, `round`, `floor`, and `ceil`

### Task 2: 3×2 Matrix Operations

Extends element-wise mathematical transformations to a $3 \times 2$ floating-point matrix. Input values are automatically normalized and clamped using `np.clip()` to maintain valid $[-1, 1]$ domains for inverse trigonometric routines.

### Task 3: 2×3 Matrix Operations & Advanced Sorting

Executes statistical analysis and multi-axis sorting on a $2 \times 3$ matrix:

* **Index Extraction:** Finds minimum and maximum elements using both flat 1D indices (`np.argmax`) and mapped 2D coordinate tuples (`np.unravel_index`).
* **Directional Sorting:**
* **Row-wise Ascending:** `np.sort(matrix, axis=1)`
* **Row-wise Descending:** `np.sort(matrix, axis=1)[:, ::-1]`
* **Full Matrix Ascending:** `np.sort(matrix.flatten())`
* **Full Matrix Descending:** `np.sort(matrix.flatten())[::-1]`


* **Statistical Metrics:** Sum, product, median, mean, and standard deviation.

### Bonus: Dynamic Input & Heatmap Visualization

Replaces static array declarations with dynamic matrix generation via `np.random.uniform(low, high, size)` and plots the resulting tensor as an annotated color heatmap using `seaborn.heatmap()`.

---

## 🚀 Usage

Execute the complete script pipeline in your terminal:

```bash
python main.py

```

### Sample Output Snippet (Task 3 Sorting)

```text
--- Task 3: 2x3 Matrix Operations ---
Original 2x3 Matrix:
 [[4.4 1.3 6.2]
  [1.9 3.0 7.9]]

Max value: 7.9 | Flat Index: 5 | 2D Index (row, col): (1, 2)
Min value: 1.3 | Flat Index: 1 | 2D Index (row, col): (0, 1)

--- Sorting ---
Row-wise Ascending:
 [[1.3 4.4 6.2]
  [1.9 3.0 7.9]]

Row-wise Descending:
 [[6.2 4.4 1.3]
  [7.9 3.0 1.9]]

Entire Matrix Ascending: [1.3 1.9 3.  4.4 6.2 7.9]
Entire Matrix Descending: [7.9 6.2 4.4 3.  1.9 1.3]

```
