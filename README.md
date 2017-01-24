# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?

A: Naked Twins is another constraint propagation strategy we can use to reduce the search space of the Sudoku problem. Basically, if there are two boxes in the same unit (row, column, square, or diagonal) have the same two values (they are twins!), the rest boxes of the same unit shall not have those values (need to be eliminated).
What I did were:

- Get all the boxes with two possible values into a list
- Find the twins
	- Pick one box from the list (box A)
	- Get two values of the box
	- Find another box in the same unit with the same values (box B)
- Eliminate two values from the same unit other than box A and B

The code could be optimized.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?

A: In addition to the row, column, and square units, the diagonal sudoku added additional constraint. The values 1 to 9 shall only be used once on the two diagonal boxes. This is additional constraint we can take advanage. The diagonal units have to meet the constraint of other units, so the work for solving diagonal sudoku is to correctly define those units and add them to the unit list. All the algorithm should be the same as the other units.