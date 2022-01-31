
# Grid Navigator: AI Programming Assignment Overview

- Created a search agent that solves a grid puzzle using multiple Algorithms
  - A-star with and without showing steps 
  - theta star
  - Genetic algorithm  
- the program allows the user to set parameters for grid size and draw the grid manually 

## Code and Resources Used

**Packages:** Tkinter, heapq\
**Grid Creation Github:** https://github.com/misbah4064/A_Star_Python  
for this programming assignment, no external AI packages were allowed all algorithms must be built from scratch

## Grid Creation

heavily modified grid creation to allow for custom grid size and grid drawing.
Also, allowed the user to specify start and goal points.

## A-Star

the A-star algorithm which uses a priority queue to minimize `F(n)` which is the sum of the distance from the starting point to the current point `g(n)` as well as the heuristic `h(n)` which has been set to be the Manhattan distance from current to goal.

![Sample run of A-Star](https://i.imgur.com/JQV7rM0.png)

## Theta-Star

 unlike the A-star algorithm, the theta star algorithm does not require the parent of the node to be a direct neighbor if it can be reached directly from it. which means it has a line of sight (i.e., there is no obstacle in between them).

 ![Sample run of Theta-Star](https://i.imgur.com/bt49lBd.png)

 ## Genetic Algorithm

 A Genetic algorithm is an algorithm that starts by filling a set with random values to variables which in this situation is a sequence of encoded moves. Then, makes new generations by crossing over between parent chromosomes and making children, then picks the best solution after running for multiple generations. Please note that my solution is not perfect and that is because the length of the sequence of moves must be predetermined. Also, the fitness function must be very complex in the sense that it must factor in walls and obstacles.\
 encoded moves are:
- 00 = down
- 10 = left
- 01 = right
- 11 = up
- 02 = stay 


 Please note that the genetic algorithm can be fixed by factoring in walls in the fitness function and writing a repair function to fix chromosomes that run into walls instead of discarding them.

![Sample run of Genetic Algorithm](https://i.imgur.com/KpN06Sj.png)

## Performance Comparison

![table showing performance measures for different algorithms](https://i.imgur.com/FWXHa9v.png)
