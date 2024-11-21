# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

In practical applications, both search algorithms are effective in finding the solution in a reasonable timeframe with at most a few hundred iterations (very fast for a computer). In terms of time complexity, using DFS is more likely to result in less iterations to solve any given puzzle compared to BFS. This is even moreso the case when a heuristic is introduced that would guide the search in the direction of the solution faster and minimize pointless checks. For solving sudoku puzzles, DFS might be better, but in other applications BFS may prove more effecient when a heuristic is available that could prioritize more accurate solutions.

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

Using a stack made the search algorithm fully exhaust every search path before moving on to the next nearest one, hence the name "depth-first". Using a queue made the search algorithm prioritize all the queued up items, which may include items that are adjacent to ones you have already checked. While we implemented the search algorithm this time using a while loop, a similar effect could be achieved using recursion.

3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

The DFS and BFS implementations are very generic, and so adapting the solution into a solver for other kinds of puzzles or grid-based logic games would be a matter of changing the board class to represent those games instead of Sudoku. Additionally, for certain games like Chess, you would need to implement depth limits and state value heuristics as it would be nearly impossible to check every state (if you could, you'd make an unbeatable chess bot!) In terms of real-world problem-solving, it teaches us to be smart about how we search for solutions. Realistically, I do programming freelancing, so knowing more about these computer science principles is always useful for me, even if I don't always use it.