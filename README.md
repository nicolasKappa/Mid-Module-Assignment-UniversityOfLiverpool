# Floyd's Algorithm Comparison


This repository contains Python implementations of Floyd's Algorithm for finding the shortest path in a graph. It provides both recursive and iterative versions of the algorithm for comparison.


## Table of Contents
- [Floyd's Recursive Algorithm](#floyds-recursive-algorithm)
- [Floyd's Iterative Algorithm](#floyds-iterative-algorithm)
- [Usage](#usage)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)


## Floyd's Recursive Algorithm
The `floyd_recursive` function implements Floyd's Algorithm using recursion. It computes the shortest distances between all pairs of vertices in a weighted graph.


## Floyd's Iterative Algorithm
The `floydWarshall` function provides an iterative implementation of Floyd's Algorithm. It efficiently calculates the shortest distances between all pairs of vertices in a graph.


## Usage
To use these implementations, simply copy the respective function(s) into your project. If you need to find the shortest path in a graph, call the function with the appropriate graph as an argument.

```python
# Example Usage
graph = [[0, 5, float('inf'), 10],
         [float('inf'), 0, 3, float('inf')],
         [float('inf'), float('inf'), 0, 1],
         [float('inf'), float('inf'), float('inf'), 0]]


# Using recursive algorithm
result_recursive = floyd_recursive(graph)


# Using iterative algorithm
floydWarshall(graph)


#Testing
import unittest
from Floyds_algoRecursive_vs_iterative_Website import floyd_recursive
from timeit import default_timer as timer


 class TestFloyd_recursive(unittest.TestCase):
     def test_list_int(self):
         graph = [[0, 5, float('inf'), 10],
                  [float('inf'), 0, 3, float('inf')],
                  [float('inf'), float('inf'), 0, 1],
                  [float('inf'), float('inf'), float('inf'), 0]]
         result = floyd_recursive(graph)

         expected_result = [[0, 5, 8, 9], [float('inf'), 0, 3, 4], [float('inf'), float('inf'), 0, 1], [float('inf'), float('inf'), float('inf'), 0]]
         self.assertEqual(result, expected_result)

 if __name__ == '__main__':
     unittest.main()

if __name__ == '__main__':
    start = timer()
    test()
    end = timer()
    print(f"Execution time: {end - start} seconds")



#Contributing
if you'd like to contribute to this project, feel free to fork the repository, make your changes, and submit a pull request


#License
This project is licensed under the MIT License.
