# A Constraint Based Sudoku Solver. Using test and generate

## Example run


Input:

```java
Unsolved sudoku (Board1):
[
    [0, 6, 0, 1, 0, 4, 0, 5, 0], 
    [0, 0, 8, 3, 0, 5, 6, 0, 0], 
    [2, 0, 0, 0, 0, 0, 0, 0, 1], 
    [8, 0, 0, 4, 0, 7, 0, 0, 6], 
    [0, 0, 6, 0, 0, 0, 3, 0, 0], 
    [7, 0, 0, 9, 0, 1, 0, 0, 4], 
    [5, 0, 0, 0, 0, 0, 0, 0, 2], 
    [0, 0, 7, 2, 0, 6, 9, 0, 0], 
    [0, 4, 0, 5, 0, 8, 0, 7, 0]
]
```

Output:

```java
[
    [9, 6, 3, 1, 7, 4, 2, 5, 8],
    [1, 7, 8, 3, 2, 5, 6, 4, 9],
    [2, 5, 4, 6, 8, 9, 7, 3, 1],
    [8, 2, 1, 4, 3, 7, 5, 9, 6],
    [4, 9, 6, 8, 5, 2, 3, 1, 7],
    [7, 3, 5, 9, 6, 1, 8, 2, 4],
    [5, 8, 9, 7, 1, 3, 4, 6, 2],
    [3, 1, 7, 2, 4, 6, 9, 8, 5],
    [6, 4, 2, 5, 9, 8, 1, 7, 3]
]
// Checked board: true
```


## Example of use
```java
int[][] board1 = {
   {0, 6, 0, 1, 0, 4, 0, 5, 0},
   {0, 0, 8, 3, 0, 5, 6, 0, 0},
   {2, 0, 0, 0, 0, 0, 0, 0, 1},
   {8, 0, 0, 4, 0, 7, 0, 0, 6},
   {0, 0, 6, 0, 0, 0, 3, 0, 0},
   {7, 0, 0, 9, 0, 1, 0, 0, 4},
   {5, 0, 0, 0, 0, 0, 0, 0, 2},
   {0, 0, 7, 2, 0, 6, 9, 0, 0},
   {0, 4, 0, 5, 0, 8, 0, 7, 0}
};
SudokuSolver solver = new SudokuSolver(board1);
solver.solveSudoku();
System.out.println(solver.getSolvedSudokuAsString());        
System.out.println(solver.checkSudoku()); // Prints true
```
