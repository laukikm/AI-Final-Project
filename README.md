Team name- Lumpus

# Life-long planning

A repository to implement the D* Lite search algorithm in a pacman environment. The agent only sees its neighboring squares,
and can store information about the locations it has visited, and the structure of the walls surrounding those locations.

If we use traditional planning algorithms like A* to plan, we have to run them each time our robot changes its state. This is 
redundant, and can be avoided by using an iterative planning approach like D* lite, which uses information computed in the previous
iterations, reducing the need to recompute.

The objective was to compare the performance of D* Lite with A* search and A* search- Tunnel Vission(TV) to corroborate that D* Lite 
performs better than A* search for big and complex enough mazes as descrobed in [this paper on D* Lite](http://idm-lab.org/bib/abstracts/papers/aaai02b.pdf) 
We present our results in terms of the number of nodes expanded for reaching the goal state and the final score achieved in the Pacman domain. 

## Results
Number of nodes expanded by the algorithms discussed above for different mazes sizes and complexities were as tabulated below.
| Maze | D* Lite | A* search | A* search (TV) |
| ------------- | ------------- | ------------- | ------------- |
| bigMaze | 10979 | 54160 | 52085 |
| mediumMaze | 3251 | 8842 | 9481 |
| SmallMaze | 669 | 548 | 582 |
| tinyMaze | 122 | 74 | 46 |

The final score achieved using the three search algortihms and different mazes were-
| Maze | D* Lite | A* search | A* search (TV) |
| ------------- | ------------- | ------------- | ------------- |
| bigMaze | 92 | 100 | 70 |
| mediumMaze | 428 | 420 | 420 |
| SmallMaze | 473 | 473 | 471 |
| tinyMaze | 502 | 502 | 502 |

## Running the tests
We have used Linux environment for this project. The corresponding commands for running the tests are given below.

To run the D* Lite algorithm on 'bigMaze', execute the following line from inside the search folder
```
python pacman.py -l bigMaze -z  -p SearchAgent -a fn=dstar,heuristic=manhattanHeuristic
```
You can replace 'dstar' with 'astar2' or 'astartv' next to 'fn' in the stated command to run the respective algorithms. 

To test on different mazes, replace 'bigMaze' in the command with another maze like 'mediumMaze', 'smallMaze', 'tinyMaze'.

A* search implemetation in Pacman domain video- https://drive.google.com/file/d/1dJxdAXtt_TP36qseuFwgjHao1YwLrx1H/view?usp=sharing

A* search- Tunnel Vision implemetation in Pacman domain video- https://drive.google.com/file/d/12yHSP5GARA5iG13dDJndBeEIUmZIvLVx/view?usp=sharing

D* Lite implemetation in Pacman domain video- https://drive.google.com/file/d/1YwP7NWzpVlkjzU_yhGjMebTtfalB7fww/view?usp=sharing

## Authors
* Sagar Khar- Research and Solution formulation
* Laukik Mujumda- Code Implementation
* Malay Tushar Nagda- Testing and Bug fixes
* Prabal Bijoy Dutta- Analysis and Report Generation
