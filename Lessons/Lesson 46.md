# 10/28/21: Trees

| Word | Meaning |
| ---- | ------- |
| Child | Node referenced by parent node, child can only have 1 parent |
| Root | Node at the top of the tree |
| Leaf | Node with no children |
| Subtree | Portion of tree |
| Level | # of esges from the root to the node |
| Height/depth | Max levles in a tree | 

![Visual](/Images/TreeLevels.png)

## Recursively Creating a Tree

```java
public class Binarytree {
    private Object value;
    private BinaryTree left;
    private BinaryTree right;
    // Constructor for leaf
    public BinaryTree(Object setValue) {
        value = setValue;
        // Left are right are null
    }
    public BinaryTree(Object setValue, Object l, Object r) {
        value = setValue;
        l = BinaryTree(l);
        r = BinaryTree(r);
    }
}
```