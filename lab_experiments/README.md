# AI Lab Experiments

These three experiments demonstrate graph search and constraint solving in Python. Each program uses only the Python standard library and can be run from this directory with `python ex-1.py, ex-2.py, or ex-3.py`.

## Experiment 1: Breadth First Search

**Aim:** Find a shortest path in an unweighted graph.

**Theory:** Breadth first search (BFS) explores vertices in increasing distance from the start. A FIFO queue ensures that the first discovered path to a vertex uses the fewest edges. A parent map records the path. Time and space complexity are both O(V + E).

**Algorithm:** Put the start vertex in a queue; repeatedly remove the front vertex; visit each unvisited neighbor, recording its parent and adding it to the queue. When the goal is reached, follow parent links back to the start.

**Program:** See [`ex-1.py`](ex-1.py).

**Sample result:** `BFS shortest path: A -> C -> F`

**Conclusion:** BFS finds a minimum-edge path in an unweighted graph, or reports that no path exists.

## Experiment 2: 8 Puzzle Problem

**Aim:** Find a minimum-move solution for the 8-puzzle.

**Theory:** The puzzle is represented as a tuple of nine values; 0 denotes the blank. Each legal blank move is one edge in a state graph. BFS returns a shortest solution because each move has equal cost. For a 3 by 3 board, an even inversion count indicates a solvable arrangement.

**Algorithm:** Check the board and solvability; enqueue the start state; generate states by swapping the blank with an adjacent tile; store each new state's parent and move; when the goal is found, reconstruct the moves.

**Program:** See [`ex-2.py`](ex-2.py).

**Sample initial board:**

```text
1 2 3
4 0 6
7 5 8
```

**Sample result:** `Moves: ['Down', 'Right']` and `Number of moves: 2`.

**Conclusion:** BFS returns an optimal sequence for this small unweighted puzzle. Its memory use grows quickly for states far from the goal.

## Experiment 3: 8 Queens Problem

**Aim:** Place eight queens on an 8 by 8 chessboard so that no two queens attack each other.

**Theory:** A queen attacks along rows, columns, and diagonals. Backtracking places one queen per row and rejects a column or diagonal as soon as it conflicts with an earlier queen.

**Algorithm:** Start in the first row; try each safe column; recurse to the next row; if no placement works, remove the queen and try the next column. Stop after finding a complete placement.

**Program:** See [`ex-3.py`](ex-3.py).

**Sample result:** The program prints one valid board using `Q` for queens and `.` for empty squares. A solution may differ if the search order changes.

**Conclusion:** Backtracking finds a valid arrangement while pruning partial boards that already violate the constraints.

## Experiment 4: Water Jug Problem

Find a sequence of operations that measures two liters with four-liter and three-liter jugs. The program uses breadth-first search over jug states. See [ex-4.py](ex-4.py) and the [Word lab record](ex-4.docx).

## Experiment 5: Crypt Arithmetic Problem

Solve SEND + MORE = MONEY by assigning distinct digits to the letters. The program searches digit permutations and checks the arithmetic equation. See [ex-5.py](ex-5.py) and the [Word lab record](ex-5.docx).

## Experiment 6: Missionaries and Cannibals Problem

Use breadth-first search to transport three missionaries and three cannibals safely across a river. See [ex-6.py](ex-6.py) and the [Word lab record](ex-6.docx).

## Experiment 7: Vacuum Cleaner Problem

Use a rule-based agent to clean a two-room environment. See [ex-7.py](ex-7.py) and the [Word lab record](ex-7.docx).

## Experiment 8: Breadth First Search

Traverse a graph level by level from a start vertex. See [ex-8.py](ex-8.py) and the [Word lab record](ex-8.docx).

## Experiment 9: Depth First Search

Traverse a graph by following branches deeply before backtracking. See [ex-9.py](ex-9.py) and the [Word lab record](ex-9.docx).

## Experiment 10: Travelling Salesman Problem

Find a minimum distance tour through four cities by checking all route permutations. See [ex-10.py](ex-10.py) and the [Word lab record](ex-10.docx).

## Experiment 11: A Star Search Algorithm

Find a least-cost path using path cost plus a heuristic estimate. See [ex-11.py](ex-11.py) and the [Word lab record](ex-11.docx).
