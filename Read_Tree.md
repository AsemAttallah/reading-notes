# Tree
## Common Terminology in tree
* Node - A Tree node is a component which may contain its own values, and references to other nodes.

* Root - The root is the node at the beginning of the tree.
* K - A number that specifies the maximum number of children any node may have in a k-ary tree.
* Left - A reference to one child node, in a binary tree.
* Right - A reference to the other child node, in a binary tree.
* Edge - The edge in a tree is the link between a parent and child node.
* Leaf - A leaf is a node that does not have any children.
* Height - The height of a tree is the number of edges from the root to the furthest leaf.

## Traversals
### There are two categories of traversals when it comes to trees:
* Depth First 
* Breadth First
##  Depth First
### Depth first traversal is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the root. Here are three methods for depth first traversal:

* Pre-order: root >> left >> right
* In-order: left >> root >> right
* Post-order: left >> right >> root
### The most common way to traverse through a tree is to use recursion. With these traversals, we rely on the call stack to navigate back up the tree when we have reached the end of a sub-path.

##  Breadth First
### Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.
### Traditionally, breadth first traversal uses a queue (instead of the call stack via recursion) to traverse the width/breadth of the tree. Let’s break down the process.



### Big O
* The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.

* The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree