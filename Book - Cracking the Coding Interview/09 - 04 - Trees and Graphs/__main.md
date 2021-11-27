# Trees and Graphs - Main

---

- __(*) Trees and graphs.__
- __(1) What type of data structure is a tree?__

<details>

- (1)
    - A non-linearly organised data structure.
    - This is unlike an array or a linked list.

</details>

---

- __(*) Trees and graphs.__
- __(1) In any algorithm regarding a tree, what two things must be evaluated?__

<details>

- The worst case time.
- The average case time.

<!---->

- These times may vary wildly.

</details>

---

- __(*) Trees and graphs.__
- __(1) What is a tree a type of?__

<details>

- (1) A graph.

</details>

---

__What must you clarify with the interviewer?__

<details>

- The definitions of terms.
- These can vary between sources.

</details>

---

## Types of Trees

---

__Detail what a tree is. (4 points. 1 point. 4 points.)__

<details>

- (1) A tree is a data structure composed of __nodes__.
- (2) Each tree has a __root node__.
- (3) The root node has __zero or more child nodes__.
- (4) Each child node has __zero or more child nodes__.

+ A tree cannot contain cycles.

- Nodes:  
    - May or may not be in a particular order.
    - Could have any data type as values.
    - May or may not have links back to their parent nodes.
    - If it has no children, it is called a "leaf" node.

</details>

---

__Code a simple class definition for a Node.__

<details>

- ![](./simpleNodeCode1.png)
- ![](./simpleNodeCode2.png)
    - The Tree class is optional.

</details>

---

### Trees vs. Binary Trees

---

__What is a binary tree?__

<details>

- A tree in which each node has up to two children.

</details>

---

### Binary Tree vs. Binary Search Tree

---

__What is a binary search tree?__

<details>

- A binary tree where each node satisfies the following condition:
    - Given that the value of the node is `n`,
    - all left descendents `< n <` all right descendents
- This is for a tree that cannot have duplicate node values.
- For trees that can have duplicate node values,
  the condition is one of the following:
    - all left descendents `<= n <` all right descendents
    - all left descendents `< n <=` all right descendents
- This should be clarified with the interviewer.
- Note that the conditions state ALL decendents,
  not just the immediate children.
- ![](./binarySearchTree.png)

</details>

---

### Balanced vs. Unbalanced

---

__What is a balanced tree?__

<details>

- A tree that is "not terribly imbalanced".
- Balanced enough for time complexity: `O(log n)`
  for `insert` and `find`.
- But could be more balanced, all the way to being a "perfect binary tree".

</details>

---

__Name two common types of balanced trees.__

<details>

- Red-black trees.
- AVL trees.

</details>

---

__Name 3 types of binary trees and detail them.__

<details>

- Complete binary tree:  
    - Where every level of the tree is fully filled.
    - It is ok for the lowest level to not be filled, 
        however it must be filled left to right.
    - ![](./completeBinaryTree.png)

+ Full binary tree:
    - Where every node has either 0 or 2 children.
    - ![](./fullBinaryTree.png)

- Perfect binary tree:
    - A binary tree that is both complete and full.
    - Characteristics:
        - All leaf nodes are at the same level.
        - This level has the maximum number of nodes.
    - Rare in real life and in interviews.
    - ![](./perfectBinaryTree.png)

</details>

---

## Binary Tree Traversal

---

__Name and detail the three types of binary tree traversals.__

<details>

- In-Order Traversal  
    - ![](./inOrderTraversal.png)

+ Pre-Order Traversal
    - ![](./preOrderTraversal.png)

- Post-Order Traversal
    - ![](./postOrderTraversal.png)

</details>

---

## Binary Heaps (Min-Heaps and Max-Heaps)

---

__What is a binary min-heap and a binary max-heap?__

<details>

- Min-heap:
    - Complete binary tree.
    - Where each node is smaller than it's children.
- Max-heap:
    - ' ' '
    - ' ' ' larger than it's children.

+ There is no inherent ordering between a left and right child.

</details>

---

__What is special about the root node of a binary min/max-heap?__

<details>

- Root node:
    - Min-heap: Min element in the tree.
    - Max-heap: Max element in the tree.

</details>

---

__What are two key operations on a min-heap?__

