# Assignment 5: Quicksort Algorithm Implementation, Analysis, and Randomization

## Overview
This project was completed for **Algorithms and Data Structures** as part of **Assignment 5: Quicksort Algorithm Implementation, Analysis, and Randomization**.

The purpose of this assignment is to study Quicksort from both a theoretical and practical point of view. In this project, I implemented:

- a **deterministic Quicksort**
- a **randomized Quicksort**
- a **performance analysis** of both versions
- an **empirical comparison** using different input sizes and input distributions

The notebook is written in a clear step-by-step format so that the discussion and reasoning are separated from the code.

## Objectives
The main goals of this assignment are:

1. implement Quicksort in Python
2. explain its best-case, average-case, and worst-case time complexity
3. implement a randomized version of Quicksort
4. compare deterministic and randomized Quicksort experimentally
5. connect the observed results to the theoretical analysis

## Files Included
- `Assignment5_Quicksort_Polished_Student_Version.ipynb` — main notebook with explanation, implementation, testing, and analysis
- `README.md` — project overview and instructions
- `report` — include your written report file here if needed for submission
- `python file` — include a `.py` version if you export one separately

## What the Notebook Contains
The notebook is organized into the following sections:

- introduction and assignment purpose
- explanation of how Quicksort works
- partition function
- deterministic Quicksort implementation
- theoretical time complexity analysis
- randomized Quicksort implementation
- correctness checks
- empirical timing analysis
- discussion of results
- conclusion

This structure was chosen to make the notebook read more like a student submission and less like a raw coding file.

## Algorithms Implemented

### 1. Deterministic Quicksort
In the deterministic version, the pivot is always chosen using a fixed rule: the **last element** of the subarray.

This version is easy to implement and works well on many inputs, but it can perform poorly when the input is already sorted or reverse-sorted.

### 2. Randomized Quicksort
In the randomized version, the pivot is chosen **randomly** from the current subarray before partitioning.

This helps reduce the chance of repeatedly making poor pivot choices. While the theoretical worst case is still \(O(n^2)\), the expected running time is usually much better and more stable.

## Time Complexity Summary

### Deterministic Quicksort
- **Best Case:** O(n log n)
- **Average Case:** O(n log n)
- **Worst Case:** O(n^2)

### Randomized Quicksort
- **Expected Case:** O(n log n)
- **Worst Case:** O(n^2)

## Space Complexity
Both versions of Quicksort are considered in-place sorting algorithms, but recursive calls use stack space:

- **Best/Average Case:** O(log n)
- **Worst Case:** O(n)

## Empirical Analysis
The notebook compares both algorithms on three types of input:

- random input
- sorted input
- reverse-sorted input

It measures execution time for different input sizes and presents the results in a table.

### Expected Behavior
- On random input, both versions should usually perform well.
- On sorted and reverse-sorted input, deterministic Quicksort may become slower because of unbalanced partitions.
- Randomized Quicksort should usually behave more consistently across all input types.

## How to Run

### Option 1: Google Colab
1. Upload the notebook to Google Colab.
2. Open the notebook.
3. Run the cells from top to bottom.

### Option 2: Jupyter Notebook
1. Make sure Python 3 is installed.
2. Install Jupyter if needed:
   ```bash
   pip install notebook pandas
   ```
3. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open the notebook file:
   ```text
   Assignment5_Quicksort_Polished_Student_Version.ipynb
   ```
5. Run all cells in order.

## Requirements
The notebook uses standard Python libraries and one external library:

- `random`
- `time`
- `statistics`
- `sys`
- `typing`
- `pandas`

Install pandas if it is not already installed:
```bash
pip install pandas
```

## Example of What Is Tested
The notebook includes correctness checks on cases such as:

- empty list
- single-element list
- unsorted list
- list with duplicates
- sorted list
- reverse-sorted list

The output of both implementations is compared with Python’s built-in `sorted()` function.

## Main Takeaways
This assignment shows that Quicksort is a powerful and efficient sorting algorithm, but its performance depends a lot on pivot selection.

The deterministic version is simple, but it can be sensitive to input order.  
The randomized version improves reliability by reducing the chance of consistently bad partitions.

This makes randomized Quicksort more dependable in practical use.

## Notes
- Very large sorted or reverse-sorted inputs may still be slow for deterministic Quicksort because of recursion depth and worst-case behavior.
- The notebook uses moderate input sizes for fair and stable comparison.
- The writing in the notebook is intentionally separated from the code to improve readability.

## Author
**Sai Venkata Bharath Reddy Singareddy**

## Course
**Algorithms and Data Structures**

