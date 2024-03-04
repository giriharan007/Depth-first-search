# Depth-first-search
Depth First Search (DFS) is a popular algorithm for traversing or searching tree or graph data structures. In the context of a maze puzzle game, DFS can be used to find a path from the starting point to the goal within the maze. Here's a simple explanation of how DFS works in the context of a maze puzzle game:

1. **Setup**: You start at the entrance of the maze (the starting point) and you want to find a path to the exit (the goal).

2. **Algorithm**:
   - Start at the entrance of the maze.
   - Explore one of the adjacent cells that hasn't been visited yet.
   - If you encounter a wall, backtrack to the previous cell and explore a different direction.
   - Repeat this process until you reach the exit or until you've explored all possible paths.

3. **Implementation**:
   - You can implement DFS using recursion or by using a stack data structure.
   - In the recursive approach, you would recursively explore neighboring cells until you find the exit or until there are no more unvisited cells to explore.
   - In the stack-based approach, you would push cells onto a stack as you explore them and backtrack if necessary.

4. **Pseudocode** (Recursive DFS):
   ```
   function DFS(currentCell):
       if currentCell is the exit:
           return true
       mark currentCell as visited
       for each neighbor of currentCell:
           if neighbor is not a wall and neighbor is not visited:
               if DFS(neighbor) returns true:
                   return true
       return false
   ```

5. **Notes**:
   - You need to keep track of visited cells to avoid infinite loops.
   - You can represent the maze as a 2D grid, where each cell can be either a wall or a passage.
   - You can define rules for movement, such as allowing movement in four directions (up, down, left, right) or eight directions (including diagonals).
   - DFS doesn't guarantee finding the shortest path. It might find a path to the exit, but it might not be the shortest one.

By applying DFS in a maze puzzle game, you can systematically explore the maze and find a path from the entrance to the exit.
