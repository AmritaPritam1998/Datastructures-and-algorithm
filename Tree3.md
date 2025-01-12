Pre-order Traversal of Binary Trees
Pre-order Traversal is a type of Depth First Search, where each node is visited in a certain order. Read more about Binary Tree traversals in general here.

Pre-order traversal of a Binary Tree looks like this:

R
A
B
C
D
E
F
G
Result:

Pre-order Traverse
Pre-order Traversal is done by visiting the root node first, then recursively do a pre-order traversal of the left subtree, followed by a recursive pre-order traversal of the right subtree. It's used for creating a copy of the tree, prefix notation of an expression tree, etc.

This traversal is "pre" order because the node is visited "before" the recursive pre-order traversal of the left and right subtrees.

This is how the code for pre-order traversal looks like:

Example
Python:

def preOrderTraversal(node):
    if node is None:
        return
    print(node.data, end=", ")
    preOrderTraversal(node.left)
    preOrderTraversal(node.right)
The first node to be printed is node R, as the Pre-order Traversal works by first visiting, or printing, the current node (line 4), before calling the left and right child nodes recursively (line 5 and 6).

The preOrderTraversal() function keeps traversing the left subtree recursively (line 5), before going on to traversing the right subtree (line 6). So the next nodes that are printed are 'A' and then 'C'.

The first time the argument node is None is when the left child of node C is given as an argument (C has no left child).

After None is returned the first time when calling C's left child, C's right child also returns None, and then the recursive calls continue to propagate back so that A's right child D is the next to be printed.

The code continues to propagate back so that the rest of the nodes in R's right subtree gets printed.

