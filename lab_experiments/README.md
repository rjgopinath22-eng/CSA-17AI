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

## Experiment 12: Map Coloring using CSP

Assign colors to the Australia map so adjacent regions differ. See [ex-12.py](ex-12.py) and [ex-12.docx](ex-12.docx). (CO2)

## Experiment 13: Tic Tac Toe Game

Play a two-player console game with legal move checks and win/draw detection. See [ex-13.py](ex-13.py) and [ex-13.docx](ex-13.docx). (CO5)

## Experiment 14: Minimax Algorithm

Select an optimal Tic-Tac-Toe move using minimax. See [ex-14.py](ex-14.py) and [ex-14.docx](ex-14.docx). (CO3)

## Experiment 15: Alpha Beta Pruning

Apply alpha-beta pruning to the Tic-Tac-Toe minimax search. See [ex-15.py](ex-15.py) and [ex-15.docx](ex-15.docx). (CO3)

## Experiment 16: Decision Tree

Build an ID3 decision tree from categorical weather data. See [ex-16.py](ex-16.py) and [ex-16.docx](ex-16.docx). (CO3)

## Experiment 17: Feed Forward Neural Network

Compute hidden and output activations for a small sigmoid network. See [ex-17.py](ex-17.py) and [ex-17.docx](ex-17.docx). (CO3)

## Experiment 18: Sum Integers in Prolog

Use recursion to sum integers from one through N. See [ex-18.pl](ex-18.pl) and [ex-18.docx](ex-18.docx). (CO4)

## Experiment 19: Names and Dates of Birth Database

Store and query names with dates of birth. See [ex-19.pl](ex-19.pl) and [ex-19.docx](ex-19.docx). (CO4)

## Experiment 20: Student Teacher Subject Code Database

Store student, teacher, subject, and course-code records as Prolog facts. See [ex-20.pl](ex-20.pl) and [ex-20.docx](ex-20.docx). (CO5)

## Experiment 21: Planets Database

Store planet names, order from the Sun, and type in Prolog facts. See [ex-21.pl](ex-21.pl) and [ex-21.docx](ex-21.docx). (CO4)

## Experiment 22: Towers of Hanoi

A recursive Prolog solution that prints the disk moves. See [ex-22.pl](ex-22.pl) and [ex-22.docx](ex-22.docx). (CO4)

## Experiment 23: Bird Flight Queries

Query whether listed birds can fly and enumerate answers through backtracking. See [ex-23.pl](ex-23.pl) and [ex-23.docx](ex-23.docx). (CO4)

## Experiment 24: Family Tree

Store parent facts and query sibling, grandparent, and ancestor relationships. See [ex-24.pl](ex-24.pl) and [ex-24.docx](ex-24.docx). (CO4)

## Experiment 25: Diet Suggestions by Disease

Retrieve illustrative sample food lists based on a condition label. This is a programming example, not health guidance. See [ex-25.pl](ex-25.pl) and [ex-25.docx](ex-25.docx). (CO4)

## Experiment 26: Monkey and Banana Problem

Search a small state space for actions that let the monkey reach the banana. See [ex-26.pl](ex-26.pl) and [ex-26.docx](ex-26.docx). (CO4)

## Experiment 27: Fruit and Color Backtracking

Use Prolog facts and backtracking to enumerate fruit and color matches. See [ex-27.pl](ex-27.pl) and [ex-27.docx](ex-27.docx). (CO4)

## Experiment 28: Best First Search

Prioritize graph nodes using heuristic values. See [ex-28.pl](ex-28.pl) and [ex-28.docx](ex-28.docx). (CO4)

## Experiment 29: Medical Diagnosis Rule Example

Use sample symptom facts and rules to infer possible labels. This is a programming example, not medical guidance. See [ex-29.pl](ex-29.pl) and [ex-29.docx](ex-29.docx). (CO4)

## Experiment 30: Forward Chaining

Repeatedly apply rules to known facts until reaching closure. See [ex-30.pl](ex-30.pl) and [ex-30.docx](ex-30.docx). (CO4)

## Experiment 31: Backward Chaining

Prove goals from facts and rule conditions. See [ex-31.pl](ex-31.pl) and [ex-31.docx](ex-31.docx). (CO4)
