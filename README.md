# Generating-Sudoku-Puzzle-And-Its-Solver

## Objective:
The objective of this project is to generate sudoku puzzle and its solver

## Methodology: 
The major part of methodology includes studying the backtracking algorithm and how to use that with recursion. Also, we did search for the logic behind sudoku solver and sudoku generator.Using the backtracking algorithm. The initial code which we wrote was hard to debug and very large so we tried our best to make it short. 
The algorithm which we used is explained below:-
We are simply assigning a number to empty cells & checking its possibility. Number is possible only if it is not in that row, column & 3x3 subgrid. After checking the possibility we assign the number & recursively check if it leads to a unique solution. If yes, then we are done. If it doesn't lead to solution, we assign the next number to the empty cell & again check recursively. If no number from 1 to 9 leads to a solution then sudoku is not solvable & function returns false. The algorithm used is termed as BACKTRACKING ALGORITHM i.e. every possible combination is searched to solve a problem.For random sudoku generator, we are assigning random numbers at random places & checking if the generated grid has a unique solution. If yes, we are done. If no, then we are recursively creating random grids until it has a unique solution. Directly, checking for a solution is a bit computationally heavy. Let’s take an example,  suppose by random generator your grid has repeated numbers in a row. It's clear that this can’t be sudoku still it will go for finding a solution & search for various solutions by the combination of numbers & at last will give false. For this, we defined a function that can check if the randomly generated grid is possible as sudoku or not. If yes, then search for its solution. If no, then generate another grid & no need to check for a solution.Later, we are randomly removing 62 numbers from the solved randomly generated grid & printing it in a grid format.

### Results:
The results that we obtain after running code is shown below. In this, we have included three conditions and those are :

1)If the user enters **yes**  or  **y** or **YES**  or **Y**:

**OUTPUT:-**

Hii there!!!
Here's ur SUDOKU genius

 || _| _| _ || _| _| _ || _| _| _ ||
 
 || _| _| 1 || 7| _| _ || _| _| 5 ||
 
 || _| 9| 8 || 2| _| 5 || _| _| _ ||

 || _| _| _ || _| _| 6 || _| 9| _ ||
 
 || _| _| _ || _| _| _ || _| _| _ ||
 
 || _| _| _ || _| _| _ || 3| _| _ ||

 || _| 5| _ || _| _| _ || _| _| 7 ||
 
 || _| _| _ || _| _| 7 || _| _| 2 ||
 
 || _| 2| _ || _| 9| 4 || _| 5| 3 ||

Wanna know solution of this:  **yes**

So here is your answer 

 || 2| 3| 5 || 1| 4| 8 || 6| 7| 9 ||
 
 || 4| 6| 1 || 7| 3| 9 || 2| 8| 5 ||
 
 || 7| 9| 8 || 2| 6| 5 || 1| 3| 4 ||

 || 3| 1| 2 || 4| 5| 6 || 7| 9| 8 ||
 
 || 6| 7| 9 || 3| 8| 2 || 5| 4| 1 ||
 
 || 5| 8| 4 || 9| 7| 1 || 3| 2| 6 ||

 || 9| 5| 6 || 8| 2| 3 || 4| 1| 7 ||
 
 || 8| 4| 3 || 5| 1| 7 || 9| 6| 2 ||
 
 || 1| 2| 7 || 6| 9| 4 || 8| 5| 3 ||

2)If the user enters **no**  or **n** or **NO** or **N**:

**OUTPUT:-**

Hii there!!!
Here's ur SUDOKU genius

 || _| _| 3 || _| _| _ || _| 6| _ ||
 
 || _| _| _ || _| _| 6 || _| _| _ ||
 
 || 6| _| _ || _| _| _ || _| _| _ ||

 || 7| 1| _ || _| _| _ || _| _| 6 ||
 
 || _| 9| _ || _| _| _ || 1| 8| _ ||
 
 || _| _| _ || _| 9| _ || _| _| _ ||

 || 2| 3| _ || _| 8| _ || _| _| _ ||
 
 || _| 4| _ || _| _| _ || _| _| 2 ||
 
 || _| _| 1 || _| _| _ || 6| _| 5 ||

Wanna know solution of this : **no**

Okie, GoodBye

3)If the user enters **something unusual**:

**OUTPUT:-**

Hii there!!!
Here's ur SUDOKU genius

 || 1| 2| _ || _| 5| _ || _| 7| _ ||
 
 || _| _| _ || _| _| _ || _| _| _ ||
 
 || _| _| _ || 3| _| 9 || _| _| 4 ||

 || _| _| _ || _| _| _ || _| _| _ ||
 
 || _| 9| 6 || _| 1| _ || _| _| 5 ||
 
 || _| 7| _ || _| _| _ || 6| 2| 1 ||

 || _| _| _ || _| _| _ || _| 5| _ ||
 
 || _| _| _ || _| _| _ || _| _| _ ||
 
 || _| _| _ || 8| _| _ || _| 4| 7 ||

Wanna know solution of this : **KY**

Sry couldn’t get u.... YES or NO????

Wanna know solution of this :  **NO**

Okie, GoodBye

__And this is how code works__
