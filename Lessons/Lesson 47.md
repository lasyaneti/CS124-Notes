# 10/29/21: Trees and Recursion

## Tree Search
Tree search recursive algorithms can be extremely efficient because you can return the answer if the match is found, i.e. no need to recurse the entire tree!

```java
import cs125.trees.BinaryTree;

boolean searchTree(BinaryTree tree, Object lookingFor) {
    // Base case
    if (tree == null) {
        return false;
    }
    // Check at every point in time
    if (tree.getValue().equals(lookingFor)) {
        return true;
    }
    // Use or because function return booleann
    return searchTree(tree.getLeft(), lookingFor) || searchTree(tree.getRight(), lookingFor);
}
```

## Count Tree Nodes
```java
import cs125.trees.BinaryTree;

int countNodes(BinaryTree tree) {
    if (tree == null) {
        return 0;
    }
    return 1 + countNodes(tree.getLeft()) + countNodes(tree.getRight());
}
```