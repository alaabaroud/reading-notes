

# Trees -- Data Structure

-  trees are hierarchical data structures, unlike the Arrays, linked lists, stack and queue which are linar. that means that trees can allow us to search for a specific node of any type of data, without caring much about the order.
Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).

here are some terms that we should keep in mind:

-  Node: the items of a tree.
- Root: First node of the tree
- K:  A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left:  A reference to one child node, in a binary tree
- Right: A reference to the other child node, in a binary tree
- Edge: The edge in a tree is the link between a parent and child node
- Leaf: A leaf is a node that does not have any children
- Height: The height of a tree is the number of edges from the root to the furthest leaf.
------------------------------

## Traversals:

***Depth First***
is an algorithm for traversing or searching tree data structure. The algorithm starts at the root node
the methods: 
Pre-order:( root to right):

in which  means that the root has to be looked at first.
In-order: (left to  right):
from the beginnig to the end.
Post-order: (left to  root)
in which means that the left side will be the first to look for.
--------------------------

 going through each level of the tree node-by-node Is ***Breadth First traversal*** and it uses a queue.
 
 
