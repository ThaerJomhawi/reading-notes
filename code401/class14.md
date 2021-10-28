# Trees



- A Tree node is a component which may contain it’s own values, and references to other nodes
- The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node, in a binary tree
- Right - A reference to the other child node, in a binary tree
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
- Height - The height of a tree is the number of edges from the root to the furthest leaf

## Traversals

Traversing a tree allows us to search for a node, print out the contents of a tree, and much more.

**Depth First** :Depth first traversal is where we prioritize going through the depth (height) of the tree first. the Three methods for depth first traversal:

- `Pre-order`: root >> left >> right
- `In-order`: left >> root >> right
- `Post-order`: left >> right >> root

**[Pre-order]**

```java
ALGORITHM preOrder(root)
// INPUT <-- root node
// OUTPUT <-- pre-order output of tree node's values
    OUTPUT <-- root.value
    if root.left is not Null
        preOrder(root.left)
    if root.right is not NULL
        preOrder(root.right)
```

**[in-order]**

```java
/* ALGORITHM inOrder(root) */
// INPUT <-- root node
// OUTPUT <-- in-order output of tree node's values
    if root.left is not NULL
        inOrder(root.left)
    OUTPUT <-- root.value
    if root.right is not NULL
        inOrder(root.right)
```

**[Post-order]**

```java
/* ALGORITHM postOrder(root) */
// INPUT <-- root node
// OUTPUT <-- post-order output of tree node's values
    if root.left is not NULL
        postOrder(root.left)
    if root.right is not NULL
        postOrder(root.right)
    OUTPUT <-- root.value
```

## Breadth First

Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

```java
ALGORITHM breadthFirst(root)
// INPUT  <-- root node
// OUTPUT <-- front node of queue to console

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while breadth.peek()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)
```

## Binary Tree Vs K-ary Trees

There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows.

If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use `K` to refer to the maximum number of children that each Node is able to have.

## Adding a node

strategy for adding a new node to a binary tree is to fill all “child” spots from the top down. To do so, we would leverage the use of breadth first traversal. During the traversal, we find the first node that does not have all it’s children filled, and insert the new node as a child. We fill the child slots from left to right.

## Big O

- The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n).

- The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree.

- A “perfect” binary tree is one where every non-leaf node has exactly two children.

## Binary Search Trees



A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the `root` are placed to the left, and all values that are larger than the `root` are placed to the right.