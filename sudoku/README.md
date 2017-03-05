# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: In constraint propagation we use constraints to make the search space more simple. In the naked twins problem the constraint
is that no other boxes in the same unit(s) as both naked twins can have digits which compose value of both naked twin boxes.
By eliminating these digits from all units containing all naked twin boxes we can make out sudoku game simpler to solve. By
exploiting opportunties to propagate constraints via elimination, single choice or naked twins strategies we get closer to 
the solution. 


# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: We build on existing solution for regular sudoku game by defining two new units - one for each diagonal. This units are 
then added to the unit list and help to define new dictionary of peers for every sudoku box. The strategies to solve the game
such as elimination, single choice and naked twins do not change in principle but we use new definitions of units and peers to
solve the game by enforcing new set of constraints which in addition to previous constraints contain two new constraints such 
that the digits 1-9 should appear on both diagonals only once. As previously we use constraint propagation in the new constraint
space to reduce the search space and find the solution. 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

