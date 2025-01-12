A Linked List is, as the word implies, a list where the nodes are linked together. Each node contains data and a pointer. The way they are linked together is that each node points to where in the memory the next node is placed.

Linked Lists
A linked list consists of nodes with some sort of data, and a pointer, or link, to the next node.
A big benefit with using linked lists is that nodes are stored wherever there is free space in memory, the nodes do not have to be stored contiguously right after each other like elements are stored in arrays. Another nice thing with linked lists is that when adding or removing nodes, the rest of the nodes in the list do not have to be shifted.

Linked Lists vs Arrays
The easiest way to understand linked lists is perhaps by comparing linked lists with arrays.

Linked lists consist of nodes, and is a linear data structure we make ourselves, unlike arrays which is an existing data structure in the programming language that we can use.

Nodes in a linked list store links to other nodes, but array elements do not need to store links to other elements.

Note: How linked lists and arrays are stored in memory will be explained in more detail on the next page.

The table below compares linked lists with arrays to give a better understanding of what linked lists are.

Arrays	Linked Lists
An existing data structure in the programming language	Yes	No
Fixed size in memory	Yes	No
Elements, or nodes, are stored right after each other in memory (contiguously)	Yes	No
Memory usage is low
(each node only contains data, no links to other nodes)	Yes	No
Elements, or nodes, can be accessed directly (random access)	Yes	No
Elements, or nodes, can be inserted or deleted in constant time, no shifting operations in memory needed.	No	Yes
To explain these differences in more detail, the next page will focus on how linked lists and arrays are stored in memory.