<details>

- `insert`
- `extract_min`

</details>

---

__Detail the `insert` operation on a binary min-heap.__

<details>

- Insert the new element in the bottom row,
  in the leftmost spot (to maintain the _complete_ property of the tree).
- "Fix" the tree: Swap the element with it's parent until the appropriate spot is found.
  Essentially bubble up the minimum element.
- Time complexity: `O(log n)`, where `n` is the number of nodes in the heap.
- ![](./binaryMinHeap_insert.png)

</details>

---

__Detail the `extract_min` operation on a binary min-heap.__

<details>

- Remove the minimum element and put the last (bottom-most & right-most) element it it's place.
- Bubble down this element until the min-heap property is restored.
- It does not matter if you swap with the left or right child...
- However, you need to swap it with the smaller child in order to maintain min-heap ordering.
- Time complexity: `O(log n)`, where `n` is the number of nodes in the heap.
- ![](./binaryMinHeap_extractMin.png)

</details>

---

## Tries (Prefix Trees)

---

__What is a trie?__

<details>

- Sometimes called a prefix tree.
- Varient of an `n`-ry tree.
- A character is stored at each node.
- Each path down the tree may represent a word.
- `*` nodes / "null nodes" are often used to indicate complete words. They could be:
    - (1) A special type of child.
    - (2) Encapsulated as a boolean within the "parent" node.
- `n`:
    - (1): 1 - (`ALPHABET_SIZE` + 1)
    - (2): 0 - `ALPHABET_SIZE`
- ![](./trie.png)

</details>

---

__What is a common use case for a trie?__

<details>

- A store of the English language for quick _prefix_ lookups.

</details>

---

__Why is a hash table not suitable for a prefix lookup?__

<details>

- A hash table:
    - can quickly look up whether a string is a valid word.
    - cannot tell if a string is a prefix of any valid words.

</details>

---

__How quickly can a trie check if a string is a valid prefix?__

<details>

- In `O(K)` time where `K` is the length of the string.
- ![](./trieTimeComplexity.png)

</details>

---

__In situations when you search through the tree on related prefixes repeatedly (e.g., looking up M, then MA, then MAN, then MANY) what would be a good way to do it?__

<details>

- Keep a reference to the current node in the tree and work from there each time.

</details>

---

## Graphs

---

- __(1) What is a graph?__
- __(2) Name two types of graphs (/nodes).__
- __(3) Give two things graphs can have.__
- __(4) Name two types of graphs.__

<details>

+ (1) A collection of nodes (/vertices) with edges between (some of) them.

- (2) Graphs (and edges) can be:  
    - Directed
    - Undirected

+ (3):
    - Graphs may consist of isolated subgraphs.
    - Graphs can have cycles.

- (4):
    - Connected graph: Where there is a (direct or indirect) path between every pair of vertices.
    - Acyclic graph: One without cycles.

+ Wiki:
  - ![](./wiki_connectedGraph.png)

</details>

---

__How do a trees relate to graphs?__

<details>

- A tree is a connected graph without cycles.

</details>

---

Graph example:

![](./graphExample.png)

---

__In terms of programming, what are the two common ways to represent a graph?__

<details>

- Adjacency List
- Adjacency Matrices

</details>

---

### Adjacency List

---

__Detail an adjacency list. 3 points.__

<details>

- Every vertex stores a list of adjacent vertices.
- In an undirected graph, an edge like (a, b) will be stored twice.
- It is the most common way to represent a graph.

</details>

---

+ __(a) Detail a simple class definition for a graph and a node.__
+ __(b) Why do you need a graph class?__

<details>

- (a):
    - ![](./adjacencyListCode.png)
- (b):
    - You need the graph class because, unlike a tree,
      you can't necessarily reach all the nodes from a single node.

</details>

---

+ __(a) How can you represent a graph, as an adjacency list, without using any additional classes?__
+ __(b) Comment.__

<details>

- (a): Using an array of lists (or a hash table).
    - "Lists": arrays, arraylists, linked lists, etc.
    - e.g.:
        - ![](./graphExample.png)
        - ... can be represented as:
        - ![](./adjacencyListArray.png)
- (b):
    - More compact.
    - Not as clean.
    - Tend to use classes.

</details>

---

### Adjacency Matrices

---

- __(a) What is an adjacency matrix?__
- __(b) Detail two implementations.__
- __(c) Details two properties.__

<details>

<!---->

- (a):
    - An `N` x `N` matrix that encodes the edges between nodes.
    - `N`: The number of nodes.
- (b):
    - An `N` x `N` boolean matrix.
        - A `true` value at `matrix[i][j]` indicates an edge from node `i` to node `j`.
        - Opposite: `false`.
    - An `N` x `N` integer matrix.
        - A `1` value at `matrix[i][j]` indicates an edge from node `i` to node `j`.
        - Opposite: `0`.
- (c):
    - Undirected graph: Symmetric matrix.
    - Directed graph: Not necessarily symmetric matrix.
-  ![](adjacencyMatrix.png)

</details>

---

__How does an adjacency matrix compare to an adjacency list?__

<details>

- Less efficient.
- Adjacency list: Can easily iterate through the neighbours of a node.
- Adjacency matrix: Will need to iterate through all the nodes to identify a node's neighbours.

</details>

---

## Graph Search

---

__What are the 2 most common ways to search a graph?__

<details>

- Depth-first search (DFS)
- Breadth-first search (BFS)

</details>

---

__Describe how a depth-first search (DFS) works.__

<details>

- Start: Root or any node.
- Explore each branch completely before moving on to the next branch.
- Can explore nodes in order of their number.
- This search goes deep first before wide.

</details>

---

__Describe how a breadth-first search (BFS) works.__

<details>

- Start: Root or any node.
- Explore each neighbour before going on to any of their children.
- Can explore nodes in order of their number.
- This search goes wide first before deep.

</details>

---

__For the following graph, list the order nodes are visited for both DFS and BFS.__

![](./exampleGraphForGraphSearch.png)

<details>

- ![](./nodeList_dfs.png)
- ![](./nodeList_bfs.png)

</details>

---

__When are DFS and BFS preferred?__

<details>

- DFS is often preferred if we want to visit every node in a graph.
- BFS is often preferred if we want to find the shortest path.

</details>

---

### Depth-First Search (DFS)

---

__What type of tree traversal is a form of DFS?__

<details>

- Pre-order (and other forms).

</details>

---

__When implementing a DFS for a graph, what is one important thing you need to check?__

<details>

- Check if a node has already been visited.
- If this is not done, you risk getting stuck in an infinite loop.

</details>

---

__Detail the pseudocode for an implementation of a DFS.__

<details>

- ![](./dfsPseudocode.png)

</details>

---

### Breadth-First Search (BFS)

---

- __(1) What is the main tripping point of implementing a BFS?__
- __(2) What is the key point in implementing a BFS?__
- __(3) What is the overall design of a BFS implementation?__

<details>

- (1): The false assumption that BFS is recursive.
- (2): To use a queue.
- (3): An iterative solution involving a queue.

</details>

---

__Detail the pseudocode for an implementation of a BFS.__

<details>

- ![](./bfsPseudocode.png)

</details>

---

### Bidirectional Search

---

- (*) Bidirectional search.
- (1) What is bidirectional search used for?
- (2) How does it work?
- (3) How does it end?

<details>

- (1): Finding the shortest path between two nodes (source & destination).
- (2): Running two simultaneous breadth-first searches.
- (3): When their searches collide, a path has been found.

</details>

---

- (*) Bidirectional search.
- (1) Draw out the searched nodes when finding a path from node `s` to node `t` using a
    - (a) Breadth-first search.
    - (b) Bidirectional (breadth-first) search.
- The number of nodes b/w `s` and `t` is `d`.
- (2) Find the time complexity of (a) and (b).
- (3) By what factor is (b) faster than (a)?

<details>

- (1): (a) & (b):
    - ![](./bfsVsBs.png)
- (2):
    - ![](./bfsTimeComplexity.png)
    - (a): `O(k^d)`
    - (b): `O(k^(d/2))`
- (3): k^(d/2)

</details>

---

- Additional reading:
    - Topological Sort (pg 632).
    - Dijkstra's Algorithm (pg 633).
    - AVL Trees (pg 637).
    - Red­ Black Trees (pg 639).

---