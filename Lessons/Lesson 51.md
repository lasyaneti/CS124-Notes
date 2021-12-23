# 11/05/21: Graph Algorithms

Graphs don't have a linear order, use getNode() for a random starting point
```java
graph.getNode();
```

## Graph Traversal
Connected graphs can be traversed using a **set to keep track of visisted** and call neighbors recursively to keep exploring other nodes
```java
void traverse(GraphNode<Integer> node, Set<GraphNode<Integer>> visited) {
    // Base case
    if (visited.contains(node)) {
        return; 
    }
    visited.add(node);
    // Recurse to visit all neighbors
    for (GraphNode<Integer> neighbor : node.getNeighbors()) {
        traverse(neighbor, visited)
    }
}
```

## Graph Cycle

![Visual](/Images/GraphCycle.png)

- In connected graphs, a cycle is a path where you start from node A back to node A by visiting each edge no more than once 
- **Set cannot be used to write a graph cycle algorithm** because the way we establish this set, it cannot differentiate between the following paths:
  - node A -> node B -> node C = **cycle**
  - node A -> node B -> node A -> node B -> node C -> node A = **backtracking**
- We need a new data structure for this algorithm: create a new list to pass all neighors so each path will independently ensure it's going in a cycle. 
- Logic: when you are backtracking, the current node is the second to last item in the list vs. in a cycle you take a whole new path so the current node is not the second to last item in the list. Trick is to look at the position of the visited node in the path list.

```java
boolean hasCycle(GraphNode<Integer> node, List<GraphNode<Integer>> path) {
  if (path.contains(node)) {
    return path.indexOf(node) != (path.size() - 2);
  }
  path.add(node);
  for (GraphNode<Integer> neighbor : node.getNeighbors()) {
    if (hasCycle(neighbor, new ArrayList<>(path))) {
      return true;
    }
  }
  return false;
}
```