# n-puzzle with A*

This project implements an **A*** algorithm to solve the **n x n sliding puzzle**, also known as Gem Puzzle, Boss Puzzle, Mystic Square, etc. The algorithm combines two heuristics: 
- **Manhattan Distance** 
- **Linear Conflict**

The **Manhattan Distance** heuristic provides a basic estimate of the cost to solve the puzzle by summing the minimum number of moves each tile needs to reach its goal position. The **Linear Conflict** heuristic improves on Manhattan Distance by identifying pairs of tiles in the same row or column that must swap positions. Each conflict adds 2 additional moves to the heuristic, making it more accurate and informed. This improvement proved to reduce the number of incorrect paths explored and improve performance for larger puzzles. Using **Manhattan Distance with Linear Conflict**, the algorithm often explores fewer states and solves puzzles faster compared to using Manhattan Distance alone.

Note: The **time and cost** depend significantly on how "scrambled" the initial state is. Highly scrambled states may require significantly more time to reach the solution. While the algorithm is effective for small to medium-sized puzzles, solving highly scrambled or very large puzzles (6x6, 7x7, etc) remains computationally expensive.