In-order Traversal of Binary Trees
In-order Traversal is a type of Depth First Search, where each node is visited in a certain order. Read more about Binary Tree traversals in general here.

Run the animation below to see how an In-order Traversal of a Binary Tree is done.

R
A
B
C
D
E
F
G
Result:

In-order Traverse
In-order Traversal does a recursive In-order Traversal of the left subtree, visits the root node, and finally, does a recursive In-order Traversal of the right subtree. This traversal is mainly used for Binary Search Trees where it returns values in ascending order.

What makes this traversal "in" order, is that the node is visited in between the recursive function calls. The node is visited after the In-order Traversal of the left subtree, and before the In-order Traversal of the right subtree.

This is how the code for In-order Traversal looks like:

Example
Python:

def inOrderTraversal(node):
    if node is None:
        return
    inOrderTraversal(node.left)
    print(node.data, end=", ")
    inOrderTraversal(node.right)
The inOrderTraversal() function keeps calling itself with the current left child node as an argument (line 4) until that argument is None and the function returns (line 2-3).

The first time the argument node is None is when the left child of node C is given as an argument (C has no left child).

After that, the data part of node C is printed (line 5), which means that 'C' is the first thing that gets printed.

Then, node C's right child is given as an argument (line 6), which is None, so the function call returns without doing anything else.

After 'C' is printed, the previous inOrderTraversal() function calls continue to run, so that 'A' gets printed, then 'D', then 'R', and so on.

