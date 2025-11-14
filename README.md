# Data Structures and Algorithms Library

## Overview

A comprehensive Python implementation of fundamental data structures and algorithms. This repository serves as both a reference implementation and a practical toolkit for understanding core computer science concepts. Each implementation emphasizes clarity, correctness, and educational value.

## Table of Contents

- [Data Structures](#data-structures)
- [Algorithms](#algorithms)
- [Features](#features)
- [Implementation Highlights](#implementation-highlights)
- [Usage](#usage)
- [Educational Value](#educational-value)
- [Technical Details](#technical-details)

## Data Structures

### Linear Data Structures

#### **Linked Lists**
- **LinkedList.py** - Singly linked list with insertion, deletion, and traversal
- **DoublyLinkedList.py** - Bidirectional linked list for efficient reverse traversal
- **CircularLinkedList.py** - Circular linked list for round-robin applications

#### **Stacks and Queues**
- **Stack.py** - LIFO (Last In First Out) data structure
- **Queue.py** - FIFO (First In First Out) data structure
- **Queue_LinkedList.py** - Queue implementation using linked list
- **CircularQueue.py** - Fixed-size circular buffer implementation

### Tree-Based Data Structures

#### **Binary Search Trees**
- **BinarySearchTree.py** - Basic BST with search, insert, and delete operations
- **BinarySearchTreeFullImplementation.py** - Complete BST with advanced operations
- **AVLTree.py** - Self-balancing BST with height-balancing rotations
- **RedBlackTree.py** - Self-balancing BST with red-black properties

#### **Heap**
- **MaxHeap.py** - Priority queue implementation with O(log n) operations

### Hash-Based Data Structures

- **HashTable.py** - Hash table with collision resolution via linear probing
- **HashSet.py** - Set implementation using hashing for O(1) membership testing

### Advanced Data Structures

- **Graph.py** - Graph representation with adjacency list
- **Graph with AdjacencyMatrix.py** - Alternative graph implementation using matrix
- **SkipList.py** - Probabilistic data structure for fast search in ordered sequences

## Algorithms

### Sorting Algorithms

**File:** `Sorting Algorithms.py`

- **Bubble Sort** - Simple comparison-based sorting (O(n²))
- **Insertion Sort** - Efficient for small datasets and nearly sorted data
- **Selection Sort** - In-place comparison sort
- **Merge Sort** - Divide-and-conquer stable sort (O(n log n))
- **Quick Sort** - Efficient in-place sorting algorithm
- **Shell Sort** - Optimization of insertion sort with gap sequences
- **Heap Sort** - Comparison-based sort using heap data structure

### Search Algorithms

**File:** `Search Algorithms.py`

- **Linear Search** - Sequential search through unsorted data (O(n))
- **Binary Search** - Efficient search in sorted arrays (O(log n))
- **Interpolation Search** - Improved binary search for uniformly distributed data

## Features

### Code Quality
- Clean, readable Python implementations
- Consistent naming conventions and structure
- Well-documented methods and classes
- Educational comments where appropriate

### Comprehensive Coverage
- 17 different data structure implementations
- Multiple algorithm categories (sorting, searching)
- Both basic and advanced implementations
- Multiple approaches to similar problems

### Practical Applications
- Real-world use case demonstrations
- Performance considerations included
- Space-time complexity awareness
- Collision resolution strategies

## Implementation Highlights

### Self-Balancing Trees
The AVL and Red-Black tree implementations demonstrate:
- Automatic height balancing
- Rotation operations (left, right, left-right, right-left)
- O(log n) guaranteed search time
- Insertion and deletion with rebalancing

### Hash Table with Collision Resolution
- Custom hash function implementation
- Linear probing for collision handling
- Dynamic key-value storage
- Python dictionary-like interface (`__getitem__`, `__setitem__`)

### Graph Implementations
Two approaches for different use cases:
- **Adjacency List** - Space-efficient for sparse graphs
- **Adjacency Matrix** - Fast edge lookup for dense graphs

### Advanced Sorting
Multiple sorting algorithms showcasing:
- Different time complexity trade-offs
- Stable vs unstable sorting
- In-place vs auxiliary space requirements
- Recursive vs iterative approaches

## Usage

### Basic Example - Hash Table
```python
from DataStructures.HashTable import HashTable

# Create and use hash table
ht = HashTable()
ht['name'] = 'John'
ht['age'] = 30

print(ht['name'])  # Output: John
```

### Example - AVL Tree
```python
from DataStructures.AVLTree import AVLTree, Node

# Create AVL tree
tree = AVLTree()
root = None

# Insert elements
root = tree.insert(root, 10)
root = tree.insert(root, 20)
root = tree.insert(root, 30)

# Tree automatically balances itself
```

### Example - Sorting
```python
from Algorithms.SortingAlgorithms import bubble_sort, MergeSort

# Bubble sort
data = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(data)

# Merge sort
unsorted = [38, 27, 43, 3, 9, 82, 10]
sorted_data = MergeSort.merge_sort(unsorted)
```

### Example - Graph Traversal
```python
from DataStructures.Graph import Graph, Vertex

# Create graph
g = Graph()

# Add vertices
a = Vertex('A')
b = Vertex('B')
g.add_vertex(a)
g.add_vertex(b)

# Add edge
g.add_edge('A', 'B')
```

## Educational Value

### Learning Objectives

This repository helps understand:

1. **Time Complexity Analysis**
   - Big O notation in practice
   - Trade-offs between different approaches
   - When to use which data structure

2. **Space Complexity**
   - Memory efficiency considerations
   - In-place vs auxiliary space algorithms
   - Recursion stack implications

3. **Design Patterns**
   - Iterator pattern in linked structures
   - Strategy pattern in sorting algorithms
   - Template method in tree operations

4. **Problem-Solving Techniques**
   - Divide and conquer (Merge Sort)
   - Dynamic programming concepts
   - Greedy algorithms
   - Backtracking possibilities

### Interview Preparation

Covers common technical interview topics:
- Data structure implementation from scratch
- Algorithm complexity analysis
- Problem-solving approaches
- Code organization and style

## Technical Details

### Requirements
- Python 3.x
- No external dependencies
- Pure Python implementations

### Design Decisions

**Object-Oriented Approach**
- Encapsulation of data structure internals
- Clear separation of concerns
- Reusable and extensible code

**Pythonic Conventions**
- Magic methods (`__len__`, `__repr__`, `__getitem__`)
- Type hints where applicable
- Class methods and static methods

**Performance Considerations**
- Optimal algorithm choices
- Efficient memory usage
- Consideration of Python's performance characteristics

## Time Complexity Reference

### Data Structures

| Operation | LinkedList | AVL Tree | Hash Table | Heap |
|-----------|-----------|----------|------------|------|
| Search    | O(n)      | O(log n) | O(1)*      | O(n) |
| Insert    | O(1)      | O(log n) | O(1)*      | O(log n) |
| Delete    | O(n)      | O(log n) | O(1)*      | O(log n) |
| Access    | O(n)      | O(log n) | O(1)*      | O(1) |

*Average case with good hash function

### Algorithms

| Algorithm | Best | Average | Worst | Space |
|-----------|------|---------|-------|-------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) |
| Linear Search | O(1) | O(n) | O(n) | O(1) |
| Binary Search | O(1) | O(log n) | O(log n) | O(1) |

## Use Cases

### When to Use Each Data Structure

- **LinkedList**: Dynamic size, frequent insertions/deletions at beginning
- **AVL Tree**: Frequent searches, need balanced height
- **Red-Black Tree**: Good balance between search and update operations
- **Hash Table**: Fast key-value lookups, unique keys
- **Heap**: Priority queue, finding min/max efficiently
- **Graph**: Modeling relationships, network algorithms
- **Skip List**: Alternative to balanced trees, simpler implementation

## Future Enhancements

Potential additions:
- Unit tests for all implementations
- Performance benchmarking suite
- Visualization tools
- More advanced algorithms (graph algorithms, dynamic programming)
- Additional data structures (Trie, B-Tree, Bloom Filter)
- Jupyter notebooks with examples

## Contributing

This repository serves as a learning resource and portfolio piece. Suggestions and improvements are welcome.

## License

Available for educational and reference purposes.

## Contact

For questions or collaboration opportunities, please reach out through GitHub.

---

**Note**: These implementations prioritize clarity and educational value. For production use, consider Python's built-in data structures (`list`, `dict`, `set`, `heapq`, `collections.deque`) or established libraries.