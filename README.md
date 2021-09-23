# Sudoku-Solver
Implementation of an object-oriented system for solving a sudoku board at an easy difficulty level

In order to build a solver for the Sudoku game, we will divide the problem into three parts. Each part will form a class. The departments are Cell,
SubGrid, Grid, representing a single cell, an inner square, and the board itself, respectively.

cell class have 3 fields:
i - holds the row index in the inner square where the cell is located, 0≤𝑖≤2.
j - holds the column index in the inner square where the cell is located, 0≤𝑗≤2.
values - holds a list of possible cell values (the values will be between 1 and 9).


subGrid class represents an inner square on the sudoku board. This class has 3 fields:
The field i - represents the number of the square (according to the numbering in the picture at the beginning of the question (0≤𝑖≤8).
The grid field - a list of 3x3 lists, with each cell holding a Cell type object. Cell Type Object with
Indexes i, j will be held in a grid matrix at position i, j.
The field collected_values - a list of cell values that have already been placed in an internal square (initial values ​​or values ​​that have already been
We have found (so far in an inner square numbered i.
For example, for square number 5 in the following table:
![image](https://user-images.githubusercontent.com/81520237/134527565-1a5fc06f-4e14-44c1-85eb-20d95c351080.png)


The values will be:
i = 5
grid = [[Cell(0, 0), Cell(0, 1), Cell(0, 2, 3)],
[Cell(1, 0), Cell(1, 1), Cell(1, 2, 1)],
[Cell(2, 0), Cell(2, 1), Cell(2, 2, 6),]]
collected_values = [3, 1, 6] (doesn’t have to be in this order)

Grid class represents the Sudoku game board in its entirety. The department has 3 fields:
The sub_grids field - a list of 9 lengths, which holds all the inner squares of the board. The cell in position i will be an object
Of the SubGrid type numbered i.
The rows field - a list containing 9 internal lists of numbers, where the internal list in position i will contain all the values
We have so far solved in line number i.
The columns field - a list that contains 9 internal lists of numbers, where the internal list in position i will contain all
The values we have solved so far in column number i.
