# Artificial Intelligence Sudoku Problem - Shoven Shrivastava


# Question 1 (Naked Twins)
Q 1 : How do we use constraint propagation to solve the naked twins problem?

A: Constraint propagation is the process of communicating the domain reduction of a decision variable to all of the constraints that are stated over this variable. 

This process can result in more domain reductions. These domain reductions, in turn, are communicated to the appropriate constraints. This process continues until no 

more variable domains can be reduced or when a domain becomes empty and a failure occurs. An empty domain during the initial constraint propagation means that the 

model has no solution. (from IBM knowledge center).

In Sudoku, Naked twins is a strategy to reduce the number of possibilities. The objective is to identify a pair of boxes belonging to the same set of peers that have 

the same two numbers as possibilities, and eliminate these two numbers from all the boxes that have these two boxes as peers.
This method was implemented in Python as follows. 

Inline-style: 
![alt text](https://github.com/shoven/Udacity_Sudoku/blob/master/Diag.PNG)

We identify all boxes that have only two possible values. Then we identify which boxes among these have the same elements to get naked twins. Once we get the naked 

twins, we remove the corresponding digits from all the boxes that are peers to both the twins. 





# Question 2 (Diagonal Sudoku)
Q 2: How do we use constraint propagation to solve the diagonal Sudoku problem?
A: For diagonal Sudoku, I put all the diagonal entries as peers so that it acts as another constraint. the easiest way to incorporate diagonal constraint was to 

include it as an additional unit in Sudoku. This will result in not accepting solutions that do not satisfy the diagonal constraint. The code snippet below presents 

the method of implementing diagonal constraint.
Following code put diagonal constraint:

Inline-style: 
![alt text](https://github.com/shoven/Udacity_Sudoku/blob/master/Diag_Cons.PNG)


