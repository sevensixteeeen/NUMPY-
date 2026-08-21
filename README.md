# NumPy

NumPy (**Num**erical **Py**thon) is Python's core library for working with **arrays** and numerical computation. It underlies pandas, scikit-learn, PyTorch, and most of the Python data/ML stack.

---

## 1. What is NumPy?

NumPy provides `ndarray`, an N-dimensional array object, plus tools for linear algebra, Fourier transforms, and random number generation. Created in 2005 by Travis Oliphant, it's open source and free to use.

## 2. Why Use It Over Python Lists?

Python lists are flexible but slow for numerical work. NumPy arrays can be **up to 50x faster** because:

- Array data sits in **one continuous block of memory** (vs. lists, which store scattered pointers). This is called *locality of reference*.
- Core operations run in **C/C++**, not Python. NumPy is written partially in Python, but the performance-critical parts are C/C++.
- Operations are **vectorized**, applied to the whole array at once instead of looping element by element.

This matters most in **data science**: storing, processing, and analyzing large datasets fast.

---

## 3. Install

```bash
pip install numpy
```

```python
import numpy as np   # universal alias
```

---

## 4. Creating Arrays

```python
np.array([1, 2, 3])              # from a list → 1D array
np.array([[1, 2], [3, 4]])       # from nested lists → 2D array

np.zeros((3, 3))                  # 3x3 array of zeros
np.ones((2, 4))                   # 2x4 array of ones
np.arange(0, 10, 2)                # [0, 2, 4, 6, 8], like range()
np.linspace(0, 1, 5)               # 5 evenly spaced values between 0 and 1
np.random.rand(2, 2)                # 2x2 random values (0–1)
```

## 5. Indexing & Slicing

```python
a = np.array([[1, 2, 3], [4, 5, 6]])

a[0]          # first row → [1, 2, 3]
a[0, 2]       # row 0, col 2 → 3
a[:, 1]       # all rows, col 1 → [2, 5]
a[a > 3]      # boolean mask → [4, 5, 6]
```

## 6. Array Math (Vectorized)

```python
a = np.array([1, 2, 3])
b = np.array([10, 20, 30])

a + b          # [11, 22, 33]  (element-wise, no loop needed)
a * 2          # [2, 4, 6]
a.sum()        # 6
a.mean()       # 2.0
np.dot(a, b)   # 140, dot product
```

**Broadcasting**: NumPy automatically expands smaller arrays to match shapes during operations, so you rarely need manual loops.
```python
matrix = np.array([[1, 2], [3, 4]])
matrix + 10     # adds 10 to every element: [[11,12],[13,14]]
```

---

## 7. Common Methods Cheatsheet

| Task | Code |
|---|---|
| Shape / dimensions | `a.shape`, `a.ndim` |
| Reshape | `a.reshape(2, 3)` |
| Flatten to 1D | `a.flatten()` |
| Transpose | `a.T` |
| Concatenate | `np.concatenate([a, b])` |
| Stack | `np.vstack([a, b])`, `np.hstack([a, b])` |
| Min / max / index | `a.min()`, `a.max()`, `a.argmax()` |
| Sort | `np.sort(a)` |
| Unique values | `np.unique(a)` |

---

## 8. Writing Efficient NumPy Code

**Vectorize. Avoid Python `for` loops over arrays.**
```python
# ❌ Slow
result = [x * 2 for x in a]

# ✅ Fast, runs in C, not Python
result = a * 2
```

**Preallocate arrays instead of growing them in a loop.**
```python
# ❌ Slow (resizes/copies each iteration)
out = np.array([])
for x in data:
    out = np.append(out, x * 2)

# ✅ Fast, allocate once
out = np.empty(len(data))
for i, x in enumerate(data):
    out[i] = x * 2
# even better: out = data * 2 (fully vectorized)
```

**Set dtype explicitly** for large arrays to control memory:
```python
np.array([1, 2, 3], dtype="int32")   # vs default int64
```

**Use `np.where` instead of looping with if/else:**
```python
np.where(a > 2, "big", "small")
```

---

## 9. Quick Mental Model

- **ndarray** = fixed-type, contiguous-memory array → fast math
- **Vectorize first**: write `a + b`, not `for i in range: ...`
- **Broadcasting** = NumPy auto-expands shapes so you rarely loop manually
- **Shape mismatches** are the #1 source of NumPy errors. Check `.shape` when debugging

---

## Resources
- Official docs: https://numpy.org/doc/
- Video walkthrough (arrays, indexing, math, reshaping): https://youtu.be/QUT1VHiLmmI
