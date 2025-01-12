Post-order Traversal of Binary Trees
Post-order Traversal is a type of Depth First Search, where each node is visited in a certain order. Read more about Binary Tree traversals in general here.

Doing a Post-order Traversal on a Binary Tree can be visualized like this:

R
A
B
C
D
E
F
G
Result:

Post-order Traverse
Post-order Traversal works by recursively doing a Post-order Traversal of the left subtree and the right subtree, followed by a visit to the root node. It is used for deleting a tree, post-fix notation of an expression tree, etc.

What makes this traversal "post" is that visiting a node is done "after" the left and right child nodes are called recursively.

This is how the code for Post-order Traversal looks like:

Example
Python:

def postOrderTraversal(node):
    if node is None:
        return
    postOrderTraversal(node.left)
    postOrderTraversal(node.right)
    print(node.data, end=", ")
The postOrderTraversal() function keeps traversing the left subtree recursively (line 4), until None is returned when C's left child node is called as the node argument.

After C's left child node returns None, line 5 runs and C's right child node returns None, and then the letter 'C' is printed (line 6).

This means that C is visited, or printed, "after" its left and right child nodes are traversed, that is why it is called "post" order traversal.

The postOrderTraversal() function continues to propagate back to previous recursive function calls, so the next node to be printed is 'D', then 'A'.

The function continues to propagate back and printing nodes until all nodes are printed, or visited.