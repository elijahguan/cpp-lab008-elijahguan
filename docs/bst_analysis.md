# Binary Search Tree Analysis

## Core operations

Students should analyze the following BST operations:

- insertion; For insertion, the best case would be when the node to be inserted becomes the root (empty tree), resulting in O(1). Average-case behavior would be for a balanced BST, where since values are split left/right by numerical size, would result in O(log n) time complexity since each iteration chooses a subtree. The worst-case behavior would be for a skewed tree where insertion could possibly require in a full traversal, and therefore O(n). Recursive and iterative implementations usually have the same complexity but can differ in the space complexity. Recursive methods have O(h) call-stack space, where h is the height of the tree. Iterative methods, on the other hand, use O(1) space for the operations. Recursive implementation will still require a stack, meaning that since the search cost depends on h (the height of the tree), a taller tree may require more comparisons. In addition, a skewed BST may end up behaving like a linked list. 
- search; For search, the best case is when the value being searched for is the root, which results in O(1) time complexity. In a balanced BST, the average time complexity is also O(log n) since each comparison chooses a subtree. In a skewed tree, which is the worst case, search may require checking almost every node, resulting in O(n). Recursive and iterative implementations usually have the same complexity but can differ in the space complexity. Recursive methods have O(h) call-stack space, where h is the height of the tree. Iterative methods, on the other hand, use O(1) space for the operations. Since the search cost depends on h (the height of the tree), a taller tree may require more comparisons. In addition, a skewed BST may end up behaving like a linked list. 
- deletion; The best case for deletion is when the node to be deleted is the root and the root has no children, which results in O(1) time complexity. In a balanced BST, deletion will become O(log n) since deletion requires finding the node along with its successor/predecessor if there is one. The skewed tree will also result in O(n) since it may require traversal through the whole tree. Recursive and iterative implementations usually have the same complexity but can differ in the space complexity. Recursive methods have O(h) call-stack space, where h is the height of the tree. Iterative methods, on the other hand, use O(1) space for the operations. Since the search cost depends on h (the height of the tree), a taller tree may require more comparisons. In addition, a skewed BST may end up behaving like a linked list. 
- traversal; For all cases (best, average, worst), the time complexity will always be O(n) since every node must be visited. Both recursive and iterative traversals require O(h) space where h is the height of the tree. The height of the tree will affect the space needed but not the O(n) time complexity.
- minimum/maximum lookup; For minimum lookup, the best case is when the root does not have a left child, meaning that the root is the minimum. For maximum lookup, the best case is when the root does not have a right child, meaning that the root is the maximum. Both of these would mean O(1) time complexity. In a balanced BST, the lookup will require O(log n) for both min/max lookup, because since smaller elements are the left child, and the greater elements are the right child, each comparison chooses a subtree. Worst case in a skewed tree will once again be O(n) because it requires traversal through almost every node. Recursive and iterative implementations usually have the same complexity but can differ in the space complexity. Recursive methods have O(h) call-stack space, where h is the height of the tree. Iterative methods, on the other hand, use O(1) space for the operations. Since the search cost depends on h (the height of the tree), a taller tree may require more comparisons. In addition, a skewed BST may end up behaving like a linked list. 
- subtree height. To find the subtree height, the algorithm needs to examine all nodes in the subtree to find the longest path from a root node to a leaf node. Therefore, its time complexity is O(n) for all cases, where n is the amount of nodes in the subtree. Recursive implementation uses O(h) space where h is the height, and the iterative implementation requires space for its nodes which also results in O(n). 

## Required discussion

Provide a short analysis comparing the complexity of the following operations:

- best-case vs. worst-case behavior;
- average-case behavior for a balanced BST;
- worst-case behavior for a skewed tree;
- recursive vs. iterative implementations;
- how tree height affects search cost.

## Expected Big-O summary

Students should identify the Big-Oh complexity for:

- `insert`: Balanced O(log n), Skewed O(n)
- `search`: Balanced O(log n), Skewed O(n)
- `remove`: Balanced O(log n), Skewed O(n)
- `inorderTraversal`: O(n)
- `height`: O(n), all nodes need to be visited

For a balanced binary search tree, expected operations are near O(log n), while a degenerate tree can degrade to O(n).
