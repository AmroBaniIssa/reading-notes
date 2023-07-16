Trees

types of trees:
 -Binary Trees:  number of children restrict  to two 
 -K-ary Trees: number of children more than two
 -Binary Search Trees: in a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.


Common Terminology
  -Node - A Tree node is a component which may contain its own values, and references to other nodes
  -Root - The root is the node at the beginning of the tree
  -K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
  -Left - A reference to one child node, in a binary tree
  -Right - A reference to the other child node, in a binary tree
  -Edge - The edge in a tree is the link between a parent and child node
  -Leaf - A leaf is a node that does not have any children
  -Height - The height of a tree is the number of edges from the root to the furthest leaf

Traversals
  An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:

  Depth First: Depth first traversal is where we prioritize going through the depth (height) of the tree first
   1- Pre-order: root >> left >> right
   2- In-order: left >> root >> right
   3-Post-order: left >> right >> root
  
  Breadth First: Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.
   traverse Breadth process by dequeuing and processing the Nodes at the front of the queue, followed by enqueing the current Node’s children continues until our queue is empty of child Nodes:

Big O
-The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.

-The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.

-The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.

-The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree. For example, in the above tree, w is 4.

-A “perfect” binary tree is one where every non-leaf node has exactly two children. The maximum width for a perfect binary tree, is 2^(h-1), where h is the height of the tree. Height can be calculated as log n, where n is the number of nodes.