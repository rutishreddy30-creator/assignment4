AI Backtracking Algorithms – README

 Overview:-

This project implements three classic Artificial Intelligence problems using the Backtracking algorithm:

1. Map Coloring Problem
2. Sudoku Solver
3. Cryptarithmetic Puzzle Solver

Backtracking is a systematic search technique that explores all possible solutions and abandons invalid paths early.

 Requirements:-

* Python 3.x
* No external libraries required (only built-in modules like `itertools` are used)

 1. Map Coloring Problem

Description:The map coloring problem assigns colors to regions such that:
* No two adjacent regions have the same color.
This is a Constraint Satisfaction Problem (CSP)

 Implementation Details:
* Uses recursive backtracking
* Checks constraints using:

  ```python
  is_valid_color()
  ```
* Assigns colors from a predefined domain

 Test Cases:

- Australia Map

* Regions: WA, NT, SA, Q, NSW, V, T
* Colors used: Red, Green, Blue
* Tasmania (T) has no neighbors

- Telangana Map (Partial)

* Example districts included:

  * Adilabad, Nirmal, Nizamabad, Jagtial, Kamareddy
* Colors used: Red, Green, Blue, Yellow
* Can be extended to all 33 districts

Output Example:-

```id="a1"
{'WA': 'Red', 'NT': 'Green', 'SA': 'Blue', ...}
```

 Key Concepts:-
* Constraint Satisfaction Problems (CSP)
* Backtracking Search
* Graph Representation

2. Sudoku Solver

Description:Solves a 9×9 Sudoku puzzle where:
* Each row contains numbers 1–9
* Each column contains numbers 1–9
* Each 3×3 subgrid contains numbers 1–9

 Implementation Details:
* Uses backtracking recursion
* Functions used:

  * `find_empty()` → finds empty cells
  * `is_valid_sudoku()` → checks constraints
  * `solve_sudoku()` → main solver

 Input Format:

* 2D list (matrix)
* Empty cells represented by `0`

Example:

```id="a2"
[5, 3, 0, 0, 7, 0, 0, 0, 0]
```

Output Example:

```id="a3"
[5, 3, 4, 6, 7, 8, 9, 1, 2]
...
```

Key Concepts:

* Backtracking
* Constraint checking (row, column, subgrid)
* Recursive search

 3. Cryptarithmetic Solver

 Description:Solves puzzles where letters represent digits.

Example:

```id="a4"
SEND + MORE = MONEY
```

 Implementation Details:
* Uses permutations of digits (0–9)
* Each letter gets a unique digit
* Leading digits cannot be zero

 Output Example:

```id="a5"
Mapping: {'S': 9, 'E': 5, 'N': 6, 'D': 7, ...}
Equation: 9567 + 1085 = 10652
```

---

Key Concepts:
* Brute-force search with pruning
* Permutations (`itertools`)
* Constraint satisfaction


Algorithm Used: Backtracking

Steps:-

1. Choose a variable
2. Assign a value
3. Check constraints
4. Recurse
5. Backtrack if invalid

Time Complexity:-

* Map Coloring: O(m^n)
* Sudoku: O(9^(n*n)) (worst case)
* Cryptarithmetic: O(10!)

 Advantages:-

* Guarantees correct solution (if exists)
* Simple and general approach

 Limitations:-

* Can be slow for large inputs
* Exponential time complexity

 How to Run:-

```bash
python filename.py
```

Conclusion:-

This project demonstrates how backtracking can be applied to solve:

* Constraint Satisfaction Problems
* Logical puzzles
* Combinatorial problems
